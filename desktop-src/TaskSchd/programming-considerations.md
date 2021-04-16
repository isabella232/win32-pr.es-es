---
title: Consideraciones de programación (Programador de tareas)
description: Al desarrollar aplicaciones que usan el Programador de tareas 1,0, tenga en cuenta los siguientes problemas de programación. La aplicación debe asegurarse de que el servicio de Programador de tareas se está ejecutando antes de intentar realizar llamadas mediante la API de Programador de tareas. Al recuperar cadenas, asegúrese de llamar a CoTaskMemFree para liberar cada cadena una vez que ya no se necesite. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz. Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a IPersistFile Save para guardar el elemento de trabajo en el disco. Después de usar cualquiera de las interfaces proporcionadas por la API de Programador de tareas, asegúrese de llamar a la versión IUnknown para liberar la interfaz. IUnknown es compatible con cada objeto de Programador de tareas.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Inicio Programador de tareas
- consideraciones de programación Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676533"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="4a0e7-107">Consideraciones de programación (Programador de tareas)</span><span class="sxs-lookup"><span data-stu-id="4a0e7-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="4a0e7-108">Al desarrollar aplicaciones que usan el Programador de tareas 1,0, tenga en cuenta los siguientes problemas de programación.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="4a0e7-109">La aplicación debe asegurarse de que el servicio de Programador de tareas se está ejecutando antes de intentar realizar llamadas mediante la API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="4a0e7-110">Al recuperar cadenas, asegúrese de llamar a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar cada cadena una vez que ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="4a0e7-111">Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="4a0e7-112">Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo en el disco.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="4a0e7-113">Después de usar cualquiera de las interfaces proporcionadas por el Programador de tareas API, asegúrese de llamar a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="4a0e7-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es compatible con cada objeto de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="4a0e7-115">La sección uso de la documentación Programador de tareas proporciona numerosos ejemplos que siguen estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="4a0e7-116">En la tabla siguiente se proporcionan saltos a algunos de estos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="4a0e7-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="4a0e7-117">Para obtener un ejemplo de</span><span class="sxs-lookup"><span data-stu-id="4a0e7-117">For an example of</span></span>         | <span data-ttu-id="4a0e7-118">Vea</span><span class="sxs-lookup"><span data-stu-id="4a0e7-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0e7-119">Liberar cadenas</span><span class="sxs-lookup"><span data-stu-id="4a0e7-119">Releasing strings</span></span>         | [<span data-ttu-id="4a0e7-120">Recuperar ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="4a0e7-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="4a0e7-121">Guardar elementos de trabajo en el disco</span><span class="sxs-lookup"><span data-stu-id="4a0e7-121">Saving work items to disk</span></span> | [<span data-ttu-id="4a0e7-122">Configuración de ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="4a0e7-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="4a0e7-123">Liberar interfaces</span><span class="sxs-lookup"><span data-stu-id="4a0e7-123">Releasing interfaces</span></span>      | [<span data-ttu-id="4a0e7-124">Crear una tarea mediante el ejemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="4a0e7-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 
