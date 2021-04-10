---
title: Desencadenadores de tareas
description: Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- crear desencadenadores Programador de tareas
- desencadenadores Programador de tareas
- desencadenadores Programador de tareas, descritos
- desencadenadores Programador de tareas, basados en el tiempo
- desencadenadores Programador de tareas, basados en eventos
- desencadenadores basados en eventos Programador de tareas
- desencadenadores basados en tiempo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268419"
---
# <a name="task-triggers"></a><span data-ttu-id="1c25c-110">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="1c25c-110">Task Triggers</span></span>

<span data-ttu-id="1c25c-111">Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea.</span><span class="sxs-lookup"><span data-stu-id="1c25c-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="1c25c-112">Programador de tareas proporciona desencadenadores basados en tiempo y basados en eventos que pueden iniciar una tarea de varias maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="1c25c-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="1c25c-113">Una tarea determinada puede iniciarse mediante uno o varios desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="1c25c-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="1c25c-114">Una tarea puede tener un máximo de 48 desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="1c25c-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="1c25c-115">Desencadenadores basados en tiempo</span><span class="sxs-lookup"><span data-stu-id="1c25c-115">Time-based Triggers</span></span>

<span data-ttu-id="1c25c-116">Los desencadenadores basados en tiempo inician las tareas a las horas especificadas.</span><span class="sxs-lookup"><span data-stu-id="1c25c-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="1c25c-117">Esto incluye el inicio de la tarea una vez a una hora específica o el inicio de la tarea varias veces en una programación diaria, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="1c25c-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="1c25c-118">Desencadenadores basados en eventos</span><span class="sxs-lookup"><span data-stu-id="1c25c-118">Event-based Triggers</span></span>

<span data-ttu-id="1c25c-119">Los desencadenadores basados en eventos inician una tarea en respuesta a unos determinados eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="1c25c-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="1c25c-120">Por ejemplo, los desencadenadores basados en eventos se pueden establecer para iniciar una tarea cuando se inicia el sistema, cuando un usuario inicia sesión en el equipo local o cuando el sistema se queda inactivo.</span><span class="sxs-lookup"><span data-stu-id="1c25c-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="1c25c-121">Desencadenadores múltiples</span><span class="sxs-lookup"><span data-stu-id="1c25c-121">Multiple Triggers</span></span>

<span data-ttu-id="1c25c-122">Cada tarea se puede iniciar mediante uno o varios desencadenadores, lo que permite iniciar la tarea de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="1c25c-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="1c25c-123">Sin embargo, se implementan varios desencadenadores de manera diferente en Programador de tareas 1,0 y Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="1c25c-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="1c25c-124">En Programador de tareas 2,0, cada desencadenador se define mediante una API de desencadenador independiente que está asociada a la tarea a través de la colección de desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="1c25c-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="1c25c-125">En Programador de tareas 1,0, se pueden considerar varios desencadenadores como una programación, un conjunto de veces en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="1c25c-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="1c25c-126">En este caso, la programación es el conjunto de horas (especificado por la Unión de todos los desencadenadores asociados al elemento de trabajo) en el que se ejecutará un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1c25c-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c25c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c25c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c25c-128">Repetir una tarea</span><span class="sxs-lookup"><span data-stu-id="1c25c-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="1c25c-129">Tipos de desencadenador</span><span class="sxs-lookup"><span data-stu-id="1c25c-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="1c25c-130">Interfaces de desencadenador</span><span class="sxs-lookup"><span data-stu-id="1c25c-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1c25c-131">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="1c25c-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




