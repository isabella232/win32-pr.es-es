---
title: Elemento Interval (repetitionType)
description: Especifica la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Intervalo de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734200"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="1ce8e-104">Elemento Interval (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="1ce8e-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="1ce8e-105">Especifica la cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="1ce8e-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="1ce8e-106">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="1ce8e-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="1ce8e-107">El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="1ce8e-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1ce8e-108">El elemento se define mediante el [**tipo complejo repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8e-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1ce8e-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1ce8e-109">Parent element</span></span>



| <span data-ttu-id="1ce8e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="1ce8e-110">Element</span></span>                                                                      | <span data-ttu-id="1ce8e-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1ce8e-111">Derived from</span></span>                                                             | <span data-ttu-id="1ce8e-112">Description</span><span class="sxs-lookup"><span data-stu-id="1ce8e-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce8e-113">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="1ce8e-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="1ce8e-114">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="1ce8e-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="1ce8e-115">Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="1ce8e-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1ce8e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ce8e-116">Remarks</span></span>

<span data-ttu-id="1ce8e-117">Para el desarrollo de scripting, el intervalo del patrón de repetición se especifica mediante la [**propiedad RepetitionPattern.Interval.**](repetitionpattern-interval.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8e-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="1ce8e-118">Para el desarrollo de C++, el intervalo del patrón de repetición se especifica mediante la [**propiedad IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)</span><span class="sxs-lookup"><span data-stu-id="1ce8e-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1ce8e-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1ce8e-119">Examples</span></span>

<span data-ttu-id="1ce8e-120">Para obtener un ejemplo completo del XML para una tarea que usa un intervalo de repetición, vea [Ejemplo de desencadenador diario (XML).](daily-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8e-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce8e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ce8e-121">Requirements</span></span>



| <span data-ttu-id="1ce8e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce8e-122">Requirement</span></span> | <span data-ttu-id="1ce8e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce8e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ce8e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ce8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce8e-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ce8e-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ce8e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ce8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce8e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ce8e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ce8e-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ce8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce8e-129">Programador de tareas de esquema</span><span class="sxs-lookup"><span data-stu-id="1ce8e-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1ce8e-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="1ce8e-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





