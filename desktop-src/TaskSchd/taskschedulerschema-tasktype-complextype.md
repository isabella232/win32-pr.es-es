---
title: Tipo complejo de taskType (Programador de tareas)
description: Define los elementos secundarios y la información de secuenciación para el elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- tipo complejo de taskType Programador de tareas
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491668"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="06853-104">Tipo complejo de taskType</span><span class="sxs-lookup"><span data-stu-id="06853-104">taskType Complex Type</span></span>

<span data-ttu-id="06853-105">Define los elementos secundarios y la información de secuenciación para el elemento [**Task**](taskschedulerschema-task-element.md) .</span><span class="sxs-lookup"><span data-stu-id="06853-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="06853-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06853-106">Child elements</span></span>



| <span data-ttu-id="06853-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="06853-107">Element</span></span>                                                                           | <span data-ttu-id="06853-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="06853-108">Type</span></span>                                                                                 | <span data-ttu-id="06853-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="06853-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06853-110">**Acciones**</span><span class="sxs-lookup"><span data-stu-id="06853-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="06853-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="06853-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="06853-112">Especifica las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="06853-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="06853-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="06853-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06853-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="06853-115">Especifica los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="06853-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="06853-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="06853-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="06853-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="06853-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="06853-118">Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="06853-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="06853-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="06853-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="06853-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="06853-121">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="06853-122">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="06853-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="06853-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="06853-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="06853-124">Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="06853-125">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="06853-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="06853-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="06853-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="06853-127">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="06853-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="06853-128">Attributes</span></span>



| <span data-ttu-id="06853-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="06853-129">Name</span></span>    | <span data-ttu-id="06853-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="06853-130">Type</span></span>                                                              | <span data-ttu-id="06853-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="06853-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="06853-132">version</span><span class="sxs-lookup"><span data-stu-id="06853-132">version</span></span> | [<span data-ttu-id="06853-133">**versionType**</span><span class="sxs-lookup"><span data-stu-id="06853-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="06853-134">Especifica la versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="06853-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="06853-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06853-135">Requirements</span></span>



| <span data-ttu-id="06853-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="06853-136">Requirement</span></span> | <span data-ttu-id="06853-137">Value</span><span class="sxs-lookup"><span data-stu-id="06853-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06853-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06853-138">Minimum supported client</span></span><br/> | <span data-ttu-id="06853-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="06853-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06853-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06853-140">Minimum supported server</span></span><br/> | <span data-ttu-id="06853-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="06853-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06853-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="06853-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06853-143">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="06853-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="06853-144">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="06853-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





