---
title: Paquetes de solicitud bits
description: Paquetes de solicitud bits
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60921c9adb8e1312a6b74cd129e591db5a3be7807394807b984eb3fff153b3a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588685"
---
# <a name="bits-request-packets"></a>Paquetes de solicitud bits

Los paquetes de solicitud describen las solicitudes de cliente. Solo puede haber una solicitud pendiente en un momento dado; debe recibir una [confirmación para](bits-response-packets.md) la solicitud actual del servidor antes de enviar otra solicitud.

En la tabla siguiente se enumeran los paquetes de solicitud enviados al servidor BITS para los trabajos de carga y respuesta. En la tabla se enumeran los paquetes de la secuencia típica que se envían al servidor.



| Paquete de solicitud                       | Propósito                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Establece una conexión y negocia la seguridad con el servidor.                                                                                              |
| [Create-Session](create-session.md) | Solicita una sesión de carga con el servidor BITS.                                                                                                               |
| [Fragmento](fragment.md)             | Envía un fragmento del archivo al servidor BITS. El número de solicitudes de fragmento enviadas depende del tamaño del fragmento que elija y del tamaño del archivo de carga. |
| [Cerrar sesión](close-session.md)   | Finaliza la sesión de carga de archivos con el servidor BITS.                                                                                                             |
| [Cancelar sesión](cancel-session.md) | Finaliza la sesión de carga de archivos con el servidor BITS. Normalmente, se envía el Cancel-Session paquete si el usuario canceló el trabajo.                                 |



 

El paquete Ping es opcional. En lugar de enviar un paquete Ping, puede usar el paquete Create-Session para establecer una conexión y negociar la seguridad. Sin embargo, es más eficaz usar el paquete Ping para este propósito.

 

 




