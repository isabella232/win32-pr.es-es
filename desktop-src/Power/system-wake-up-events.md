---
description: La aplicación puede restaurar un equipo que se encuentra en estado de suspensión al estado de funcionamiento mediante un temporizador programado o un evento de dispositivo.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Eventos de reactivación del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f363820425f143b9a669008ce45df7e7d014817
ms.sourcegitcommit: 5c2f3d7242e53805cc45deb2b251aaa64750ea46
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "129584569"
---
# <a name="system-wake-up-events"></a>Eventos de reactivación del sistema

La siguiente información se aplica a las reactivaciones de suspensión [(S3) e hibernación (S4).](/windows-hardware/drivers/kernel/system-sleeping-states) Para las reactivaciones del modo de espera moderno (S0 low power idle), consulte transición entre [los estados inactivo y activo](/windows-hardware/design/device-experiences/transitioning-between-idle-and-active-states).

La aplicación puede restaurar un equipo que se encuentra en estado de suspensión al estado de funcionamiento mediante un temporizador programado o un evento de dispositivo. Esto se conoce como evento *de reactivación.* Use un [objeto de temporizador que se](/windows/desktop/Sync/waitable-timer-objects) puede esperar para especificar la hora a la que se debe reactivar el sistema. Para crear el objeto, use la [**función CreateWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Para establecer el temporizador, use la [**función SetWaitableTimer.**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) El *parámetro pDueTime* especifica cuándo se señalará el temporizador. Para especificar que el sistema debe activarse cuando se señale el temporizador, establezca el *parámetro fResume* en **TRUE.**

Cuando el sistema se activa automáticamente debido a un evento (que no sea el conmutador de alimentación o la actividad del usuario), el sistema establece automáticamente un temporizador de inactividad desatendido en al menos 2 minutos. Este temporizador proporciona a las aplicaciones tiempo suficiente para llamar a la [**función SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que están ocupadas. Este tiempo permite que el sistema vuelva al estado de suspensión rápidamente después de que el equipo ya no sea necesario. Los criterios siguientes determinan si el sistema vuelve al estado de suspensión:

-   Si el sistema se activa automáticamente (es decir, no hay ninguna actividad del usuario), se apaga en cuanto expira el temporizador de inactividad desatendido, suponiendo que ninguna aplicación haya llamado a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que el sistema es necesario.
-   Las reactivaciones basadas en dispositivos desencadenan el temporizador de inactividad desatendido de forma predeterminada, a menos que el controlador del dispositivo indique la presencia del usuario. Si el controlador indica la presencia del usuario, se usa el temporizador de inactividad del sistema.
-   Si el sistema se activa automáticamente, pero el usuario proporciona una nueva entrada mientras se controla el evento, el sistema no vuelve automáticamente a la suspensión en función del temporizador de inactividad desatendido. En su lugar, el sistema vuelve a suspensión en función del temporizador de inactividad del sistema.
-   Si el sistema se reactiva debido a la actividad del usuario, el sistema no vuelve automáticamente a suspensión en función del temporizador de inactividad desatendido. En su lugar, el sistema vuelve a suspensión en función del temporizador de inactividad del sistema.

Cuando el sistema se activa automáticamente, difunde el evento [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) a todas las aplicaciones. Dado que el usuario no está presente, la mayoría de las aplicaciones no deben hacer nada. Las aplicaciones de control de eventos, como los servidores de fax, deben controlar sus eventos. Para determinar si el sistema está en este estado, llame a la [**función IsSystemResumeAutomatic.**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) Cuando el sistema se activa automáticamente, la pantalla no se activa automáticamente.

Si el sistema se reactiva debido a la actividad del usuario, el sistema difundirá primero el evento [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) seguido de un evento [ \_ PBT APMRESUMESUSPEND.](pbt-apmresumesuspend.md) Además, el sistema activará la pantalla. La aplicación debe volver a abrir los archivos que cerró cuando el sistema entró en suspensión y prepararse para la entrada del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Criterios de suspensión del sistema](system-sleep-criteria.md)
</dt> </dl>

 

 
