---
title: Condiciones de inactividad de tareas
description: Una tarea se puede controlar de varias maneras cuando el equipo entra en un estado de inactividad. Esto incluye definir un desencadenador inactivo o establecer las condiciones de inactividad para cuando se inicia la tarea.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- condiciones de inactividad Programador de tareas
- condiciones de inactividad Programador de tareas , discusión
- crear desencadenadores inactivos Programador de tareas
- desencadenadores inactivos Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f21f11939808f147020d29e4d10e04b62b404820c413f88fab3bafe2654d6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072604"
---
# <a name="task-idle-conditions"></a>Condiciones de inactividad de tareas

Una tarea se puede controlar de varias maneras cuando el equipo entra en un estado de inactividad. Esto incluye definir un desencadenador inactivo o establecer las condiciones de inactividad para cuando se inicia la tarea.

## <a name="detecting-the-idle-state"></a>Detección del estado de inactividad

En Windows 7, el Programador de tareas comprueba que el equipo está en estado inactivo cada 15 minutos. Programador de tareas comprueba si hay un estado de inactividad con dos criterios: ausencia del usuario y falta de consumo de recursos. El usuario se considera ausente si no hay ninguna entrada de teclado o mouse durante este período de tiempo. El equipo se considera inactivo si todos los procesadores y todos los discos estaban inactivos durante más del 90 % del último intervalo de detección. (Una excepción sería para cualquier aplicación de tipo de presentación que establece el es \_ Marca DISPLAY \_ REQUIRED. Esta marca obliga a la programación de tareas a no considerar el sistema como inactivo, independientemente de la actividad del usuario o el consumo de recursos).

En Windows 7, Programador de tareas un procesador como inactivo incluso cuando se ejecutan subprocesos de prioridad baja (prioridad de subproceso < normal).

En Windows 7, cuando el Programador de tareas detecta que el equipo está inactivo, el servicio espera solo la entrada del usuario para marcar el final del estado de inactividad.

En Windows 8, Programador de tareas realiza las mismas comprobaciones generales de ausencia de usuario y consumo de recursos. Sin embargo, Programador de tareas se basa en el subsistema de energía del sistema operativo para detectar la presencia del usuario. De forma predeterminada, el usuario se considera ausente después de cuatro minutos sin entrada del teclado ni del mouse. El tiempo de comprobación del consumo de recursos se reduce a intervalos de 10 minutos cuando el usuario está presente. Cuando el usuario está fuera, el tiempo de comprobación se reduce a intervalos de 30 segundos. Programador de tareas realiza comprobaciones de consumo de recursos adicionales para los siguientes eventos:

-   Estado de presencia del usuario cambiado
-   Fuente de alimentación de CA/DC cambiada
-   Se ha cambiado el nivel de batería (solo cuando está en baterías)

Cuando se produce cualquiera de los eventos anteriores, Programador de tareas prueba la inactividad del equipo desde la hora de la última comprobación. En la práctica, esto significa Programador de tareas declarar el sistema como inactivo inmediatamente después de que se detecte la ausencia del usuario, si se cumplen las otras condiciones desde la hora de la última comprobación.

En Windows 8, los umbrales de CPU y E/S se establecen en el 80 %.

Al detectar el estado de inactividad en Windows 8 Server, Programador de tareas no tiene en cuenta la presencia o ausencia del usuario. Para marcar el final del estado de inactividad, Programador de tareas el consumo de recursos una vez en 90 minutos.

## <a name="defining-an-idle-trigger"></a>Definición de un desencadenador inactivo

Se puede iniciar una tarea cuando el equipo entra en un estado de inactividad mediante la definición de un desencadenador inactivo.

Un desencadenador inactivo solo desencadenará una acción de tarea si el equipo entra en un estado de inactividad después del límite inicial del desencadenador.

Una aplicación puede definir un desencadenador inactivo mediante la [**interfaz IIdleTrigger.**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)

Si lee o escribe XML, el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) del esquema Programador de tareas inactivo especifica el desencadenador inactivo.

## <a name="task-settings-for-idle-conditions"></a>Configuración de tareas para condiciones de inactividad

La configuración de la tarea se puede usar para definir cómo el Programador de tareas controla la tarea cuando el equipo entra en un estado de inactividad.

En las ilustraciones siguientes se proporcionan tres escalas de tiempo posibles que muestran cómo se relacionan entre sí estas distintas condiciones de inactividad. Tenga en cuenta que las ilustraciones se inician cuando se activa el desencadenador de tareas o cuando la tarea se inicia a petición (sin solicitar omitir las [restricciones de tarea existentes).](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)

> [!NOTE]
> La *configuración de* *Duración y Tiempo de espera* está en desuso. Todavía están presentes en la interfaz Programador de tareas usuario y sus métodos de interfaz pueden devolver valores válidos, pero ya no se usan.

![escala de tiempo de condición de inactividad](images/idle-conditions2.png)

En la lista siguiente se describen las condiciones de inactividad.
- Inicio de inactividad: hora a la que el equipo entra en el estado de inactividad.
- Idle end (Fin de inactividad): hora a la que el equipo pasa fuera del estado de inactividad. Tenga en cuenta que la cantidad de tiempo que el equipo está en estado de inactividad es independiente del tiempo de duración de inactividad descrito anteriormente.

La espera de inactividad y la duración de inactividad han quedado en desuso.
- Espera inactiva: la cantidad de tiempo que el Programador de tareas esperará a que se produzca un estado de inactividad después de activar un desencadenador de tareas o después de que la tarea se inicia a petición.
- Duración de inactividad: la cantidad de tiempo que desea que el equipo esté inactivo antes de iniciar la tarea.

Por ejemplo, si una tarea está configurada para iniciarse solo si el equipo está inactivo durante 30 minutos y la tarea espera a que el equipo esté inactivo durante 10 minutos, la tarea se iniciará en 5 minutos solo si el equipo ha estado inactivo durante 25 minutos antes del momento en que se activó el desencadenador. La tarea no se iniciará si el equipo entra en un estado de inactividad 5 minutos después de activar el desencadenador.

De forma predeterminada, una propiedad [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) de tarea se establece en true, lo que significa que el servicio Programador de tareas no ejecutará tareas desencadenadas por un desencadenador inactivo (o un desencadenador con condiciones de inactividad) cuando un equipo se ejecuta con batería. Puede cambiar este comportamiento estableciendo la **propiedad DisallowStartIfOnBatteries** en false.

Si un desencadenador inactivo desencadena una tarea, se omite la propiedad [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) de la interfaz [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) [**(IdleSettings**](idlesettings.md) para scripting).

Las aplicaciones pueden controlar las condiciones de inactividad estableciendo las propiedades en las interfaces [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) e [**IIdleTrigger.**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)

Si lee o escribe XML, estas condiciones se especifican en el [**elemento Configuración**](taskschedulerschema-settings-tasktype-element.md) del Programador de tareas esquema.

## <a name="cycling-idle-condition"></a>Condición de inactividad de ciclo

Si el equipo está dentro y fuera del estado de inactividad, puede finalizar y reiniciar la tarea con las siguientes condiciones de inactividad. Para finalizar y reiniciar una tarea, tanto las propiedades como los elementos deben establecerse en True:

-   Para finalizar la tarea cuando finalice la condición de inactividad, establezca la [**propiedad StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) o el [**elemento StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) en True.
-   Para reiniciar la tarea cuando el equipo vuelva a pasar a la condición de inactividad, establezca la propiedad [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) o el [**elemento RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) en True.
