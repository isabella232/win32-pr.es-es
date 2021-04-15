---
title: Ejemplo de enumeración de tareas
description: Para enumerar las tareas, debe llamar a la enumeración ITaskScheduler para crear un objeto de enumeración. A continuación, use la interfaz IEnumWorkItems del objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676447"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="e61be-104">Ejemplo de enumeración de tareas</span><span class="sxs-lookup"><span data-stu-id="e61be-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="e61be-105">Para enumerar las tareas, debe llamar a [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para crear un [*objeto de enumeración*](e.md).</span><span class="sxs-lookup"><span data-stu-id="e61be-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="e61be-106">A continuación, use la interfaz [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) del objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="e61be-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="e61be-107">En el procedimiento siguiente se describe cómo enumerar las tareas en la carpeta tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="e61be-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="e61be-108">**Para enumerar las tareas de la carpeta tareas programadas**</span><span class="sxs-lookup"><span data-stu-id="e61be-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="e61be-109">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="e61be-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="e61be-110">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="e61be-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="e61be-111">Llame a [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para obtener un objeto de enumeración.</span><span class="sxs-lookup"><span data-stu-id="e61be-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="e61be-112">Llame a [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) para recuperar las tareas.</span><span class="sxs-lookup"><span data-stu-id="e61be-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="e61be-113">(En este ejemplo se intenta recuperar cinco tareas con cada llamada).</span><span class="sxs-lookup"><span data-stu-id="e61be-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="e61be-114">Procesa las tareas devueltas.</span><span class="sxs-lookup"><span data-stu-id="e61be-114">Process the tasks returned.</span></span> <span data-ttu-id="e61be-115">(Este ejemplo simplemente imprime el nombre de cada tarea en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e61be-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="e61be-116">Libere recursos.</span><span class="sxs-lookup"><span data-stu-id="e61be-116">Release resources.</span></span> <span data-ttu-id="e61be-117">Llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria usada para los nombres.</span><span class="sxs-lookup"><span data-stu-id="e61be-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="e61be-118">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="e61be-118">For a code example of</span></span>                                                         | <span data-ttu-id="e61be-119">Vea</span><span class="sxs-lookup"><span data-stu-id="e61be-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e61be-120">Enumerar todas las tareas de la carpeta tareas programadas del equipo local</span><span class="sxs-lookup"><span data-stu-id="e61be-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="e61be-121">Ejemplo de código de C/C++: enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="e61be-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="e61be-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e61be-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e61be-123">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="e61be-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 