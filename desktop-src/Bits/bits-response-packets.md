---
title: Paquetes de respuesta de BITS
description: Paquetes de respuesta de BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903144"
---
# <a name="bits-response-packets"></a>Paquetes de respuesta de BITS

En la tabla siguiente se enumeran los paquetes de respuesta enviados al cliente de BITS para los trabajos de carga y de carga y respuesta. En la tabla se enumeran los paquetes en la secuencia típica que se envían al cliente.



| Paquete de respuesta                                      | Propósito                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Confirmación del ping](ack-for-ping.md)                     | Confirma la solicitud de [ping](ping.md) .                                                                                                                                                  |
| [Confirmación de creación: sesión](ack-for-create-session.md) | Confirma la solicitud [de creación de sesión](create-session.md) y devuelve un identificador de sesión que el cliente de bits usa en todas las solicitudes posteriores para identificar esta sesión de transferencia de archivos. |
| [Confirmación para fragmento](ack-for-fragment.md)             | Confirma la solicitud de [fragmento](fragment.md) y escribe el fragmento en el archivo de carga en el servidor.                                                                                 |
| [Confirmación de cierre de sesión](ack-for-close-session.md)   | Confirma la solicitud [de cierre de sesión](close-session.md) y libera todos los recursos asociados a la sesión.                                                                         |
| [Confirmación para cancelar sesión](ack-for-cancel-session.md) | Confirma la solicitud [de cancelación de sesión](cancel-session.md) y libera todos los recursos asociados a la sesión.                                                                       |



 

 

 




