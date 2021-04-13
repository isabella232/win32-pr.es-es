---
title: Crear una tarea mediante el ejemplo NewWorkItem
description: Al crear una tarea, usará dos interfaces Programador de tareas ITaskScheduler y ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- crear elementos de trabajo Programador de tareas
- Programador de tareas de elementos de trabajo, crear tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359202"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="4b9b3-105">Crear una tarea mediante el ejemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="4b9b3-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="4b9b3-106">Al crear una tarea, usará dos interfaces Programador de tareas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) y [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="4b9b3-107">Debe proporcionar un nombre único para la tarea, el identificador de clase del objeto de tarea y el identificador de interfaz de **ITask**.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="4b9b3-108">El identificador de clase y el identificador de interfaz se muestran en el ejemplo de código que aparece a continuación de este tema.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="4b9b3-109">También puede crear una tarea mediante una llamada a [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="4b9b3-110">Al realizar esta ruta, es su responsabilidad crear una instancia del objeto de **tarea** (que admite la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ) y, a continuación, agregar la tarea con el nombre que proporcione.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b9b3-111">De forma predeterminada, solo un miembro del grupo administradores, operadores de copia de seguridad o operadores de servidor puede crear tareas en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="4b9b3-112">Un miembro del grupo administradores puede cambiar el descriptor de seguridad de la \\ carpeta de tareas de Windows para permitir que otros usuarios creen tareas.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="4b9b3-113">El nombre que proporcione para la tarea debe ser único en la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="4b9b3-114">Si ya existe una tarea con el mismo nombre, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) devuelve el \_ archivo de error \_ .</span><span class="sxs-lookup"><span data-stu-id="4b9b3-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="4b9b3-115">Si obtiene este valor devuelto, debe especificar un nombre diferente e intentar crear la tarea de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="4b9b3-116">En el procedimiento siguiente se describe cómo crear una nueva tarea de elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="4b9b3-117">**Para crear una nueva tarea de elemento de trabajo**</span><span class="sxs-lookup"><span data-stu-id="4b9b3-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="4b9b3-118">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="4b9b3-119">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="4b9b3-120">Llame a [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para crear una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="4b9b3-121">(Este método devuelve un puntero a una interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="4b9b3-122">Guarde la nueva tarea en el disco llamando a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="4b9b3-123">(La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz **ITask** ).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="4b9b3-124">Llame a **ITask:: Release** para liberar todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="4b9b3-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="4b9b3-125">(Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="4b9b3-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="4b9b3-126">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="4b9b3-126">For a code example of</span></span>  | <span data-ttu-id="4b9b3-127">Vea</span><span class="sxs-lookup"><span data-stu-id="4b9b3-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b3-128">Crear una única tarea</span><span class="sxs-lookup"><span data-stu-id="4b9b3-128">Creating a single task</span></span> | [<span data-ttu-id="4b9b3-129">Ejemplo de código de C/C++: crear una tarea mediante NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="4b9b3-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="4b9b3-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b9b3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b9b3-131">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="4b9b3-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 