---
title: Elemento Delay (bootTriggerType)
description: Especifica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997129"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="6edf0-104">Elemento Delay (bootTriggerType)</span><span class="sxs-lookup"><span data-stu-id="6edf0-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="6edf0-105">Especifica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="6edf0-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="6edf0-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="6edf0-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6edf0-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="6edf0-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="6edf0-108">El elemento **Delay** se define mediante el tipo complejo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6edf0-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6edf0-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6edf0-109">Parent element</span></span>



| <span data-ttu-id="6edf0-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="6edf0-110">Element</span></span>                                                                     | <span data-ttu-id="6edf0-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6edf0-111">Derived from</span></span>                                                               | <span data-ttu-id="6edf0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6edf0-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="6edf0-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="6edf0-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="6edf0-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="6edf0-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="6edf0-115">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="6edf0-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6edf0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6edf0-116">Remarks</span></span>

<span data-ttu-id="6edf0-117">Para el desarrollo de scripts, el retraso del desencadenador de eventos se especifica mediante la propiedad [**BootTrigger. Delay**](boottrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="6edf0-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="6edf0-118">En el desarrollo de C++, el retraso del desencadenador de eventos se especifica mediante la propiedad [**IBootTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="6edf0-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edf0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6edf0-119">Requirements</span></span>



| <span data-ttu-id="6edf0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edf0-120">Requirement</span></span> | <span data-ttu-id="6edf0-121">Value</span><span class="sxs-lookup"><span data-stu-id="6edf0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6edf0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edf0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6edf0-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6edf0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6edf0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edf0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6edf0-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6edf0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6edf0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6edf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edf0-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="6edf0-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6edf0-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6edf0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





