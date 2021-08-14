---
title: Comportamiento del grupo de sistemas
description: Explicación sobre las acciones realizadas por el grupo de sistemas cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923cfff4b36bd14d100ce1f73db455be5261d75dc2c5be1eddc8f9d6af87fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911598"
---
# <a name="system-pool-behavior"></a>Comportamiento del grupo de sistemas

En la siguiente explicación se resaltan las acciones realizadas por el grupo de sistemas cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.

## <a name="event-dispatching"></a>Distribución de eventos

Cuando una unidad biométrica genera un aviso de evento, el grupo de sistemas usa un filtro en cascada para enviar el aviso y asignarle uno de los siguientes niveles de prioridad:

-   La prioridad alta se asigna a las solicitudes explícitas de coincidencia e inscripción generadas por los clientes.
-   La prioridad media se asigna a eventos de inscripción o coincidencia inesperados o no reclamados.
-   La prioridad baja se asigna a los eventos de navegación.

Los eventos de captura se entregan en la secuencia siguiente:

-   Si la ventana de foco actual está esperando una operación de coincidencia o de inscripción, el ejemplo se procesa y se envía al cliente que posee la ventana de foco actual.
-   Si la ventana de foco actual no reclama el evento de captura y se ha registrado un controlador de eventos no reclamado con el servicio biométrico de Windows, el evento de captura se envía a este controlador.
-   Si el evento permanece sin reclamación, se descarta.

Si el evento es un evento de navegación y se ha registrado un controlador de eventos de navegación con Windows Biometric Service, el evento de captura se envía a este controlador. Si no hay ningún controlador de eventos, se descarta el evento.

## <a name="idle-mode"></a>Modo inactivo

Cuando no hay ningún cliente esperando a que se completen las solicitudes de inscripción o coincidencia explícitas, el grupo del sistema determina si se generan automáticamente solicitudes de captura repetidas y se envía el aviso de evento resultante al controlador de eventos no reclamados o se esperan eventos de navegación y se envían al controlador de eventos de navegación.

Si se ha registrado un controlador de eventos no reclamado con Windows Biometric Service, el grupo de sistemas realiza las siguientes acciones:

-   El modo de navegación del sensor está deshabilitado.
-   Las operaciones no reclamadas se envían al controlador de eventos independientemente del foco de ventana.
-   Si no hay solicitudes pendientes para una operación biométrica, se realiza una captura automática.

Si se ha registrado un controlador de navegación con Windows Biometric Service, el grupo de sistemas hace lo siguiente:

-   Las unidades biométricas del grupo del sistema se colocan en un estado de navegación si no hay ninguna operación biométrica pendiente.
-   Los eventos de navegación se deshabilitan si un cliente envía un aviso de evento de coincidencia o inscripción.
-   Si se ha registrado un controlador de eventos no reclamados, los eventos de navegación se deshabilitan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grupo de sensores privados](private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Grupo de sensores del sistema](system-sensor-pool.md)
</dt> </dl>

 

 




