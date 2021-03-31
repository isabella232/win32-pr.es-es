---
title: Comportamiento del grupo de sistemas
description: Debate sobre las acciones realizadas por el grupo del sistema cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a82d957b2b1b4968835eec1482662e30765e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418759"
---
# <a name="system-pool-behavior"></a>Comportamiento del grupo de sistemas

En la siguiente explicación se resaltan las acciones realizadas por el grupo del sistema cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.

## <a name="event-dispatching"></a>Envío de eventos

Cuando una unidad biométrica genera un aviso de eventos, el grupo de sistema usa un filtro en cascada para enviar el aviso y asignarle uno de los siguientes niveles de prioridad:

-   La prioridad alta se asigna a las solicitudes de coincidencia explícita e inscripción generadas por los clientes.
-   La prioridad media se asigna a los eventos de inscripción o de coincidencia inesperados o no notificados.
-   La prioridad baja se asigna a los eventos de navegación.

Los eventos de captura se entregan en la secuencia siguiente:

-   Si la ventana de foco actual está esperando una operación de inscripción o de coincidencia, el ejemplo se procesa y se envía al cliente que posee la ventana de foco actual.
-   Si el evento de captura no es reclamado por la ventana de foco actual y se ha registrado un controlador de eventos no reclamado con el servicio biométrico de Windows, el evento de captura se envía a este controlador.
-   Si el evento sigue sin ser reclamado, se descarta.

Si el evento es un evento de navegación y se ha registrado un controlador de eventos de navegación con el servicio biométrico de Windows, el evento de captura se envía a este controlador. Si no hay ningún controlador de eventos, el evento se descarta.

## <a name="idle-mode"></a>Modo inactivo

Cuando no hay clientes a la espera de que se completen las solicitudes explícitas de inscripción o de inscripción, el grupo de sistema determina si se generan automáticamente solicitudes de captura repetidas y se envía el aviso de eventos resultante al controlador de eventos no reclamado o se espera a los eventos de navegación y se envían al controlador de eventos de navegación.

Si se ha registrado un controlador de eventos no reclamado con el servicio biométrico de Windows, el grupo de sistema realiza las siguientes acciones:

-   El modo de navegación para el sensor está deshabilitado.
-   Las operaciones no reclamadas se envían al controlador de eventos independientemente del foco de la ventana.
-   Si no hay solicitudes pendientes para una operación biométrica, se realiza una captura automática.

Si se ha registrado un controlador de navegación con el servicio biométrico de Windows, el grupo de sistema hace lo siguiente:

-   Las unidades biométricas del grupo de sistema se colocan en un estado de navegación si no hay ninguna operación biométrica pendiente.
-   Los eventos de navegación se deshabilitan si un cliente envía una notificación de evento de coincidencia o inscripción.
-   Si se ha registrado un controlador de eventos no reclamado, los eventos de navegación están deshabilitados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grupo de sensores privados](private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Grupo de sensores del sistema](system-sensor-pool.md)
</dt> </dl>

 

 




