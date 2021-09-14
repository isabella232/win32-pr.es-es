---
title: Controlador de Client-Side ligero
description: Los controladores ligeros del lado cliente permiten crear controladores generales del lado cliente de cualquier tamaño para ayudarle a realizar cualquier tipo de tarea estándar.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253101"
---
# <a name="the-lightweight-client-side-handler"></a>Controlador de Client-Side ligero

Los controladores ligeros del lado cliente permiten crear controladores generales del lado cliente de cualquier tamaño para ayudarle a realizar cualquier tipo de tarea estándar. Como controladores, son utilizables por más de un cliente. Difieren de los controladores OLE en que no se pueden crear antes de iniciar el servidor y su duración está vinculada a la del administrador de proxy, lo que impide una posible condición de carrera en la que el controlador podría liberarse prematuramente.

El administrador de proxy es el objeto creado por el sistema que implementa la [**interfaz IMarshal.**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Si usa la serialización estándar, el sistema la crea automáticamente al llamar a [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (o [**CoGetStdMarshalEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)para crear un serializador agregado para controladores ligeros) y también implementa las interfaces [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) en el objeto . En el lado servidor, hay un objeto del sistema correspondiente que también implementa **IMarshal**. Estos objetos controlan la serialización de forma transparente.

Hay dos tipos generales de estos controladores que puede que desee implementar:

-   Un controlador que realiza un servicio que no requiere datos adicionales del servidor
-   Controlador que usa datos adicionales del servidor

Algunos posibles usos de los datos adicionales en la secuencia proporcionada por el servidor son los siguientes:

-   Datos estáticos del servidor. Independientemente de la interfaz concreta que se esté serializando, el servidor escribe los mismos datos en la secuencia.
-   Datos por interfaz del servidor. Dependiendo de la interfaz concreta que se esté serializando, el servidor puede escribir datos diferentes en la secuencia.
-   Asistentes por interfaz. Componentes COM por interfaz agregados en el controlador de cliente y delegando al proxy estándar. Por ejemplo, para mejorar el rendimiento de la red, un componente COM para [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) podría realizar el almacenamiento en caché del lado cliente de datos, lectura adelantada, escritura detrás, bloqueo de operaciones, etc.
-   Versión de red de una interfaz. La versión de red de la interfaz es diferente de la interfaz expuesta por el código de aplicación de cliente y servidor. Es posible, por ejemplo, multiplexar interfaces expuestas IA e IB a través de la misma interfaz de red INetAB, de la manera en que lo hace el controlador del servidor de inserción. Por ejemplo, se podría convertir una interfaz de transferencia de datos en una interfaz de red que use canalizaciones para una transferencia de datos eficaz.

Es posible que los clientes de nivel inferior no tengan la capacidad de desmarque de interfaces que tienen controladores personalizados, por dos motivos: en primer lugar, es posible que no comprendan el CLSID usado en el paquete serializado personalizado cuando se agrega el controlador del servidor y el objeto quiere un controlador. En segundo lugar, es posible que el código de controlador ni siquiera se ejecute en el lado cliente si requiere una nueva funcionalidad de COM para crear el serializador estándar agregado y realizar llamadas [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El controlador OLE](the-ole-handler.md)
</dt> </dl>

 

 