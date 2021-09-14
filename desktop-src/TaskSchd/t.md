---
title: T (Programador de tareas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170654"
---
# <a name="t-task-scheduler"></a>T (Programador de tareas)

A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objetos task**
</dt> <dd>

Instancias de un objeto que proporciona métodos para administrar tareas. Esto incluye métodos para establecer y recuperar propiedades; ejecutar, terminar y eliminar tareas; y crear nuevos desencadenadores y recuperar desencadenadores antiguos.

El objeto de tarea se crea mediante llamadas a [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objetos del programador de tareas**
</dt> <dd>

Instancias de un objeto que representa el Programador de tareas servicio. Este objeto admite dos interfaces: **IUnknown** e [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (actualmente, las tareas son el único tipo de elementos de trabajo admitidos por el servicio Programador de tareas trabajo).

Los objetos del programador de tareas se crean mediante llamadas **a CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objetos de desencadenador de tareas**
</dt> <dd>

Instancias de un objeto proporciona métodos para establecer y recuperar desencadenadores de tareas. Este objeto admite dos interfaces: **IUnknown** e [**ITaskTrigger.**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)

Los objetos de desencadenador de tareas se crean mediante llamadas a [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

Vea también: *desencadenadores*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**Tareas**
</dt> <dd>

Cualquier elemento que el Programador de tareas puede ejecutar. Estos elementos pueden incluir cualquiera de los siguientes elementos (según sea compatible con el sistema operativo en el que se ejecutará la tarea): aplicaciones Win32®, aplicaciones Win16, aplicaciones de OS/2, aplicaciones MS-DOS®, archivos por lotes (.bat), archivos de comandos ( .cmd) o cualquier tipo de archivo registrado \* \* correctamente.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Carpeta Tasks**
</dt> <dd>

Carpeta que enumera todos los archivos de tareas (actualmente, las tareas son los únicos elementos de trabajo disponibles). Estos archivos contienen la información sobre la tarea. El nombre de estos archivos refleja el nombre de la tarea.

Puede recuperar la ubicación de la carpeta Tasks del Registro obteniendo datos para el siguiente valor:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**desencadenantes**
</dt> <dd>

Conjunto de criterios que, cuando se cumplan, harán que se ejecute una tarea. Programador de tareas proporciona desencadenadores basados en el tiempo y basados en eventos que pueden especificar horas de inicio de tareas, criterios de repetición y otros parámetros.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**cadenas de desencadenador**
</dt> <dd>

Cadena que describe el desencadenador. Esta cadena la crea el servicio Programador de tareas y aparece en la interfaz de usuario de Programador de tareas con un formato similar a "A las 2 p. m. todos los días, a partir del 11/11/97".

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**estructuras de desencadenador**
</dt> <dd>

Estructura [**TASK \_ TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) usada al establecer o recuperar los criterios que definen el desencadenador. Los criterios incluyen cuándo se activará el desencadenador y el tipo del desencadenador.

</dd> </dl>

 

 




