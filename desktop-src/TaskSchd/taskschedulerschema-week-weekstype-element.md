---
title: Elemento Week (weeksType)
description: Especifica una semana específica del mes.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Programador de tareas de elemento Week
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686186"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="67d6d-104">Elemento Week (weeksType)</span><span class="sxs-lookup"><span data-stu-id="67d6d-104">Week (weeksType) Element</span></span>

<span data-ttu-id="67d6d-105">Especifica una semana específica del mes.</span><span class="sxs-lookup"><span data-stu-id="67d6d-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="67d6d-106">El elemento **Week** se define mediante el tipo complejo [**weeksType**](taskschedulerschema-weekstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="67d6d-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="67d6d-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="67d6d-107">Parent element</span></span>



| <span data-ttu-id="67d6d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="67d6d-108">Element</span></span>                                                                                                        | <span data-ttu-id="67d6d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="67d6d-109">Derived from</span></span>                                                   | <span data-ttu-id="67d6d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="67d6d-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="67d6d-111">**Semanas (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="67d6d-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="67d6d-112">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="67d6d-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="67d6d-113">Especifica las semanas del mes en que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="67d6d-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="67d6d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67d6d-114">Remarks</span></span>

<span data-ttu-id="67d6d-115">Al especificar las semanas del mes, use los números 1-4 para las cuatro primeras semanas del mes o use la cadena "Last" para indicar la última semana del mes.</span><span class="sxs-lookup"><span data-stu-id="67d6d-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d6d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67d6d-116">Requirements</span></span>



| <span data-ttu-id="67d6d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="67d6d-117">Requirement</span></span> | <span data-ttu-id="67d6d-118">Value</span><span class="sxs-lookup"><span data-stu-id="67d6d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67d6d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67d6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="67d6d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67d6d-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67d6d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67d6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="67d6d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67d6d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67d6d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="67d6d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d6d-124">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="67d6d-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="67d6d-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="67d6d-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





