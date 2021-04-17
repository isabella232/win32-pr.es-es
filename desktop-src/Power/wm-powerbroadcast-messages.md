---
description: El sistema difunde un mensaje a todas las aplicaciones y controladores instalables siempre que se produzca un evento de administración de energía.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Mensajes de WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677877"
---
# <a name="wm_powerbroadcast-messages"></a>\_Mensajes POWERBROADCAST de WM

El sistema difunde un mensaje a todas las aplicaciones y controladores instalables siempre que se produzca un evento de administración de energía. El sistema difunde estos eventos a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) , estableciendo el parámetro *wParam* en el evento de administración de energía adecuado. Por ejemplo, el evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica un cambio de estado de energía del sistema. Debe asegurarse de que la aplicación responde correctamente al mensaje de **\_ POWERBROADCAST de WM** .

El sistema difunde un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) inmediatamente antes de suspender la operación. Esto proporciona a las aplicaciones y controladores una última oportunidad para prepararse para el evento. En muchos casos, el sistema difunde estos mensajes sin solicitar permiso para hacerlo. Esto sucede, por ejemplo, si una aplicación fuerza la suspensión con la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

El sistema difunde el evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) cuando se ha restaurado la operación del sistema. Si una aplicación ha recibido un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de que se suspendiera el equipo, recibirá el \_ evento PBT APMRESUMESUSPEND. De lo contrario, recibirá el \_ evento PBT APMRESUMECRITICAL.

El sistema envía un evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) a las aplicaciones que se han registrado para el evento específico mediante [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Para obtener más información, consulte [registro de eventos de energía](registering-for-power-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



