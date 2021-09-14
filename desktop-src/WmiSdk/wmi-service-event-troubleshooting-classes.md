---
description: Los eventos del servicio WMI generan clases de solución de problemas de eventos del servicio WMI, como la creación del grupo de subprocesos.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Clases de solución de problemas de eventos del servicio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e811ac5b276e5562f73b5b432d5f3255af5bab7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966995"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Clases de solución de problemas de eventos del servicio WMI

Los eventos del servicio WMI generan clases de solución de problemas de eventos del servicio WMI, como la creación del grupo de subprocesos.

Puede suscribirse a las notificaciones de [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) de clase base abstracta para obtener todos los eventos derivados enumerados en la tabla siguiente.



|   Evento                                                                                        |   Descripción                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Clase primaria para todos Windows eventos propios del subsistema de eventos (ESS) de Instrumental de administración de administración de eventos (WMI). |
| [**\_WMITRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Representa la creación de un receptor de eventos para la notificación de una consulta de eventos.                       |
| [**\_WMITCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | se genera cuando se cancela un receptor de eventos.                                                           |
| [**WMIT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | proporciona la notificación de eventos de subproceso en el subs sistema de eventos WMI (ESS).                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Proporciona una notificación cuando se crea un subproceso en el subs sistema de eventos WMI (ESS).                   |
| [**WMIT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Proporciona una notificación cuando se elimina un subproceso en el subs sistema de eventos WMI (ESS).                   |
| [**WMIFILTEREvent de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Clase primaria para todos los eventos de filtro de consumidor de eventos permanentes.                                        |
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

[Recepción de un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
