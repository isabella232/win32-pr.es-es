---
title: Programador de tareas para desarrolladores
description: El Programador de tareas permite realizar automáticamente las tareas rutinarias en un equipo seleccionado. Programador de tareas lo hace mediante la supervisión de los criterios que elija (denominados desencadenadores) y la ejecución de las tareas cuando se cumplan esos criterios.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Programador de tareas para desarrolladores
- Programador de tareas para el desarrollo
- Desarrollo con Programador de tareas
- Programador de tareas, página del portal
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2019
ms.locfileid: "104148865"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="65e0f-108">Programador de tareas para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="65e0f-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65e0f-109">Este tema y los otros temas de esta sección son para un público del desarrollador.</span><span class="sxs-lookup"><span data-stu-id="65e0f-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="65e0f-110">Si desea usar el componente de Programador de tareas en su capacidad como administrador o como profesional de ti, consulte [programador de tareas](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="65e0f-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="65e0f-111">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65e0f-111">About the Task Scheduler</span></span>

<span data-ttu-id="65e0f-112">El Programador de tareas permite realizar automáticamente las tareas rutinarias en un equipo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="65e0f-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="65e0f-113">Programador de tareas lo hace mediante la supervisión de los criterios que elija (denominados desencadenadores) y la ejecución de las tareas cuando se cumplan esos criterios.</span><span class="sxs-lookup"><span data-stu-id="65e0f-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="65e0f-114">Puede utilizar la Programador de tareas para ejecutar tareas como el inicio de una aplicación, el envío de un mensaje de correo electrónico o la presentación de un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="65e0f-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="65e0f-115">Las tareas se pueden programar para que se ejecuten en respuesta a estos eventos o desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="65e0f-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="65e0f-116">Cuando se produce un evento de sistema específico.</span><span class="sxs-lookup"><span data-stu-id="65e0f-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="65e0f-117">En un momento dado.</span><span class="sxs-lookup"><span data-stu-id="65e0f-117">At a specific time.</span></span>
- <span data-ttu-id="65e0f-118">A una hora específica en una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="65e0f-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="65e0f-119">En un momento específico según una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="65e0f-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="65e0f-120">A una hora específica en una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="65e0f-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="65e0f-121">A una hora específica de una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="65e0f-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="65e0f-122">Cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="65e0f-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="65e0f-123">Cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="65e0f-123">When the task is registered.</span></span>
- <span data-ttu-id="65e0f-124">Cuando se arranca el sistema.</span><span class="sxs-lookup"><span data-stu-id="65e0f-124">When the system is booted.</span></span>
- <span data-ttu-id="65e0f-125">Cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="65e0f-125">When a user logs on.</span></span>
- <span data-ttu-id="65e0f-126">Cuando una sesión de Terminal Server cambia de estado.</span><span class="sxs-lookup"><span data-stu-id="65e0f-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="65e0f-127">Desarrolladores</span><span class="sxs-lookup"><span data-stu-id="65e0f-127">Developers</span></span>

<span data-ttu-id="65e0f-128">El Programador de tareas proporciona las API de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="65e0f-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="65e0f-129">Programador de tareas 2,0: se proporcionan interfaces y objetos para C++ y para el desarrollo de scripting, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="65e0f-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="65e0f-130">Programador de tareas 1,0: se proporcionan interfaces para el desarrollo de C++.</span><span class="sxs-lookup"><span data-stu-id="65e0f-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="65e0f-131">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="65e0f-131">Run-time requirements</span></span>

<span data-ttu-id="65e0f-132">El Programador de tareas requiere los siguientes sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="65e0f-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="65e0f-133">Programador de tareas 2,0: el cliente requiere Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="65e0f-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="65e0f-134">El servidor requiere Windows Server 2008 o posterior.</span><span class="sxs-lookup"><span data-stu-id="65e0f-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="65e0f-135">Programador de tareas 1,0: el cliente requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65e0f-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="65e0f-136">El servidor requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="65e0f-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65e0f-137">En esta sección</span><span class="sxs-lookup"><span data-stu-id="65e0f-137">In this section</span></span>

| <span data-ttu-id="65e0f-138">Tema</span><span class="sxs-lookup"><span data-stu-id="65e0f-138">Topic</span></span> | <span data-ttu-id="65e0f-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="65e0f-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="65e0f-140">Novedades de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65e0f-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="65e0f-141">Resumen de las nuevas funciones introducidas por el Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="65e0f-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="65e0f-142">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65e0f-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="65e0f-143">Información conceptual general sobre la API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="65e0f-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="65e0f-144">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65e0f-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="65e0f-145">Ejemplos de código que muestran cómo usar las API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="65e0f-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="65e0f-146">Referencia de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65e0f-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="65e0f-147">Información de referencia detallada sobre las API de Programador de tareas y el esquema de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="65e0f-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |