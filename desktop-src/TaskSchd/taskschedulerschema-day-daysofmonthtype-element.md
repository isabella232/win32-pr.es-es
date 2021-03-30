---
title: Elemento Day (daysOfMonthType)
description: Especifica un día del mes durante el que se ejecuta la tarea.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Programador de tareas del elemento Day
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079100"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="b568e-104">Elemento Day (daysOfMonthType)</span><span class="sxs-lookup"><span data-stu-id="b568e-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="b568e-105">Especifica un día del mes durante el que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="b568e-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="b568e-106">El elemento **Day** se define mediante el tipo complejo [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b568e-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b568e-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b568e-107">Parent element</span></span>



| <span data-ttu-id="b568e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b568e-108">Element</span></span>                                                                            | <span data-ttu-id="b568e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b568e-109">Derived from</span></span>                                                               | <span data-ttu-id="b568e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b568e-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="b568e-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="b568e-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="b568e-112">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="b568e-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="b568e-113">Especifica los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="b568e-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="b568e-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b568e-114">Examples</span></span>

<span data-ttu-id="b568e-115">El siguiente código XML define la parte correspondiente a los días de un calendario mensual que ejecuta la tarea el día 1 y el 15 del mes.</span><span class="sxs-lookup"><span data-stu-id="b568e-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="b568e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b568e-116">Requirements</span></span>



| <span data-ttu-id="b568e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b568e-117">Requirement</span></span> | <span data-ttu-id="b568e-118">Value</span><span class="sxs-lookup"><span data-stu-id="b568e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b568e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b568e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b568e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b568e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b568e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b568e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b568e-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b568e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b568e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b568e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b568e-124">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b568e-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





