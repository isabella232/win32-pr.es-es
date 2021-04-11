---
title: Months (monthlyScheduleType), elemento
description: Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Months, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150849"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="c299a-104">Months (monthlyScheduleType), elemento</span><span class="sxs-lookup"><span data-stu-id="c299a-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="c299a-105">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="c299a-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="c299a-106">El elemento **months** se define mediante el tipo complejo [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c299a-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c299a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c299a-107">Parent element</span></span>



| <span data-ttu-id="c299a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c299a-108">Element</span></span>                                                                                    | <span data-ttu-id="c299a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c299a-109">Derived from</span></span>                                                                       | <span data-ttu-id="c299a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c299a-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="c299a-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="c299a-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="c299a-112">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="c299a-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="c299a-113">Especifica una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="c299a-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c299a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c299a-114">Child elements</span></span>



| <span data-ttu-id="c299a-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c299a-115">Element</span></span>                                                                            | <span data-ttu-id="c299a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c299a-116">Type</span></span> | <span data-ttu-id="c299a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c299a-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="c299a-118">**Abril (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="c299a-119">Especifica que la tarea se ejecuta en abril.</span><span class="sxs-lookup"><span data-stu-id="c299a-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="c299a-120">**Agosto (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="c299a-121">Especifica que la tarea se ejecuta en agosto.</span><span class="sxs-lookup"><span data-stu-id="c299a-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="c299a-122">**Diciembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="c299a-123">Especifica que la tarea se ejecuta en diciembre.</span><span class="sxs-lookup"><span data-stu-id="c299a-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="c299a-124">**Febrero (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="c299a-125">Especifica que la tarea se ejecuta en febrero.</span><span class="sxs-lookup"><span data-stu-id="c299a-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="c299a-126">**Enero (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="c299a-127">Especifica que la tarea se ejecuta en enero.</span><span class="sxs-lookup"><span data-stu-id="c299a-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="c299a-128">**Julio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="c299a-129">Especifica que la tarea se ejecuta en julio.</span><span class="sxs-lookup"><span data-stu-id="c299a-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="c299a-130">**Junio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="c299a-131">Especifica que la tarea se ejecuta en junio.</span><span class="sxs-lookup"><span data-stu-id="c299a-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="c299a-132">**Marzo (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="c299a-133">Especifica que la tarea se ejecuta en marzo.</span><span class="sxs-lookup"><span data-stu-id="c299a-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="c299a-134">**Mayo (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="c299a-135">Especifica que la tarea se ejecuta en mayo.</span><span class="sxs-lookup"><span data-stu-id="c299a-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="c299a-136">**Noviembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="c299a-137">Especifica que la tarea se ejecuta en noviembre.</span><span class="sxs-lookup"><span data-stu-id="c299a-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="c299a-138">**Octubre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="c299a-139">Especifica que la tarea se ejecuta en octubre.</span><span class="sxs-lookup"><span data-stu-id="c299a-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="c299a-140">**Septiembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="c299a-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="c299a-141">Especifica que la tarea se ejecuta en septiembre.</span><span class="sxs-lookup"><span data-stu-id="c299a-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c299a-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c299a-142">Remarks</span></span>

<span data-ttu-id="c299a-143">Para el desarrollo de scripts, los meses de la programación se especifican mediante la propiedad [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="c299a-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="c299a-144">En el desarrollo de C++, los meses de la programación se especifican mediante la propiedad [**IMonthlyTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="c299a-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c299a-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c299a-145">Examples</span></span>

<span data-ttu-id="c299a-146">El siguiente código XML define un calendario mensual que inicia la tarea el día 1 y 15 de cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="c299a-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a><span data-ttu-id="c299a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c299a-147">Requirements</span></span>



| <span data-ttu-id="c299a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c299a-148">Requirement</span></span> | <span data-ttu-id="c299a-149">Value</span><span class="sxs-lookup"><span data-stu-id="c299a-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c299a-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c299a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c299a-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c299a-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c299a-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c299a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c299a-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c299a-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c299a-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="c299a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c299a-155">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c299a-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c299a-156">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c299a-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





