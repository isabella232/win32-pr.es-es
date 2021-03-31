---
title: Elemento de entidades de seguridad (taskType)
description: Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento de entidades de seguridad Programador de tareas
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996030"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="8b9b9-104">Elemento de entidades de seguridad (taskType)</span><span class="sxs-lookup"><span data-stu-id="8b9b9-104">Principals (taskType) Element</span></span>

<span data-ttu-id="8b9b9-105">Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b9b9-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="8b9b9-106">El elemento de **entidades** de seguridad se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8b9b9-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8b9b9-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8b9b9-107">Parent element</span></span>



| <span data-ttu-id="8b9b9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b9b9-108">Element</span></span>                                          | <span data-ttu-id="8b9b9-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8b9b9-109">Derived from</span></span>                                                 | <span data-ttu-id="8b9b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b9b9-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="8b9b9-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="8b9b9-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="8b9b9-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="8b9b9-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="8b9b9-113">Define la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8b9b9-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="8b9b9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b9b9-114">Child elements</span></span>



| <span data-ttu-id="8b9b9-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b9b9-115">Element</span></span>                                                                  | <span data-ttu-id="8b9b9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b9b9-116">Type</span></span>                                                                   | <span data-ttu-id="8b9b9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b9b9-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8b9b9-118">**Principal**</span><span class="sxs-lookup"><span data-stu-id="8b9b9-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="8b9b9-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="8b9b9-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="8b9b9-120">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8b9b9-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8b9b9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b9b9-121">Remarks</span></span>

<span data-ttu-id="8b9b9-122">Puede especificar hasta 32 entidades de seguridad para una tarea.</span><span class="sxs-lookup"><span data-stu-id="8b9b9-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="8b9b9-123">Para el desarrollo de scripting, las entidades de seguridad de una tarea se especifican mediante la propiedad [**TaskDefinition. principal**](taskdefinition-principal.md) .</span><span class="sxs-lookup"><span data-stu-id="8b9b9-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="8b9b9-124">En el desarrollo de C++, las entidades de seguridad de una tarea se especifican mediante la [**propiedad principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span><span class="sxs-lookup"><span data-stu-id="8b9b9-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="8b9b9-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b9b9-125">Examples</span></span>

<span data-ttu-id="8b9b9-126">En el código XML siguiente se definen dos entidades de seguridad: un identificador de usuario y una entidad de seguridad de identificador de grupo para la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b9b9-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="8b9b9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9b9-127">Requirements</span></span>



| <span data-ttu-id="8b9b9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9b9-128">Requirement</span></span> | <span data-ttu-id="8b9b9-129">Value</span><span class="sxs-lookup"><span data-stu-id="8b9b9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b9b9-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9b9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9b9-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b9b9-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8b9b9-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9b9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9b9-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b9b9-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b9b9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b9b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9b9-135">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8b9b9-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8b9b9-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8b9b9-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





