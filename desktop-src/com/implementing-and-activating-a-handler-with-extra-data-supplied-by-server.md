---
title: Implementar y activar un controlador con datos adicionales proporcionados por el servidor
description: Implementar y activar un controlador con datos adicionales proporcionados por el servidor
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4777c44dd9983a0193872507272862766c51e708f5caa491a6f8d787923749c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029943"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementar y activar un controlador con datos adicionales proporcionados por el servidor

Si el servidor desea incluir algunos datos adicionales en el paquete para que lo use el controlador, el servidor debe implementar las interfaces [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) e [**IStdMarshalInfo.**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) El servidor debe agregar el serializador estándar y debe delegar la primera parte de la serialización en el serializador estándar agregado, incluido [**IMarshal::GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), y debe agregar su propio tamaño de datos al tamaño devuelto por [**IMarshal::GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)del serializador estándar. El serializador estándar llama [**a IStdMarshalInfo::GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) para obtener el CLSID del controlador que se va a crear. Una vez que el serializador estándar ha realizado su serialización, el servidor escribe sus propios datos adicionales en la secuencia. Las estructuras resultantes, con datos adicionales en la secuencia, se muestran en la ilustración siguiente:

![Diagrama que muestra estructuras con datos adicionales en la secuencia.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side estructuras con datos adicionales en stream

Esto permite que la llamada de COM a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) en el lado cliente pueda omitir los datos no leídos y dejar la secuencia en la posición adecuada después de todos los datos de la interfaz serializada si no se puede crear el controlador.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side estructuras con datos adicionales en stream

Como en el caso de que no haya datos de servidor adicionales en la secuencia, la llamada COM del lado cliente a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) creará la identidad y el controlador. El controlador debe implementar [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) y debe delegar primero las llamadas **IMarshal** al serializador estándar agregado y, a continuación, serializar o desmarshal los datos adicionales proporcionados por el servidor. Se llamará [**a UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) del controlador para cada unmarshal, independientemente de si ha desmarshalado la interfaz antes o no. En este caso, el servidor no llama [**a CoGetStdMarshalEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) pero el controlador debe hacerlo. La estructura del lado cliente resultante se muestra en la ilustración siguiente.

![Diagrama que muestra la estructura del lado cliente.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 