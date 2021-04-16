---
title: Tipo complejo de eventTriggerType
description: Define los elementos secundarios y la información de secuenciación para el elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- tipo complejo de eventTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686100"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="b8456-104">Tipo complejo de eventTriggerType</span><span class="sxs-lookup"><span data-stu-id="b8456-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="b8456-105">Define los elementos secundarios y la información de secuenciación para el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b8456-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b8456-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8456-106">Child elements</span></span>



| <span data-ttu-id="b8456-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8456-107">Element</span></span>                                                                           | <span data-ttu-id="b8456-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8456-108">Type</span></span>                                                                    | <span data-ttu-id="b8456-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8456-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8456-110">**Delay**</span><span class="sxs-lookup"><span data-stu-id="b8456-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="b8456-111">duration</span><span class="sxs-lookup"><span data-stu-id="b8456-111">duration</span></span>                                                                | <span data-ttu-id="b8456-112">Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8456-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="b8456-113">**Subscription**</span><span class="sxs-lookup"><span data-stu-id="b8456-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="b8456-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="b8456-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="b8456-115">Especifica la consulta XPath que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b8456-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="b8456-116">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="b8456-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="b8456-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="b8456-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="b8456-118">Especifica una secuencia de elementos que contienen un nombre y un valor de consulta XPath.</span><span class="sxs-lookup"><span data-stu-id="b8456-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="b8456-119">Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el elemento [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b8456-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="b8456-120">El nombre del valor de consulta XPath se puede usar como una variable en el elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) de la sección de acción [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) de una tarea.</span><span class="sxs-lookup"><span data-stu-id="b8456-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b8456-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8456-121">Remarks</span></span>

<span data-ttu-id="b8456-122">Además del elemento secundario que se define aquí, el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) también utiliza elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8456-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8456-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8456-123">Requirements</span></span>



| <span data-ttu-id="b8456-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8456-124">Requirement</span></span> | <span data-ttu-id="b8456-125">Value</span><span class="sxs-lookup"><span data-stu-id="b8456-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8456-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8456-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b8456-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8456-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8456-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8456-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b8456-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8456-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8456-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8456-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8456-131">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b8456-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b8456-132">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b8456-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





