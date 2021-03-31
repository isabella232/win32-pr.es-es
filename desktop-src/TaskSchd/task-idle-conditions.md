---
title: Condiciones de inactividad de tareas
description: Una tarea se puede controlar de varias maneras cuando el equipo entra en un estado de inactividad. Esto incluye la definición de un desencadenador inactivo o el establecimiento de las condiciones de inactividad cuando se inicia la tarea.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- condiciones de inactividad Programador de tareas
- condiciones de inactividad Programador de tareas, discusión
- crear desencadenadores inactivos Programador de tareas
- desencadenadores inactivos Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2020
ms.locfileid: "103797151"
---
# <a name="task-idle-conditions"></a>Condiciones de inactividad de tareas

Una tarea se puede controlar de varias maneras cuando el equipo entra en un estado de inactividad. Esto incluye la definición de un desencadenador inactivo o el establecimiento de las condiciones de inactividad cuando se inicia la tarea.

## <a name="detecting-the-idle-state"></a>Detección del estado de inactividad

En Windows 7, el Programador de tareas comprueba que el equipo está en un estado de inactividad cada 15 minutos. Programador de tareas comprueba un estado de inactividad mediante dos criterios: ausencia de usuario y falta de consumo de recursos. El usuario se considera ausente si no hay ninguna entrada de teclado o de mouse durante este período de tiempo. El equipo se considera inactivo si todos los procesadores y todos los discos estaban inactivos durante más del 90% del último intervalo de detección. (Una excepción sería para cualquier aplicación de tipo de presentación que establezca ES \_ Mostrar \_ marca requerida. Esta marca obliga a la programación de tareas a no tener en cuenta el sistema como inactivo, independientemente de la actividad del usuario o del consumo de recursos.

En Windows 7, Programador de tareas considera que un procesador está inactivo incluso cuando se ejecutan subprocesos de prioridad baja (prioridad de subproceso < normal).

En Windows 7, cuando el Programador de tareas detecta que el equipo está inactivo, el servicio espera solo a que los datos proporcionados por el usuario marquen el final del estado de inactividad.

En Windows 8, Programador de tareas realiza las mismas comprobaciones de consumo de recursos y de ausencia general de usuario. Sin embargo, Programador de tareas se basa en el subsistema de alimentación del sistema operativo para detectar la presencia del usuario. De forma predeterminada, se considera que el usuario no está presente después de cuatro minutos sin entradas de teclado o de mouse. El tiempo de comprobación del consumo de recursos se acorta a intervalos de 10 minutos cuando el usuario está presente. Cuando el usuario está fuera, el tiempo de comprobación se acorta a intervalos de 30 segundos. Programador de tareas realiza comprobaciones de consumo de recursos adicionales para los siguientes eventos:

-   Estado de presencia de usuario cambiado
-   Fuente de alimentación de AC/DC cambiada
-   Nivel de batería cambiado (solo cuando está en baterías)

Cuando se produce cualquiera de los eventos anteriores, Programador de tareas comprueba si el equipo está inactivo desde la última hora de comprobación. En la práctica, esto significa que Programador de tareas puede declarar el sistema como inactivo inmediatamente después de que se detecte la ausencia del usuario, si se han cumplido las otras condiciones desde la última hora de comprobación.

En Windows 8, los umbrales de CPU y de e/s se establecen en 80%.

Al detectar el estado de inactividad en Windows 8 Server, Programador de tareas no tiene en cuenta la presencia o ausencia del usuario. Para marcar el final del estado de inactividad, Programador de tareas revisa el consumo de recursos una vez en 90 minutos.

## <a name="defining-an-idle-trigger"></a>Definir un desencadenador inactivo

Una tarea se puede iniciar cuando el equipo entra en un estado de inactividad definiendo un desencadenador inactivo.

Un desencadenador inactivo solo desencadenará una acción de tarea si el equipo entra en un estado de inactividad después del límite de inicio del desencadenador.

Una aplicación puede definir un desencadenador inactivo mediante la interfaz [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Si lee o escribe XML, el desencadenador inactivo se especifica mediante el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) del esquema de programador de tareas.

## <a name="task-settings-for-idle-conditions"></a>Configuración de tareas para condiciones de inactividad

La configuración de la tarea se puede usar para definir el modo en que el Programador de tareas controla la tarea cuando el equipo entra en un estado de inactividad.

Las siguientes ilustraciones proporcionan tres escalas de tiempo posibles que muestran cómo se relacionan entre sí estas condiciones de inactividad diferentes. Tenga en cuenta que las ilustraciones se inician cuando se activa el desencadenador de tarea o cuando la tarea se inicia a petición (sin solicitar [la omisión de las restricciones de tarea existentes](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)).

> [!NOTE]
> La configuración de *Duration* y *WaitTimeout* está en desuso. Todavía están presentes en la interfaz de usuario de Programador de tareas y sus métodos de interfaz todavía pueden devolver valores válidos, pero ya no se usan.

![escala de tiempo de condición inactiva](images/idle-conditions2.png)

En la lista siguiente se describen las condiciones de inactividad.
- Inicio de inactividad: la hora a la que el equipo entra en el estado de inactividad.
- Fin de inactividad: la hora a la que el equipo realiza la transición fuera del estado de inactividad. Tenga en cuenta que la cantidad de tiempo que el equipo está en estado inactivo es independiente del tiempo de inactividad que se ha descrito anteriormente.

La espera de inactividad y la duración de inactividad están desusadas.
- Espera inactiva: la cantidad de tiempo que el Programador de tareas esperará a que se produzca un estado de inactividad después de que se active un desencadenador de tarea o después de que la tarea se inicie a petición.
- Duración de inactividad: la cantidad de tiempo que desea que el equipo esté inactivo antes de iniciar la tarea.

Por ejemplo, si una tarea está configurada para iniciarse solo si el equipo está inactivo durante 30 minutos y la tarea espera a que el equipo esté inactivo durante 10 minutos, la tarea se iniciará en 5 minutos solo si el equipo ha estado inactivo durante 25 minutos antes de que se activara el desencadenador. La tarea no se iniciará si el equipo entra en un estado de inactividad 5 minutos después de que se active el desencadenador.

De forma predeterminada, una propiedad [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) de la tarea se establece en true, lo que significa que el servicio Programador de tareas no ejecutará las tareas desencadenadas por un desencadenador inactivo (o un desencadenador con condiciones de inactividad) cuando un equipo está funcionando con batería. Puede cambiar este comportamiento estableciendo la propiedad **DisallowStartIfOnBatteries** en false.

Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) de la interfaz [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) ([**IdleSettings**](idlesettings.md) para scripting).

Las aplicaciones pueden controlar las condiciones de inactividad mediante el establecimiento de las propiedades de las interfaces [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) y [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Si se lee o se escribe XML, estas condiciones se especifican en el elemento [**Settings**](taskschedulerschema-settings-tasktype-element.md) del esquema de programador de tareas.

## <a name="cycling-idle-condition"></a>Ciclo inactivo de condición

Si el equipo está recorriendo y sale del estado de inactividad, puede finalizar y reiniciar la tarea con las siguientes condiciones de inactividad. Para finalizar y reiniciar una tarea, tanto las propiedades como los elementos deben establecerse en true:

-   Para finalizar la tarea cuando finalice la condición de inactividad, establezca la propiedad [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) o el elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) en true.
-   Para reiniciar la tarea cuando el equipo vuelva a la condición de inactividad, establezca la propiedad [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) o el elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) en true.
