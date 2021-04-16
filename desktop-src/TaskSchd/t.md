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
# <a name="t-task-scheduler"></a><span data-ttu-id="69c25-103">T (Programador de tareas)</span><span class="sxs-lookup"><span data-stu-id="69c25-103">T (Task Scheduler)</span></span>

<span data-ttu-id="69c25-104">A B C D [E](e.md) F G H [I](i.md) J K L M N o [p](p.md) Q R [s](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="69c25-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="69c25-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objetos de tarea**</span><span class="sxs-lookup"><span data-stu-id="69c25-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-106">Instancias de un objeto que proporciona métodos para administrar tareas.</span><span class="sxs-lookup"><span data-stu-id="69c25-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="69c25-107">Esto incluye métodos para establecer y recuperar propiedades; ejecutar, terminar y eliminar tareas; y la creación de desencadenadores nuevos y la recuperación de los desencadenadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="69c25-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="69c25-108">El objeto de tarea se crea mediante llamadas a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) y [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="69c25-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="69c25-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objetos del programador de tareas**</span><span class="sxs-lookup"><span data-stu-id="69c25-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-110">Instancias de un objeto que representa el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="69c25-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="69c25-111">Este objeto admite dos interfaces: **IUnknown** y [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (actualmente, las tareas son el único tipo de elementos de trabajo admitidos por el servicio Programador de tareas).</span><span class="sxs-lookup"><span data-stu-id="69c25-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="69c25-112">Los objetos del programador de tareas se crean mediante llamadas a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="69c25-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="69c25-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objetos de desencadenador de tarea**</span><span class="sxs-lookup"><span data-stu-id="69c25-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-114">Instancias de un objeto que proporciona métodos para establecer y recuperar desencadenadores de tareas.</span><span class="sxs-lookup"><span data-stu-id="69c25-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="69c25-115">Este objeto admite dos interfaces: **IUnknown** y [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="69c25-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="69c25-116">Los objetos de desencadenador de tarea se crean mediante llamadas a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) y [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="69c25-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="69c25-117">Vea también: *desencadenadores*.</span><span class="sxs-lookup"><span data-stu-id="69c25-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="69c25-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tareas**</span><span class="sxs-lookup"><span data-stu-id="69c25-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-119">Cualquier elemento que el Programador de tareas pueda ejecutar.</span><span class="sxs-lookup"><span data-stu-id="69c25-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="69c25-120">Estos elementos pueden incluir cualquiera de los siguientes (tal y como lo admite el sistema operativo en el que se ejecutará la tarea): Win32® aplicaciones, aplicaciones de Win16, sistema operativo/2, aplicaciones de® de MS-DOS, archivos por lotes ( \* . bat), archivos de comandos ( \* . cmd) o cualquier tipo de archivo registrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="69c25-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="69c25-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Carpeta tareas**</span><span class="sxs-lookup"><span data-stu-id="69c25-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-122">La carpeta en la que se enumeran todos los archivos de tareas (actualmente, las tareas son los únicos elementos de trabajo disponibles).</span><span class="sxs-lookup"><span data-stu-id="69c25-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="69c25-123">Estos archivos contienen la información sobre la tarea.</span><span class="sxs-lookup"><span data-stu-id="69c25-123">These files contain the information about the task.</span></span> <span data-ttu-id="69c25-124">El nombre de estos archivos refleja el nombre de la tarea.</span><span class="sxs-lookup"><span data-stu-id="69c25-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="69c25-125">Puede recuperar la ubicación de la carpeta de tareas del registro obteniendo datos para el valor siguiente:</span><span class="sxs-lookup"><span data-stu-id="69c25-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="69c25-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="69c25-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-127">Un conjunto de criterios que, cuando se cumplen, provocarán la ejecución de una tarea.</span><span class="sxs-lookup"><span data-stu-id="69c25-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="69c25-128">Programador de tareas proporciona desencadenadores basados en el tiempo y en eventos que pueden especificar las horas de inicio de la tarea, los criterios de repetición y otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="69c25-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="69c25-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**cadenas de desencadenador**</span><span class="sxs-lookup"><span data-stu-id="69c25-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-130">Cadena que describe el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="69c25-130">A string that describes the trigger.</span></span> <span data-ttu-id="69c25-131">Esta cadena la crea el servicio de Programador de tareas y aparece en la Programador de tareas interfaz de usuario en un formulario similar a "a las 14:00 días, a partir del 5/11/97".</span><span class="sxs-lookup"><span data-stu-id="69c25-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="69c25-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**estructuras de desencadenador**</span><span class="sxs-lookup"><span data-stu-id="69c25-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="69c25-133">Estructura [**del \_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea que se usa al establecer o recuperar los criterios que definen el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="69c25-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="69c25-134">Los criterios incluyen Cuándo se activará el desencadenador y el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="69c25-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




