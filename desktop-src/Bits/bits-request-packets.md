---
title: Paquetes de solicitud de BITS
description: Paquetes de solicitud de BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993977"
---
# <a name="bits-request-packets"></a>Paquetes de solicitud de BITS

Los paquetes de solicitud describen las solicitudes del cliente. Solo puede haber una solicitud pendiente en un momento dado; debe recibir una [confirmación](bits-response-packets.md) para la solicitud actual del servidor antes de enviar otra solicitud.

En la tabla siguiente se enumeran los paquetes de solicitud enviados al servidor BITS para los trabajos de carga y de carga y respuesta. En la tabla se enumeran los paquetes en la secuencia típica que se envían al servidor.



| Paquete de solicitud                       | Propósito                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Establece una conexión y negocia la seguridad con el servidor.                                                                                              |
| [Crear sesión](create-session.md) | Solicita una sesión de carga con el servidor BITS.                                                                                                               |
| [Fragmento](fragment.md)             | Envía un fragmento del archivo al servidor BITS. El número de solicitudes de fragmentos enviadas depende del tamaño de fragmento que elija y del tamaño del archivo de carga. |
| [Sesión de cierre](close-session.md)   | Finaliza la sesión de carga de archivos con el servidor BITS.                                                                                                             |
| [Cancelar sesión](cancel-session.md) | Finaliza la sesión de carga de archivos con el servidor BITS. Normalmente, se envía el paquete de Cancel-Session si el usuario canceló el trabajo.                                 |



 

El paquete Ping es opcional. En lugar de enviar un paquete ping, puede usar el paquete de Create-Session para establecer una conexión y negociar la seguridad. Sin embargo, es más eficaz usar el paquete ping con este fin.

 

 




