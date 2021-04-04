---
title: Elemento SessionStateChangeTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se cambia el estado de una sesión de Terminal Server.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Programador de tareas del elemento SessionStateChangeTrigger
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803217"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="accc8-104">Elemento SessionStateChangeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="accc8-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="accc8-105">Especifica un desencadenador que inicia una tarea cuando se cambia el estado de una sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="accc8-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="accc8-106">El elemento **SessionStateChangeTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="accc8-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="accc8-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="accc8-107">Parent element</span></span>



| <span data-ttu-id="accc8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="accc8-108">Element</span></span>                                                           | <span data-ttu-id="accc8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="accc8-109">Derived from</span></span>                                                         | <span data-ttu-id="accc8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="accc8-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="accc8-111">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="accc8-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="accc8-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="accc8-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="accc8-113">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="accc8-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="accc8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="accc8-114">Child elements</span></span>



| <span data-ttu-id="accc8-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="accc8-115">Element</span></span>                                                                                      | <span data-ttu-id="accc8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="accc8-116">Type</span></span>                                                                                    | <span data-ttu-id="accc8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="accc8-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="accc8-118">**Delay**</span><span class="sxs-lookup"><span data-stu-id="accc8-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="accc8-119">duration</span><span class="sxs-lookup"><span data-stu-id="accc8-119">duration</span></span>                                                                                | <span data-ttu-id="accc8-120">Especifica un valor que indica la duración del retraso antes de que se inicie una tarea cuando se detecta un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="accc8-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="accc8-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="accc8-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="accc8-122">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="accc8-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="accc8-123">Especifica el tipo de Terminal Server cambio de sesión que desencadenaría el inicio de una tarea.</span><span class="sxs-lookup"><span data-stu-id="accc8-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="accc8-124">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="accc8-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="accc8-125">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="accc8-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="accc8-126">Especifica el usuario de la sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="accc8-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="accc8-127">Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.</span><span class="sxs-lookup"><span data-stu-id="accc8-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="accc8-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="accc8-128">Remarks</span></span>

<span data-ttu-id="accc8-129">Para el desarrollo de scripting, se especifica un desencadenador de cambio de estado de sesión mediante el objeto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="accc8-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="accc8-130">En el desarrollo de C++, se especifica un desencadenador de cambio de estado de sesión mediante la interfaz [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .</span><span class="sxs-lookup"><span data-stu-id="accc8-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="accc8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accc8-131">Requirements</span></span>



| <span data-ttu-id="accc8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="accc8-132">Requirement</span></span> | <span data-ttu-id="accc8-133">Value</span><span class="sxs-lookup"><span data-stu-id="accc8-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="accc8-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accc8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="accc8-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="accc8-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="accc8-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accc8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="accc8-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="accc8-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





