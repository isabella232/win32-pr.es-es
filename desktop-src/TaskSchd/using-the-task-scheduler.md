---
title: Usar el Programador de tareas
description: Esta sección contiene ejemplos de código que muestran cómo se usa la API de Programador de tareas y ejemplos XML que muestran cómo se definen las tareas en el esquema de Programador de tareas.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- desencadenadores Programador de tareas, ejemplos
- Inicio de una tarea Programador de tareas
- crear tareas Programador de tareas
- Programador de tareas Programador de tareas, usar
- Programador de tareas ejemplos Programador de tareas
- Programador de tareas Programador de tareas, ejemplos vea ejemplos de Programador de tareas Programador de tareas
- ejemplos Programador de tareas ver Programador de tareas ejemplos Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676095"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="11a56-110">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-110">Using the Task Scheduler</span></span>

<span data-ttu-id="11a56-111">Esta sección contiene ejemplos de código que muestran cómo se usa la API de Programador de tareas y ejemplos XML que muestran cómo se definen las tareas en el esquema de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="11a56-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="11a56-112">La mayoría de estos ejemplos son código independiente que puede ejecutarse de forma independiente o pegarse en una aplicación más grande y modificarse según los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11a56-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="11a56-113">En la tabla siguiente se enumeran Programador de tareas ejemplos de 2,0 incluidos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="11a56-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="11a56-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11a56-114">Example</span></span>                                                                                                    | <span data-ttu-id="11a56-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a56-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="11a56-116">Iniciar un archivo ejecutable en un momento específico</span><span class="sxs-lookup"><span data-stu-id="11a56-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="11a56-117">Define una tarea que inicia el Bloc de notas a una hora especificada.</span><span class="sxs-lookup"><span data-stu-id="11a56-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="11a56-118">Iniciar un archivo ejecutable diariamente</span><span class="sxs-lookup"><span data-stu-id="11a56-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="11a56-119">Define una tarea que inicia el Bloc de notas diariamente.</span><span class="sxs-lookup"><span data-stu-id="11a56-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="11a56-120">Iniciar un archivo ejecutable en el arranque del sistema</span><span class="sxs-lookup"><span data-stu-id="11a56-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="11a56-121">Define una tarea que inicia el Bloc de notas al arrancar el sistema.</span><span class="sxs-lookup"><span data-stu-id="11a56-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="11a56-122">Iniciar una aplicación ejecutable semanalmente</span><span class="sxs-lookup"><span data-stu-id="11a56-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="11a56-123">Define una tarea que inicia el Bloc de notas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="11a56-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="11a56-124">Iniciar un archivo ejecutable cuando se registra una tarea</span><span class="sxs-lookup"><span data-stu-id="11a56-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="11a56-125">Define una tarea que inicia el Bloc de notas cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="11a56-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="11a56-126">Iniciar un archivo ejecutable cuando un usuario inicia sesión</span><span class="sxs-lookup"><span data-stu-id="11a56-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="11a56-127">Define una tarea que inicia el Bloc de notas cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="11a56-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="11a56-128">Enumerar tareas y Mostrar información de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="11a56-129">Enumera todas las tareas en el equipo local y muestra el estado de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="11a56-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="11a56-130">En la tabla siguiente se enumeran Programador de tareas ejemplos de 1,0 incluidos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="11a56-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="11a56-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11a56-131">Example</span></span>                                                                                    | <span data-ttu-id="11a56-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a56-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11a56-133">Crear una tarea mediante el ejemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="11a56-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="11a56-134">Crea una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="11a56-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="11a56-135">Ejemplo de enumeración de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="11a56-136">Enumera todas las tareas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="11a56-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="11a56-137">Ejemplo de inicio de una tarea</span><span class="sxs-lookup"><span data-stu-id="11a56-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="11a56-138">Inicia una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="11a56-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="11a56-139">Editar un elemento de trabajo mediante páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="11a56-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="11a56-140">Muestra las páginas de propiedades de una tarea para su edición.</span><span class="sxs-lookup"><span data-stu-id="11a56-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="11a56-141">Recuperar ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="11a56-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="11a56-142">Un conjunto de ejemplos que muestran cómo recuperar las propiedades que se aplican a todos los tipos de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="11a56-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="11a56-143">Configuración de ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="11a56-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="11a56-144">Un conjunto de ejemplos que muestran cómo establecer las propiedades que se aplican a todos los tipos de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="11a56-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="11a56-145">Recuperación de ejemplos de propiedades de tarea</span><span class="sxs-lookup"><span data-stu-id="11a56-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="11a56-146">Un conjunto de ejemplos que muestran cómo recuperar propiedades únicas de las tareas.</span><span class="sxs-lookup"><span data-stu-id="11a56-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="11a56-147">Configuración de ejemplos de propiedades de tarea</span><span class="sxs-lookup"><span data-stu-id="11a56-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="11a56-148">Un conjunto de ejemplos que muestran cómo establecer propiedades exclusivas de las tareas.</span><span class="sxs-lookup"><span data-stu-id="11a56-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="11a56-149">Ejemplo de recuperación de una página de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="11a56-150">Recupera y muestra la página de tareas generales de una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="11a56-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="11a56-151">Crear un nuevo desencadenador</span><span class="sxs-lookup"><span data-stu-id="11a56-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="11a56-152">Crea un nuevo desencadenador para una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="11a56-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="11a56-153">Ejemplo de creación de un desencadenador inactivo</span><span class="sxs-lookup"><span data-stu-id="11a56-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="11a56-154">Crea un desencadenador de inactividad basado en eventos para una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="11a56-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="11a56-155">Ejemplo de finalización de una tarea</span><span class="sxs-lookup"><span data-stu-id="11a56-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="11a56-156">Finaliza una tarea mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="11a56-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="11a56-157">Ejemplo de recuperación de cadenas de desencadenador</span><span class="sxs-lookup"><span data-stu-id="11a56-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="11a56-158">Recupera la cadena de desencadenador de todos los desencadenadores asociados a una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="11a56-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="11a56-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11a56-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11a56-160">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="11a56-161">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11a56-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




