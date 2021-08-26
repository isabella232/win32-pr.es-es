---
description: El sistema difunde un mensaje a todas las aplicaciones y controladores instalables cada vez que se produce un evento de administración de energía.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7997f6c9bed6b4d46068c9974f4ff3571a9617ba2bf09adc6b98bb33facb3d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032695"
---
# <a name="wm_powerbroadcast-messages"></a>Mensajes \_ DE WM POWERBROADCAST

El sistema difunde un mensaje a todas las aplicaciones y controladores instalables cada vez que se produce un evento de administración de energía. El sistema difunde estos eventos a través del [**mensaje \_ WM POWERBROADCAST,**](wm-powerbroadcast.md) estableciendo el *parámetro wParam* en el evento de administración de energía adecuado. Por ejemplo, el [evento \_ PBT APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica un cambio de estado de energía del sistema. Debe asegurarse de que la aplicación responde correctamente al **mensaje \_ WM POWERBROADCAST.**

El sistema difunde un evento [ \_ PBT APMSUSPEND](pbt-apmsuspend.md) inmediatamente antes de suspender la operación. Esto ofrece a las aplicaciones y los controladores una última oportunidad de prepararse para el evento. En muchos casos, el sistema difunde estos mensajes sin solicitar permiso para hacerlo. Esto sucede, por ejemplo, si una aplicación fuerza la suspensión con la [**función SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

El sistema difunde el evento [ \_ PBT APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) cuando se ha restaurado la operación del sistema. Si una aplicación recibió un evento [ \_ PBT APMSUSPEND](pbt-apmsuspend.md) antes de suspender el equipo, recibirá el evento \_ PBT APMRESUMESUSPEND. De lo contrario, recibirá el evento \_ PBT APMRESUMECRITICAL.

El sistema envía un [evento \_ PBT POWERSETTINGCHANGE](pbt-powersettingchange.md) a las aplicaciones que se han registrado para el evento específico [**mediante RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification). Para obtener más información, [vea Registering for Power Events](registering-for-power-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



