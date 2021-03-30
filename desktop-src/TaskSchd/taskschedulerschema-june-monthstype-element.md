---
title: Junio (monthsType), elemento
description: Especifica que la tarea se ejecuta en junio.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Programador de tareas del elemento de junio
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802966"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="898cd-104">Junio (monthsType), elemento</span><span class="sxs-lookup"><span data-stu-id="898cd-104">June (monthsType) Element</span></span>

<span data-ttu-id="898cd-105">Especifica que la tarea se ejecuta en junio.</span><span class="sxs-lookup"><span data-stu-id="898cd-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="898cd-106">El elemento de **junio** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="898cd-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="898cd-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="898cd-107">Parent element</span></span>



| <span data-ttu-id="898cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="898cd-108">Element</span></span>                                                                                                          | <span data-ttu-id="898cd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="898cd-109">Derived from</span></span>                                                     | <span data-ttu-id="898cd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="898cd-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="898cd-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="898cd-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="898cd-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="898cd-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="898cd-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="898cd-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="898cd-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="898cd-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="898cd-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="898cd-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="898cd-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="898cd-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="898cd-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="898cd-117">Examples</span></span>

<span data-ttu-id="898cd-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en junio.</span><span class="sxs-lookup"><span data-stu-id="898cd-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="898cd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="898cd-119">Requirements</span></span>



| <span data-ttu-id="898cd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="898cd-120">Requirement</span></span> | <span data-ttu-id="898cd-121">Value</span><span class="sxs-lookup"><span data-stu-id="898cd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="898cd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="898cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="898cd-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="898cd-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="898cd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="898cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="898cd-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="898cd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="898cd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="898cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="898cd-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="898cd-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="898cd-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="898cd-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





