---
title: Elemento Delay (registrationTriggerType)
description: Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803985"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="b9c8d-104">Elemento Delay (registrationTriggerType)</span><span class="sxs-lookup"><span data-stu-id="b9c8d-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="b9c8d-105">Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9c8d-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="b9c8d-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="b9c8d-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="b9c8d-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="b9c8d-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="b9c8d-108">El elemento **Delay** se define mediante el tipo complejo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c8d-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b9c8d-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b9c8d-109">Parent element</span></span>



| <span data-ttu-id="b9c8d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9c8d-110">Element</span></span>                                                                                     | <span data-ttu-id="b9c8d-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b9c8d-111">Derived from</span></span>                                                                               | <span data-ttu-id="b9c8d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9c8d-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b9c8d-113">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="b9c8d-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="b9c8d-114">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b9c8d-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="b9c8d-115">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9c8d-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9c8d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9c8d-116">Remarks</span></span>

<span data-ttu-id="b9c8d-117">Para el desarrollo de scripting, el retraso del desencadenador de registro se especifica mediante la propiedad [**RegistrationTrigger. Delay**](registrationtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c8d-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="b9c8d-118">En el desarrollo de C++, el retraso del desencadenador de registro se especifica mediante la propiedad [**IRegistrationTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="b9c8d-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b9c8d-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9c8d-119">Examples</span></span>

<span data-ttu-id="b9c8d-120">El siguiente código XML define un retraso del desencadenador de registro que permite un retraso de 5 minutos entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9c8d-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="b9c8d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9c8d-121">Requirements</span></span>



| <span data-ttu-id="b9c8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c8d-122">Requirement</span></span> | <span data-ttu-id="b9c8d-123">Value</span><span class="sxs-lookup"><span data-stu-id="b9c8d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9c8d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9c8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c8d-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b9c8d-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9c8d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9c8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c8d-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9c8d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9c8d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9c8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c8d-129">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b9c8d-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b9c8d-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b9c8d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





