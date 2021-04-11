---
title: Interfaces Programador de tareas 1,0
description: Las interfaces que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104271921"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="c757f-103">Interfaces Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="c757f-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="c757f-104">\[\[Es posible que esta API se modifique o no esté disponible en versiones posteriores del sistema operativo o del producto.</span><span class="sxs-lookup"><span data-stu-id="c757f-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="c757f-105">En su lugar, use las [Interfaces Programador de tareas 2,0](task-scheduler-2-0-interfaces.md) o los [tipos enumerados de programador de tareas 2,0](task-scheduler-2-0-enumerated-types.md) . \]\]</span><span class="sxs-lookup"><span data-stu-id="c757f-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="c757f-106">Las interfaces que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c757f-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="c757f-107">Estos temas contienen una descripción de la interfaz, una lista de las propiedades y los métodos definidos por la interfaz, así como comentarios sobre las circunstancias especiales que se deben anotar al usar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c757f-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="c757f-108">Las siguientes interfaces se incluyen en Programador de tareas 1,0.</span><span class="sxs-lookup"><span data-stu-id="c757f-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="c757f-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c757f-109">Interface</span></span>                                        | <span data-ttu-id="c757f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c757f-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c757f-111">**IEnumWorkItems**</span><span class="sxs-lookup"><span data-stu-id="c757f-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="c757f-112">Proporciona los métodos para enumerar las tareas de la [*carpeta tareas programadas*](s.md).</span><span class="sxs-lookup"><span data-stu-id="c757f-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="c757f-113">**IProvideTaskPage**</span><span class="sxs-lookup"><span data-stu-id="c757f-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="c757f-114">Proporciona los métodos para tener acceso a la configuración de la hoja de propiedades de una tarea.</span><span class="sxs-lookup"><span data-stu-id="c757f-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="c757f-115">**IScheduledWorkItem**</span><span class="sxs-lookup"><span data-stu-id="c757f-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="c757f-116">Proporciona los métodos para administrar [*elementos de trabajo*](w.md)específicos.</span><span class="sxs-lookup"><span data-stu-id="c757f-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="c757f-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="c757f-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="c757f-118">Proporciona los métodos para ejecutar tareas, obtener o establecer información de tareas y finalizar tareas.</span><span class="sxs-lookup"><span data-stu-id="c757f-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="c757f-119">Se deriva de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) y hereda todos los métodos de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="c757f-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="c757f-120">**ITaskScheduler**</span><span class="sxs-lookup"><span data-stu-id="c757f-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="c757f-121">Proporciona los métodos para programar tareas.</span><span class="sxs-lookup"><span data-stu-id="c757f-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="c757f-122">**ITaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="c757f-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="c757f-123">Proporciona los métodos para tener acceso a los desencadenadores de una tarea y establecer su configuración.</span><span class="sxs-lookup"><span data-stu-id="c757f-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="c757f-124">Los desencadenadores especifican las horas de inicio de la tarea, los criterios de repetición y otros parámetros que controlan Cuándo se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="c757f-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




