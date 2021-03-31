---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una secuencia de elementos, cada uno de los cuales contiene un nombre y un valor de consulta XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Programador de tareas del elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996084"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="e85f0-104">Elemento ValueQueries (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="e85f0-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="e85f0-105">Contiene una secuencia de elementos, cada uno de los cuales contiene un nombre y un valor de consulta XPath.</span><span class="sxs-lookup"><span data-stu-id="e85f0-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="e85f0-106">Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el elemento [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e85f0-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="e85f0-107">El nombre del valor de consulta XPath se puede usar como una variable en la sección de acción de una tarea.</span><span class="sxs-lookup"><span data-stu-id="e85f0-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="e85f0-108">El elemento **ValueQueries** se define mediante el tipo complejo de [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e85f0-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e85f0-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e85f0-109">Parent element</span></span>



| <span data-ttu-id="e85f0-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e85f0-110">Element</span></span>                                                                                      | <span data-ttu-id="e85f0-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e85f0-111">Derived from</span></span>                                                                 | <span data-ttu-id="e85f0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e85f0-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="e85f0-113">**EventTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="e85f0-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="e85f0-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e85f0-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="e85f0-115">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="e85f0-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e85f0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e85f0-116">Remarks</span></span>

<span data-ttu-id="e85f0-117">Para el desarrollo de C++, consulte la [**propiedad ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="e85f0-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="e85f0-118">Para el desarrollo de scripts, consulte [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="e85f0-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e85f0-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e85f0-119">Examples</span></span>

<span data-ttu-id="e85f0-120">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de evento mediante este elemento, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e85f0-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e85f0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85f0-121">Requirements</span></span>



| <span data-ttu-id="e85f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85f0-122">Requirement</span></span> | <span data-ttu-id="e85f0-123">Value</span><span class="sxs-lookup"><span data-stu-id="e85f0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e85f0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e85f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e85f0-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e85f0-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e85f0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e85f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e85f0-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e85f0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

