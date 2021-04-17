---
description: Un evento de administración de energía del sistema es un cambio en el estado de la alimentación del sistema, el modo operativo de un dispositivo o el sistema o el valor de una configuración de energía.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Eventos de administración de energía del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab18fad9116cfff9e1cd35703e32a49e3b12c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667195"
---
# <a name="system-power-management-events"></a>Eventos de administración de energía del sistema

Un evento de administración de energía del sistema es un cambio en el estado de la alimentación del sistema, el modo operativo de un dispositivo o el sistema o el valor de una configuración de energía. Dado que estos eventos pueden afectar al funcionamiento de las aplicaciones y los controladores instalables, el sistema notifica a todas las aplicaciones y controladores instalables mediante la difusión de una notificación para cada evento. Las aplicaciones y los servicios se registran para las notificaciones mediante la función [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Las notificaciones se reciben a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) , que contiene el evento de administración de energía y los datos específicos del evento asociados.

## <a name="system-power-status-events"></a>Eventos de estado de alimentación del sistema

Un *evento de estado de energía del sistema* se produce cuando hay un cambio en la fuente de alimentación o en el estado de la batería del sistema. Por ejemplo, el sistema difunde un evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) cada vez que el usuario cambia de la batería a la corriente alterna, o viceversa. El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.

## <a name="operational-mode-events"></a>Eventos de modo operativo

Un *evento de modo operativo* se produce cuando hay un cambio en el consumo de energía, como el cambio del sistema a un estado de suspensión debido a la inactividad o al usuario que coloca el sistema de forma manual en modo de suspensión. El sistema difunde eventos sobre estos cambios antes de que se realice el cambio de consumo de energía. Por ejemplo, si el sistema determina que está inactivo, difunde un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) que notifica a las aplicaciones y los controladores que está a punto de suspender la operación y la suspensión para ahorrar energía. Las aplicaciones y los controladores se pueden preparar para la suspensión cerrando los archivos y guardando los datos para evitar la posible pérdida de datos.

Cuando el sistema realiza una *suspensión crítica*, el sistema se pone inmediatamente en suspensión debido a una condición crítica, como una alarma de batería crítica. A diferencia de una transición de suspensión normal, el sistema no notifica a las aplicaciones y controladores antes de llevar a cabo una suspensión crítica. Por lo tanto, las aplicaciones deben estar preparadas para controlar las suspensiones críticas.

Cuando se restaura la operación del sistema después de haber sido suspendida, el sistema notifica a todas las aplicaciones y controladores. También indica si el sistema se está reanudando a partir de una suspensión crítica, por lo que la aplicación o el controlador pueden tomar los pasos adecuados para restaurar los datos y continuar con la operación.

Las aplicaciones deben realizar cada intento de controlar la transición al estado de suspensión sin intervención del usuario, ya que es posible que el usuario no pueda responder. Por ejemplo, la tapa del equipo portátil puede estar cerrada. Cuando una aplicación recibe una notificación de que el sistema está a punto de entrar en modo de suspensión, debe realizar las operaciones necesarias rápidamente y devolver el bucle de mensajes. El sistema permite un máximo de dos segundos por aplicación al controlar este mensaje antes de que se agote el tiempo de espera.

## <a name="power-setting-change-events"></a>Eventos de cambio de configuración de energía

Un evento de cambio de configuración de energía se produce cuando hay un cambio en el valor de una configuración de energía. Por ejemplo, el usuario cambia el plan de energía de alto rendimiento a equilibrado en la aplicación opciones de energía del panel de control. En este caso, el sistema difundiría un evento que indica que el plan de energía ha cambiado. Este evento incluye el nuevo valor de la configuración de energía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



