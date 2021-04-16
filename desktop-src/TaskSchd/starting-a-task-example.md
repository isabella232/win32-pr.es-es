---
title: Ejemplo de inicio de una tarea
description: Para iniciar una tarea, llame al método Run de la interfaz ITask. Run es un método asincrónico que intenta ejecutar la tarea y vuelve en cuanto se inicia la tarea. El servicio de Programador de tareas debe estar en ejecución para que este método se ejecute correctamente.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685779"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="1c48d-105">Ejemplo de inicio de una tarea</span><span class="sxs-lookup"><span data-stu-id="1c48d-105">Starting a Task Example</span></span>

<span data-ttu-id="1c48d-106">Para iniciar una tarea, llame al método [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) de la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="1c48d-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="1c48d-107">**Run** es un método asincrónico que intenta ejecutar la tarea y vuelve en cuanto se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="1c48d-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="1c48d-108">El servicio de Programador de tareas debe estar en ejecución para que este método se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c48d-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="1c48d-109">En el procedimiento siguiente se describe cómo iniciar una tarea.</span><span class="sxs-lookup"><span data-stu-id="1c48d-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="1c48d-110">**Para iniciar una tarea**</span><span class="sxs-lookup"><span data-stu-id="1c48d-110">**To start a task**</span></span>

1.  <span data-ttu-id="1c48d-111">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="1c48d-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="1c48d-112">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="1c48d-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="1c48d-113">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="1c48d-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="1c48d-114">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="1c48d-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="1c48d-115">Llame a [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) para iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="1c48d-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="1c48d-116">Tenga en cuenta que este método es heredado por la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="1c48d-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="1c48d-117">Continúe el procesamiento según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1c48d-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="1c48d-118">Llame a **ITask:: Release** para liberar los recursos y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de com.</span><span class="sxs-lookup"><span data-stu-id="1c48d-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="1c48d-119">En este ejemplo se llama a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero a la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="1c48d-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="1c48d-120">(Tenga en cuenta que **Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask**).</span><span class="sxs-lookup"><span data-stu-id="1c48d-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="1c48d-121">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="1c48d-121">For a code example of</span></span>    | <span data-ttu-id="1c48d-122">Vea</span><span class="sxs-lookup"><span data-stu-id="1c48d-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1c48d-123">Ejecutar una tarea existente</span><span class="sxs-lookup"><span data-stu-id="1c48d-123">Running an existing task</span></span> | [<span data-ttu-id="1c48d-124">Ejemplo de código de C/C++: iniciar una tarea</span><span class="sxs-lookup"><span data-stu-id="1c48d-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="1c48d-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c48d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c48d-126">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="1c48d-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 