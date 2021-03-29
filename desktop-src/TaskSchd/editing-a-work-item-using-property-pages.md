---
title: Editar un elemento de trabajo mediante páginas de propiedades
description: Puede editar las propiedades de un elemento de trabajo mediante la interfaz gráfica de usuario proporcionada por el servicio de Programador de tareas.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- editar elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792141"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="77cbb-104">Editar un elemento de trabajo mediante páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="77cbb-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="77cbb-105">Puede editar las propiedades de un elemento de trabajo mediante la interfaz gráfica de usuario proporcionada por el servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="77cbb-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="77cbb-106">(Actualmente, los únicos elementos de trabajo válidos son tareas).</span><span class="sxs-lookup"><span data-stu-id="77cbb-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="77cbb-107">En el procedimiento siguiente se describe cómo editar una tarea mediante sus páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="77cbb-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="77cbb-108">**Para editar una tarea mediante sus páginas de propiedades**</span><span class="sxs-lookup"><span data-stu-id="77cbb-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="77cbb-109">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="77cbb-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="77cbb-110">(En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="77cbb-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="77cbb-111">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="77cbb-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="77cbb-112">(Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).</span><span class="sxs-lookup"><span data-stu-id="77cbb-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="77cbb-113">Llame a [**IScheduledWorkItem:: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) para mostrar las páginas de propiedades de la tarea.</span><span class="sxs-lookup"><span data-stu-id="77cbb-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="77cbb-114">Edite las propiedades de la tarea según sea necesario y haga clic en Aceptar para aceptar los nuevos valores y quitar las páginas de propiedades que se muestran.</span><span class="sxs-lookup"><span data-stu-id="77cbb-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="77cbb-115">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="77cbb-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="77cbb-116">Vea</span><span class="sxs-lookup"><span data-stu-id="77cbb-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77cbb-117">Mostrar las páginas de propiedades de una tarea conocida y permitir que un usuario edite las propiedades del elemento de trabajo</span><span class="sxs-lookup"><span data-stu-id="77cbb-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="77cbb-118">Ejemplo de código de C/C++: editar un elemento de trabajo</span><span class="sxs-lookup"><span data-stu-id="77cbb-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="77cbb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77cbb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77cbb-120">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="77cbb-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 