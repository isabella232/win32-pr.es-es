---
title: Elemento Data (taskType)
description: Define los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Programador de tareas de elementos de datos
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801771"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="d6cf6-104">Elemento Data (taskType)</span><span class="sxs-lookup"><span data-stu-id="d6cf6-104">Data (taskType) Element</span></span>

<span data-ttu-id="d6cf6-105">Define los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d6cf6-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="d6cf6-106">El elemento de **datos** se define mediante el tipo complejo de [**taskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d6cf6-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d6cf6-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d6cf6-107">Parent element</span></span>



| <span data-ttu-id="d6cf6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d6cf6-108">Element</span></span>                                          | <span data-ttu-id="d6cf6-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d6cf6-109">Derived from</span></span>                                                 | <span data-ttu-id="d6cf6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6cf6-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="d6cf6-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="d6cf6-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="d6cf6-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="d6cf6-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="d6cf6-113">Define la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d6cf6-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d6cf6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6cf6-114">Remarks</span></span>

<span data-ttu-id="d6cf6-115">Como ejemplo de este tipo de datos, el servicio Registros y alertas de rendimiento usa esta propiedad como contenedor de almacenamiento para la consulta de contador de rendimiento asociada a una tarea.</span><span class="sxs-lookup"><span data-stu-id="d6cf6-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="d6cf6-116">En el desarrollo de C++, los datos de una tarea se especifican mediante la [**propiedad data de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span><span class="sxs-lookup"><span data-stu-id="d6cf6-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="d6cf6-117">En el desarrollo de scripting, los datos de una tarea se especifican mediante la propiedad [**TaskDefinition. Data**](taskdefinition-data.md) .</span><span class="sxs-lookup"><span data-stu-id="d6cf6-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cf6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6cf6-118">Requirements</span></span>



| <span data-ttu-id="d6cf6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6cf6-119">Requirement</span></span> | <span data-ttu-id="d6cf6-120">Value</span><span class="sxs-lookup"><span data-stu-id="d6cf6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6cf6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6cf6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6cf6-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d6cf6-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6cf6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6cf6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6cf6-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6cf6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6cf6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6cf6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cf6-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="d6cf6-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d6cf6-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d6cf6-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





