---
title: Elemento Delay (eventTriggerType)
description: Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Programador de tareas del elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676999"
---
# <a name="delay-eventtriggertype-element"></a><span data-ttu-id="c77e6-104">Elemento Delay (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="c77e6-104">Delay (eventTriggerType) Element</span></span>

<span data-ttu-id="c77e6-105">Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="c77e6-105">Specifies the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="c77e6-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="c77e6-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c77e6-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="c77e6-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="c77e6-108">El elemento **Delay** se define mediante el tipo complejo [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c77e6-108">The **Delay** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c77e6-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c77e6-109">Parent element</span></span>



| <span data-ttu-id="c77e6-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="c77e6-110">Element</span></span>                                                                       | <span data-ttu-id="c77e6-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c77e6-111">Derived from</span></span>                                                                 | <span data-ttu-id="c77e6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c77e6-112">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="c77e6-113">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c77e6-113">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="c77e6-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c77e6-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="c77e6-115">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="c77e6-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c77e6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c77e6-116">Remarks</span></span>

<span data-ttu-id="c77e6-117">Para el desarrollo de scripts, la propiedad [**EventTrigger. Delay**](eventtrigger-delay.md) especifica el retraso del desencadenador de eventos.</span><span class="sxs-lookup"><span data-stu-id="c77e6-117">For script development, the event trigger delay is specified by the [**EventTrigger.Delay**](eventtrigger-delay.md) property.</span></span>

<span data-ttu-id="c77e6-118">En el desarrollo de C++, el retraso del desencadenador de eventos se especifica mediante la propiedad [**IEventTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="c77e6-118">For C++ development, the event trigger delay is specified by the [**IEventTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c77e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c77e6-119">Requirements</span></span>



| <span data-ttu-id="c77e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c77e6-120">Requirement</span></span> | <span data-ttu-id="c77e6-121">Value</span><span class="sxs-lookup"><span data-stu-id="c77e6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c77e6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c77e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c77e6-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c77e6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c77e6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c77e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c77e6-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c77e6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c77e6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c77e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77e6-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c77e6-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c77e6-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c77e6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





