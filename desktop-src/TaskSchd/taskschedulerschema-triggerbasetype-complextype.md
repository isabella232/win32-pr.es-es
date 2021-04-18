---
title: Tipo complejo de triggerBaseType
description: Define el atributo, los elementos secundarios base y la información de secuenciación de todos los tipos de desencadenadores complejos.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- tipo complejo de triggerBaseType Programador de tareas
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359857"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="80b4e-104">Tipo complejo de triggerBaseType</span><span class="sxs-lookup"><span data-stu-id="80b4e-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="80b4e-105">Define el atributo, los elementos secundarios base y la información de secuenciación de todos los tipos de desencadenadores complejos.</span><span class="sxs-lookup"><span data-stu-id="80b4e-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="80b4e-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="80b4e-106">Child elements</span></span>



| <span data-ttu-id="80b4e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="80b4e-107">Element</span></span>                                                                                      | <span data-ttu-id="80b4e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="80b4e-108">Type</span></span>                                                                     | <span data-ttu-id="80b4e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="80b4e-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80b4e-110">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="80b4e-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="80b4e-111">boolean</span><span class="sxs-lookup"><span data-stu-id="80b4e-111">boolean</span></span>                                                                  | <span data-ttu-id="80b4e-112">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80b4e-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="80b4e-113">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="80b4e-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="80b4e-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="80b4e-114">dateTime</span></span>                                                                 | <span data-ttu-id="80b4e-115">Fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="80b4e-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="80b4e-116">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="80b4e-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="80b4e-117">duration</span><span class="sxs-lookup"><span data-stu-id="80b4e-117">duration</span></span>                                                                 | <span data-ttu-id="80b4e-118">Especifica el intervalo en el que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="80b4e-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="80b4e-119">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="80b4e-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="80b4e-120">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="80b4e-121">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="80b4e-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="80b4e-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="80b4e-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="80b4e-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="80b4e-123">dateTime</span></span>                                                                 | <span data-ttu-id="80b4e-124">Fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="80b4e-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="80b4e-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="80b4e-125">Attributes</span></span>



| <span data-ttu-id="80b4e-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="80b4e-126">Name</span></span> | <span data-ttu-id="80b4e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="80b4e-127">Type</span></span> | <span data-ttu-id="80b4e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="80b4e-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="80b4e-129">id</span><span class="sxs-lookup"><span data-stu-id="80b4e-129">id</span></span>   | <span data-ttu-id="80b4e-130">id</span><span class="sxs-lookup"><span data-stu-id="80b4e-130">ID</span></span>   | <span data-ttu-id="80b4e-131">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="80b4e-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80b4e-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80b4e-132">Remarks</span></span>

<span data-ttu-id="80b4e-133">Los tipos complejos de desencadenador incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="80b4e-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="80b4e-134">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-135">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-136">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-137">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-138">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-139">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="80b4e-140">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="80b4e-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="80b4e-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b4e-141">Requirements</span></span>



| <span data-ttu-id="80b4e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b4e-142">Requirement</span></span> | <span data-ttu-id="80b4e-143">Value</span><span class="sxs-lookup"><span data-stu-id="80b4e-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80b4e-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80b4e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="80b4e-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80b4e-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80b4e-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80b4e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="80b4e-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="80b4e-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80b4e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="80b4e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b4e-149">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="80b4e-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="80b4e-150">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="80b4e-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





