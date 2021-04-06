---
title: Ejemplo de recuperación de una página de tareas
description: Para recuperar una página de tareas, debe llamar a ITask QueryInterface para recuperar la interfaz IProvideTaskPage y, a continuación, llamar a IProvideTaskPage GetPage. El método GetPage devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recuperando Programador de tareas de página de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077919"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="d4df5-105">Ejemplo de recuperación de una página de tareas</span><span class="sxs-lookup"><span data-stu-id="d4df5-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="d4df5-106">Para recuperar una página de tareas, debe llamar a **ITask:: QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y, a continuación, llamar a [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span><span class="sxs-lookup"><span data-stu-id="d4df5-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="d4df5-107">El método **GetPage** devuelve un identificador a la página, que se puede usar para mostrar la página solicitada.</span><span class="sxs-lookup"><span data-stu-id="d4df5-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="d4df5-108">En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="d4df5-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="d4df5-109">En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d4df5-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="d4df5-110">**Para crear un nuevo desencadenador**</span><span class="sxs-lookup"><span data-stu-id="d4df5-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="d4df5-111">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d4df5-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="d4df5-112">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="d4df5-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="d4df5-113">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="d4df5-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="d4df5-114">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="d4df5-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="d4df5-115">Llame a **ITask:: QueryInterface** para recuperar la interfaz [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) y [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar la página.</span><span class="sxs-lookup"><span data-stu-id="d4df5-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="d4df5-116">Con el identificador de página devuelto, muestre la página.</span><span class="sxs-lookup"><span data-stu-id="d4df5-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="d4df5-117">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="d4df5-117">For a code example of</span></span>                                   | <span data-ttu-id="d4df5-118">Vea</span><span class="sxs-lookup"><span data-stu-id="d4df5-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d4df5-119">Recuperar y mostrar la página de tareas de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="d4df5-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="d4df5-120">Recuperación de una página de tareas</span><span class="sxs-lookup"><span data-stu-id="d4df5-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="d4df5-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4df5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4df5-122">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="d4df5-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 