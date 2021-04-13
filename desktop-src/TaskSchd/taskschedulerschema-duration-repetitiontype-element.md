---
title: Duration (repetitionType), elemento
description: Especifica cuánto tiempo se repite el patrón.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Elemento Duration Programador de tareas
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359863"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="53436-104">Duration (repetitionType), elemento</span><span class="sxs-lookup"><span data-stu-id="53436-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="53436-105">Especifica cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="53436-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="53436-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="53436-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="53436-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="53436-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="53436-108">Si no se especifica ningún valor para la duración, el patrón se repite indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="53436-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="53436-109">El valor mínimo es un minuto.</span><span class="sxs-lookup"><span data-stu-id="53436-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="53436-110">El elemento se define mediante el tipo complejo de [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="53436-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="53436-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="53436-111">Parent element</span></span>



| <span data-ttu-id="53436-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="53436-112">Element</span></span>                                                                      | <span data-ttu-id="53436-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="53436-113">Derived from</span></span>                                                             | <span data-ttu-id="53436-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="53436-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53436-115">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="53436-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="53436-116">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="53436-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="53436-117">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="53436-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="53436-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53436-118">Remarks</span></span>

<span data-ttu-id="53436-119">En el caso de las aplicaciones de scripting, la duración del patrón se especifica mediante la propiedad [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .</span><span class="sxs-lookup"><span data-stu-id="53436-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="53436-120">En el caso de las aplicaciones de C++, la duración del patrón se especifica mediante la propiedad [**IRepetitionPattern::D primario**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="53436-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="53436-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="53436-121">Examples</span></span>

<span data-ttu-id="53436-122">En el código XML siguiente se define un patrón de repetición para un desencadenador.</span><span class="sxs-lookup"><span data-stu-id="53436-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="53436-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53436-123">Requirements</span></span>



| <span data-ttu-id="53436-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53436-124">Requirement</span></span> | <span data-ttu-id="53436-125">Value</span><span class="sxs-lookup"><span data-stu-id="53436-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53436-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53436-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53436-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53436-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53436-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53436-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53436-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53436-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53436-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="53436-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53436-131">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="53436-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="53436-132">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="53436-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





