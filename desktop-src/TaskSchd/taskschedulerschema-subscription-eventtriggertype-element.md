---
title: Elemento subscription (eventTriggerType)
description: Especifica la consulta XPath que identifica el evento que activa el desencadenador.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Elemento subscription Programador de tareas
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803974"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="5d572-104">Elemento subscription (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="5d572-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="5d572-105">Especifica la consulta XPath que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="5d572-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="5d572-106">El tipo complejo [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) define el elemento **subscription** .</span><span class="sxs-lookup"><span data-stu-id="5d572-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5d572-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5d572-107">Parent element</span></span>



| <span data-ttu-id="5d572-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5d572-108">Element</span></span>                                                                       | <span data-ttu-id="5d572-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5d572-109">Derived from</span></span>                                                                 | <span data-ttu-id="5d572-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d572-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5d572-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="5d572-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="5d572-112">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5d572-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="5d572-113">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d572-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5d572-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d572-114">Remarks</span></span>

<span data-ttu-id="5d572-115">Para el desarrollo de scripts, la suscripción de eventos se especifica mediante la propiedad [**EventTrigger. subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="5d572-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="5d572-116">En el desarrollo de C++, la suscripción de eventos se especifica mediante la propiedad [**IEventTrigger:: subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .</span><span class="sxs-lookup"><span data-stu-id="5d572-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d572-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d572-117">Requirements</span></span>



| <span data-ttu-id="5d572-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d572-118">Requirement</span></span> | <span data-ttu-id="5d572-119">Value</span><span class="sxs-lookup"><span data-stu-id="5d572-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d572-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d572-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d572-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5d572-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5d572-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d572-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d572-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d572-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d572-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d572-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d572-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5d572-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5d572-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5d572-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





