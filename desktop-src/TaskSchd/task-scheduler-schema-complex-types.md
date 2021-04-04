---
title: Tipos complejos de esquema Programador de tareas
description: Esta sección contiene los tipos complejos que se usan para definir los elementos secundarios y los atributos utilizados por otros elementos. Esta información se proporciona a aquellos que desean ampliar el esquema de Programador de tareas.
ms.assetid: 1db9049d-f2c7-4dc1-b7f0-b25bec551bf3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32ef8a464b5a702530768a4317d431c5b8e52550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075670"
---
# <a name="task-scheduler-schema-complex-types"></a><span data-ttu-id="df90d-104">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df90d-104">Task Scheduler Schema Complex Types</span></span>

<span data-ttu-id="df90d-105">Esta sección contiene los tipos complejos que se usan para definir los elementos secundarios y los atributos utilizados por otros elementos.</span><span class="sxs-lookup"><span data-stu-id="df90d-105">This section contains the complex types used to define the child elements and attributes used by other elements.</span></span> <span data-ttu-id="df90d-106">Esta información se proporciona a aquellos que desean ampliar el esquema de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="df90d-106">This information is provided for those who want to extend the Task Scheduler schema.</span></span>

<span data-ttu-id="df90d-107">En los temas de esta sección se incluye una descripción de lo que proporciona el tipo complejo a los elementos definidos por el tipo. Cómo se define el tipo complejo en el XSD; los elementos secundarios o atributos que define; y comentarios que cubren circunstancias especiales.</span><span class="sxs-lookup"><span data-stu-id="df90d-107">The topics in this section include a description of what the complex type provides to those elements defined by the type; how the complex type is defined in the XSD; the child elements or attributes it defines; and remarks that cover special circumstances.</span></span>

-   [<span data-ttu-id="df90d-108">**actionBaseType**</span><span class="sxs-lookup"><span data-stu-id="df90d-108">**actionBaseType**</span></span>](taskschedulerschema-actionbasetype-complextype.md)
-   [<span data-ttu-id="df90d-109">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-109">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)
-   [<span data-ttu-id="df90d-110">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-110">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)
-   [<span data-ttu-id="df90d-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="df90d-112">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-112">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="df90d-113">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-113">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)
-   [<span data-ttu-id="df90d-114">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="df90d-114">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)
-   [<span data-ttu-id="df90d-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df90d-115">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)
-   [<span data-ttu-id="df90d-116">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="df90d-116">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md)
-   [<span data-ttu-id="df90d-117">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="df90d-117">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md)
-   [<span data-ttu-id="df90d-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="df90d-119">**execType**</span><span class="sxs-lookup"><span data-stu-id="df90d-119">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)
-   [<span data-ttu-id="df90d-120">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-120">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md)
-   [<span data-ttu-id="df90d-121">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="df90d-121">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md)
-   [<span data-ttu-id="df90d-122">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-122">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)
-   [<span data-ttu-id="df90d-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="df90d-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="df90d-125">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="df90d-125">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)
-   [<span data-ttu-id="df90d-126">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="df90d-126">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)
-   [<span data-ttu-id="df90d-127">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-127">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)
-   [<span data-ttu-id="df90d-128">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="df90d-128">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)
-   [<span data-ttu-id="df90d-129">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-129">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)
-   [<span data-ttu-id="df90d-130">**namedValue**</span><span class="sxs-lookup"><span data-stu-id="df90d-130">**namedValue**</span></span>](schema-namedvalue-complextype.md)
-   [<span data-ttu-id="df90d-131">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-131">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)
-   [<span data-ttu-id="df90d-132">**principalType**</span><span class="sxs-lookup"><span data-stu-id="df90d-132">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md)
-   [<span data-ttu-id="df90d-133">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="df90d-133">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md)
-   [<span data-ttu-id="df90d-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="df90d-135">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="df90d-135">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)
-   [<span data-ttu-id="df90d-136">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="df90d-136">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md)
-   [<span data-ttu-id="df90d-137">**restartType**</span><span class="sxs-lookup"><span data-stu-id="df90d-137">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)
-   [<span data-ttu-id="df90d-138">**sendMailType**</span><span class="sxs-lookup"><span data-stu-id="df90d-138">**sendMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)
-   [<span data-ttu-id="df90d-139">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-139">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md)
-   [<span data-ttu-id="df90d-140">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="df90d-140">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)
-   [<span data-ttu-id="df90d-141">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="df90d-141">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md)
-   [<span data-ttu-id="df90d-142">**taskType**</span><span class="sxs-lookup"><span data-stu-id="df90d-142">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
-   [<span data-ttu-id="df90d-143">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="df90d-143">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)
-   [<span data-ttu-id="df90d-144">**triggerBaseType**</span><span class="sxs-lookup"><span data-stu-id="df90d-144">**triggerBaseType**</span></span>](taskschedulerschema-triggerbasetype-complextype.md)
-   [<span data-ttu-id="df90d-145">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="df90d-145">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)
-   [<span data-ttu-id="df90d-146">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="df90d-146">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)
-   [<span data-ttu-id="df90d-147">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="df90d-147">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)

## <a name="related-topics"></a><span data-ttu-id="df90d-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df90d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df90d-149">Referencia de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df90d-149">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> <dt>

[<span data-ttu-id="df90d-150">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df90d-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




