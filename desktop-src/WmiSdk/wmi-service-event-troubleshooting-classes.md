---
description: Los eventos del servicio WMI generan clases de solución de problemas de eventos del servicio WMI, como la creación de grupos de subprocesos.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Clases de solución de problemas de eventos del servicio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3728b6ae150a948fdf71515e27f17ca7280f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278970"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Clases de solución de problemas de eventos del servicio WMI

Los eventos del servicio WMI generan clases de solución de problemas de eventos del servicio WMI, como la creación de grupos de subprocesos.

Puede suscribirse a las notificaciones de la clase base abstracta [**msft \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) para obtener todos los eventos derivados que se enumeran en la tabla siguiente.



|                                                                                           |                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Clase primaria para todos los eventos propios de subsistema de eventos (ESS) de Instrumental de administración de Windows (WMI). |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Representa la creación de un receptor de eventos para la notificación de una consulta de evento.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | se genera cuando se cancela un receptor de eventos.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | proporciona la notificación de eventos de subproceso en el subsistema de eventos WMI (ESS).                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Proporciona una notificación cuando se crea un subproceso en el subsistema de eventos WMI (ESS).                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Proporciona una notificación cuando se elimina un subproceso en el subsistema de eventos WMI (ESS).                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Clase primaria para todos los eventos de filtro de consumidor de eventos permanentes.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Define la activación correcta de un filtro de suscripción de consumidor de eventos permanente.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Define la desactivación correcta de un filtro de suscripción de consumidor permanente.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

Solución de problemas de WMI
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Recibir un evento de WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
