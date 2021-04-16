---
title: Agregar elementos de trabajo
description: Hay dos maneras de agregar elementos de trabajo al Tasksfolder programado. Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede Agregar un elemento de trabajo existente a la carpeta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Programador de tareas de elementos de trabajo, agregar
- tareas Programador de tareas, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676201"
---
# <a name="adding-work-items"></a><span data-ttu-id="3d7fe-106">Agregar elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="3d7fe-106">Adding Work Items</span></span>

<span data-ttu-id="3d7fe-107">Hay dos maneras de agregar [*elementos de trabajo*](w.md) al [*Tasksfolder programado*](s.md).</span><span class="sxs-lookup"><span data-stu-id="3d7fe-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="3d7fe-108">Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede Agregar un elemento de trabajo existente a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="3d7fe-109">Actualmente, solo se pueden agregar objetos de tarea a la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="3d7fe-110">Al agregar una tarea, debe conocer los identificadores de la clase de tarea y la interfaz de tarea [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="3d7fe-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="3d7fe-111">Cree nuevos elementos de trabajo llamando al método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) .</span><span class="sxs-lookup"><span data-stu-id="3d7fe-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="3d7fe-112">Este método crea un nuevo objeto de elemento de trabajo con el nombre que se proporciona y agrega el elemento de trabajo a la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="3d7fe-113">Cuando se crea un nuevo elemento de trabajo, el Programador de tareas asigna la memoria necesaria para el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="3d7fe-114">Para agregar elementos de trabajo existentes a la carpeta tareas programadas, llame al método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) .</span><span class="sxs-lookup"><span data-stu-id="3d7fe-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="3d7fe-115">Cuando llame a este método, debe crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="3d7fe-116">Los nombres que proporcione para los elementos de trabajo deben ser únicos en la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="3d7fe-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="3d7fe-117">Si ya existe un elemento de trabajo con el mismo nombre cuando se llama al método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o al método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , el método devuelve un error de **\_ archivo \_ de error** .</span><span class="sxs-lookup"><span data-stu-id="3d7fe-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="3d7fe-118">Para obtener más información, vea [crear una tarea mediante el ejemplo de NewWorkItem](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="3d7fe-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




