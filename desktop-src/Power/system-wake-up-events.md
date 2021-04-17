---
description: La aplicación puede restaurar un equipo que está en estado de suspensión con el estado de funcionamiento mediante un temporizador programado o un evento de dispositivo.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Eventos de reactivación del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677885"
---
# <a name="system-wake-up-events"></a>Eventos de reactivación del sistema

La siguiente información se aplica a las reactivaciones desde [suspensión (S3) e hibernación (S4)](/windows-hardware/drivers/kernel/system-sleeping-states). En el caso de las reactivaciones desde el estado de espera moderno (S0 de baja energía inactiva), consulte las [transiciones de inactividad a activa](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

La aplicación puede restaurar un equipo que está en estado de suspensión con el estado de funcionamiento mediante un temporizador programado o un evento de dispositivo. Esto se conoce como un *evento de reactivación*. Use un [objeto de temporizador](/windows/desktop/Sync/waitable-timer-objects) que se pueda esperar para especificar la hora a la que se debe reactivar el sistema. Para crear el objeto, use la función [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Para establecer el temporizador, utilice la función [**SetWaitableTimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) . El parámetro *pDueTime* especifica cuándo se señalará el temporizador. Para especificar que el sistema se debe reactivar cuando se señala el temporizador, establezca el parámetro *fResume* en **true**.

Cuando el sistema se reactiva automáticamente debido a un evento (distinto del interruptor de alimentación o la actividad de usuario), el sistema establece automáticamente un temporizador de inactividad desatendido en 2 minutos como mínimo. Este temporizador proporciona a las aplicaciones el tiempo suficiente para llamar a la función [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que están ocupados. Esta vez permite que el sistema vuelva al estado de suspensión rápidamente después de que el equipo deje de ser necesario. Los criterios siguientes determinan si el sistema vuelve al estado de suspensión:

-   Si el sistema se reactiva automáticamente (es decir, no hay ninguna actividad de usuario), se cierra en cuanto expira el temporizador de inactividad desatendido, suponiendo que ninguna aplicación ha llamado a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para indicar que el sistema es obligatorio.
-   Las reactivaciones basadas en dispositivos desencadenan el temporizador de inactividad desatendido de forma predeterminada a menos que el controlador de dispositivo indique la presencia del usuario. Si el controlador indica la presencia del usuario, se usa el temporizador inactivo del sistema.
-   Si el sistema se reactiva automáticamente, pero el usuario proporciona una nueva entrada mientras se controla el evento, el sistema no vuelve automáticamente a la suspensión según el temporizador de inactividad desatendido. En su lugar, el sistema vuelve a la suspensión según el temporizador de inactividad del sistema.
-   Si el sistema se reactiva debido a la actividad del usuario, el sistema no vuelve automáticamente a la suspensión según el temporizador de inactividad desatendido. En su lugar, el sistema vuelve a la suspensión según el temporizador de inactividad del sistema.

Cuando el sistema se reactiva automáticamente, difunde el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) a todas las aplicaciones. Dado que el usuario no está presente, la mayoría de las aplicaciones no deben hacer nada. Las aplicaciones de control de eventos, como los servidores de fax, deben controlar sus eventos. Para determinar si el sistema está en este estado, llame a la función [**IsSystemResumeAutomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) . Cuando el sistema se reactiva automáticamente, la pantalla no se activa automáticamente.

Si el sistema se reactiva debido a la actividad del usuario, el sistema difundirá primero el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) seguido de un evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) . Además, el sistema activará la pantalla. La aplicación debe volver a abrir los archivos que cerró cuando el sistema entró en suspensión y prepararse para los datos proporcionados por el usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Criterios de suspensión del sistema](system-sleep-criteria.md)
</dt> </dl>

 

 
