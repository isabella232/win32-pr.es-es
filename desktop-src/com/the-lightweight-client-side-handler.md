---
title: Controlador de Client-Side ligero
description: Los controladores de cliente ligeros le permiten crear controladores del lado cliente generales de cualquier tamaño, para ayudarle a realizar cualquier tipo de tarea estándar.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794055"
---
# <a name="the-lightweight-client-side-handler"></a>Controlador de Client-Side ligero

Los controladores de cliente ligeros le permiten crear controladores del lado cliente generales de cualquier tamaño, para ayudarle a realizar cualquier tipo de tarea estándar. Como controladores, se pueden usar en más de un cliente. Se diferencian de los controladores OLE en que no se pueden crear antes de que se inicie el servidor, y su duración está ligada a la del administrador de proxy, lo que impide una posible condición de carrera en la que el controlador podría ser liberado prematuramente.

El administrador proxy es el objeto creado por el sistema que implementa la interfaz [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) . Si usa el cálculo de referencias estándar, el sistema lo crea automáticamente al llamar a [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (o [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), para crear un contador de referencias agregado para controladores ligeros) y también implementa las interfaces [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) en el objeto. En el lado del servidor, hay un objeto del sistema correspondiente que también implementa **IMarshal**. Estos objetos controlan el cálculo de referencias de forma transparente.

Hay dos tipos generales de estos controladores que puede desear implementar:

-   Un controlador que realiza un servicio que no requiere datos adicionales del servidor.
-   Un controlador que utiliza datos adicionales del servidor

Algunos de los usos posibles de los datos adicionales en la secuencia proporcionada por el servidor son los siguientes:

-   Datos estáticos del servidor. Independientemente de la interfaz concreta en la que se calculan las referencias, el servidor escribe los mismos datos en la secuencia.
-   Datos por interfaz del servidor. Dependiendo de la interfaz concreta en la que se calculan las referencias, el servidor puede escribir datos diferentes en la secuencia.
-   Aplicaciones auxiliares por interfaz. Componentes COM por interfaz agregados al controlador de cliente y delegando en el proxy estándar. Por ejemplo, para mejorar el rendimiento de la red, un componente COM de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) podría hacer el almacenamiento en caché del lado cliente de los datos, la lectura previa, la escritura retrasada, el bloqueo de operaciones, etc.
-   Versión de red de una interfaz. La versión de red de la interfaz es diferente de la interfaz expuesta por el código de aplicación de cliente y servidor. Por ejemplo, es posible multiplexar las interfaces expuestas IA y IB sobre la misma interfaz de red INetAB, el modo en que lo hace el controlador de servidor de inserción. Por ejemplo, puede convertir una interfaz de transferencia de datos en una interfaz de red que utiliza canalizaciones para una transferencia de datos eficaz.

Es posible que los clientes de nivel inferior no dispongan de la capacidad de calcular las referencias de las interfaces que tienen controladores personalizados, por dos motivos: en primer lugar, es posible que no conozcan el CLSID utilizado en el paquete de cálculo de referencias personalizado cuando se agrega el controlador de servidor y el objeto desea un controlador. En segundo lugar, es posible que el código del controlador no se ejecute incluso en el lado cliente si requiere una nueva funcionalidad de COM para crear el serializador estándar agregado y para realizar llamadas [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El controlador OLE](the-ole-handler.md)
</dt> </dl>

 

 