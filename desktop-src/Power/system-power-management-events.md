---
description: Un evento de administración de energía del sistema es un cambio en el estado de energía del sistema, el modo operativo de un dispositivo o el sistema, o el valor de una configuración de energía.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Eventos de administración de energía del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0558dfe0c846c6b48125a382d14f03181d7f18fb2d11deb4783af975e57c4cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032935"
---
# <a name="system-power-management-events"></a>Eventos de administración de energía del sistema

Un evento de administración de energía del sistema es un cambio en el estado de energía del sistema, el modo operativo de un dispositivo o el sistema, o el valor de una configuración de energía. Dado que estos eventos pueden afectar al funcionamiento de las aplicaciones y los controladores instalables, el sistema notifica a todas las aplicaciones y controladores instalables mediante la difusión de una notificación para cada evento. Las aplicaciones y los servicios se registran para recibir notificaciones mediante [**la función RegisterPowerSettingNotification.**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) Las notificaciones se reciben a través del [**mensaje \_ WM POWERBROADCAST,**](wm-powerbroadcast.md) que contiene el evento de administración de energía y los datos específicos del evento asociados.

## <a name="system-power-status-events"></a>Eventos de estado de energía del sistema

Un *evento de estado de energía del* sistema se produce cuando hay un cambio en la fuente de alimentación o en el estado de la batería del sistema. Por ejemplo, el sistema difunde un evento [ \_ PBT APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) cada vez que el usuario cambia de batería a alimentación de CA o viceversa. El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.

## <a name="operational-mode-events"></a>Eventos en modo operativo

Un *evento de* modo operativo se produce cuando se produce un cambio en el consumo de energía, como el cambio del sistema a un estado de suspensión debido a la inactividad o cuando el usuario pone manualmente el sistema en modo de suspensión. El sistema difunde eventos sobre estos cambios antes de que se realice el cambio en el consumo de energía. Por ejemplo, si el sistema determina que está inactivo, difunde un evento [ \_ APMSUSPEND](pbt-apmsuspend.md) de PBT que notifica a las aplicaciones y los controladores que está a punto de suspender la operación y suspender para ahorrar energía. Las aplicaciones y los controladores pueden prepararse para la suspensión cerrando archivos y guardando datos para evitar la posible pérdida de datos.

Cuando el sistema lleva a cabo una *suspensión crítica,* el sistema se pone inmediatamente en suspensión debido a una condición crítica, como una alarma de batería crítica. A diferencia de una transición de suspensión normal, el sistema no notifica a las aplicaciones y los controladores antes de llevar a cabo una suspensión crítica. Por lo tanto, las aplicaciones deben estar preparadas para controlar las suspensiones críticas.

Cuando se restaura la operación del sistema después de haber sido suspendida, el sistema notifica a todas las aplicaciones y controladores. También indica si el sistema se está reanudando desde una suspensión crítica para que la aplicación o el controlador puedan realizar los pasos adecuados para restaurar sus datos y continuar el funcionamiento.

Las aplicaciones deben realizar todos los intentos de controlar la transición al estado de suspensión sin intervención del usuario, ya que es posible que no sea posible que el usuario responda. Por ejemplo, se puede cerrar la tapa del equipo del cuaderno. Cuando una aplicación recibe una notificación de que el sistema está a punto de entrar en suspensión, debe realizar las operaciones necesarias rápidamente y devolver fuera del bucle de mensajes. El sistema permite un máximo de dos segundos por aplicación al controlar este mensaje antes de que se alcance el tiempo de salida.

## <a name="power-setting-change-events"></a>Eventos de cambio de configuración de energía

Un evento de cambio de configuración de energía se produce cuando hay un cambio en el valor de una configuración de energía. Por ejemplo, el usuario cambia el plan de energía de Alto rendimiento a Equilibrado en Opciones de energía aplicación en Panel de control. En este caso, el sistema difundiría un evento que indica que el plan de energía ha cambiado. Este evento incluye el nuevo valor para la configuración de energía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



