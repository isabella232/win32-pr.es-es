---
title: Elemento Task
description: Define la tarea que realiza el servicio Programador de tareas.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Programador de tareas del elemento Task
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905086"
---
# <a name="task-element"></a><span data-ttu-id="ce6ea-104">Elemento Task</span><span class="sxs-lookup"><span data-stu-id="ce6ea-104">Task Element</span></span>

<span data-ttu-id="ce6ea-105">Define la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="ce6ea-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce6ea-106">Child elements</span></span>



| <span data-ttu-id="ce6ea-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce6ea-107">Element</span></span>                                                                           | <span data-ttu-id="ce6ea-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce6ea-108">Type</span></span>                                                                                 | <span data-ttu-id="ce6ea-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce6ea-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce6ea-110">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="ce6ea-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="ce6ea-112">Especifica las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="ce6ea-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="ce6ea-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="ce6ea-115">Especifica los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="ce6ea-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="ce6ea-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="ce6ea-118">Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="ce6ea-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="ce6ea-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="ce6ea-121">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="ce6ea-122">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="ce6ea-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="ce6ea-124">Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="ce6ea-125">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="ce6ea-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="ce6ea-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="ce6ea-127">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="ce6ea-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="ce6ea-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce6ea-128">Remarks</span></span>

<span data-ttu-id="ce6ea-129">Para el desarrollo de C++, vea [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="ce6ea-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="ce6ea-130">Para el desarrollo de scripts, vea [**TaskDefinition**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce6ea-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6ea-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce6ea-131">Requirements</span></span>



| <span data-ttu-id="ce6ea-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce6ea-132">Requirement</span></span> | <span data-ttu-id="ce6ea-133">Value</span><span class="sxs-lookup"><span data-stu-id="ce6ea-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce6ea-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6ea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6ea-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce6ea-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce6ea-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce6ea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6ea-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce6ea-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





