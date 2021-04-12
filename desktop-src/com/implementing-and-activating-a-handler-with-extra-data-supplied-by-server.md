---
title: Implementar y activar un controlador con datos adicionales proporcionados por el servidor
description: Implementar y activar un controlador con datos adicionales proporcionados por el servidor
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104361772"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementar y activar un controlador con datos adicionales proporcionados por el servidor

Si el servidor desea incluir algunos datos adicionales en el paquete para que los use el controlador, el servidor debe implementar las interfaces [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) y [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) . El servidor debe agregar el serializador estándar y debe delegar la primera parte del cálculo de referencias en el contador de referencias estándar agregado, incluido [**IMarshal:: GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), y debe agregar su propio tamaño de datos al tamaño devuelto por la propiedad [**IMarshal:: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)del contador de referencias estándar. El serializador estándar llama a [**IStdMarshalInfo:: GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) para obtener el CLSID del controlador que se va a crear. Después de que el serializador estándar haya realizado su serialización, el servidor escribe sus propios datos adicionales en la secuencia. Las estructuras resultantes, con datos adicionales en la secuencia, se muestran en la siguiente ilustración:

![Diagrama que muestra las estructuras con datos adicionales en la secuencia.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side estructuras con datos adicionales en el flujo

Esto permite que la llamada desde COM a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) en el cliente tenga la capacidad de omitir los datos no leídos y dejar la secuencia en la posición adecuada después de todos los datos de interfaz de cálculo de referencias si el controlador no se puede crear.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side estructuras con datos adicionales en el flujo

Como en el caso en el que no hay datos de servidor adicionales en la secuencia, la llamada COM del lado cliente a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) creará la identidad y el controlador. El controlador debe implementar [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) y debe delegar primero las llamadas a **IMarshal** al serializador estándar agregado y, a continuación, calcular las referencias de los datos adicionales que el servidor proporcionó o anular su serialización. Se llamará a [**unmarshalinterface (**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) del controlador para cada no serialización, independientemente de si ha quitado las referencias de la interfaz antes o no. En este caso, el servidor no llama a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) , pero el controlador debe. La estructura del lado cliente resultante se muestra en la siguiente ilustración.

![Diagrama que muestra la estructura del lado cliente.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 