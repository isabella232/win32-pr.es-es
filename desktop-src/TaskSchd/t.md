---
title: T (Programador de tareas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533669"
---
# <a name="t-task-scheduler"></a>T (Programador de tareas)

A B C D [E](e.md) F G H [I](i.md) J K L M N o [p](p.md) Q R [s](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objetos de tarea**
</dt> <dd>

Instancias de un objeto que proporciona métodos para administrar tareas. Esto incluye métodos para establecer y recuperar propiedades; ejecutar, terminar y eliminar tareas; y la creación de desencadenadores nuevos y la recuperación de los desencadenadores anteriores.

El objeto de tarea se crea mediante llamadas a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) y [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objetos del programador de tareas**
</dt> <dd>

Instancias de un objeto que representa el servicio Programador de tareas. Este objeto admite dos interfaces: **IUnknown** y [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (actualmente, las tareas son el único tipo de elementos de trabajo admitidos por el servicio Programador de tareas).

Los objetos del programador de tareas se crean mediante llamadas a **CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objetos de desencadenador de tarea**
</dt> <dd>

Instancias de un objeto que proporciona métodos para establecer y recuperar desencadenadores de tareas. Este objeto admite dos interfaces: **IUnknown** y [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Los objetos de desencadenador de tarea se crean mediante llamadas a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) y [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

Vea también: *desencadenadores*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tareas**
</dt> <dd>

Cualquier elemento que el Programador de tareas pueda ejecutar. Estos elementos pueden incluir cualquiera de los siguientes (tal y como lo admite el sistema operativo en el que se ejecutará la tarea): Win32® aplicaciones, aplicaciones de Win16, sistema operativo/2, aplicaciones de® de MS-DOS, archivos por lotes ( \* . bat), archivos de comandos ( \* . cmd) o cualquier tipo de archivo registrado correctamente.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Carpeta tareas**
</dt> <dd>

La carpeta en la que se enumeran todos los archivos de tareas (actualmente, las tareas son los únicos elementos de trabajo disponibles). Estos archivos contienen la información sobre la tarea. El nombre de estos archivos refleja el nombre de la tarea.

Puede recuperar la ubicación de la carpeta de tareas del registro obteniendo datos para el valor siguiente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**desencadenadores**
</dt> <dd>

Un conjunto de criterios que, cuando se cumplen, provocarán la ejecución de una tarea. Programador de tareas proporciona desencadenadores basados en el tiempo y en eventos que pueden especificar las horas de inicio de la tarea, los criterios de repetición y otros parámetros.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**cadenas de desencadenador**
</dt> <dd>

Cadena que describe el desencadenador. Esta cadena la crea el servicio de Programador de tareas y aparece en la Programador de tareas interfaz de usuario en un formulario similar a "a las 14:00 días, a partir del 5/11/97".

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**estructuras de desencadenador**
</dt> <dd>

Estructura [**del \_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea que se usa al establecer o recuperar los criterios que definen el desencadenador. Los criterios incluyen Cuándo se activará el desencadenador y el tipo del desencadenador.

</dd> </dl>

 

 




