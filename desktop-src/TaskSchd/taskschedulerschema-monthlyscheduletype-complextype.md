---
title: Tipo complejo de monthlyScheduleType
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- tipo complejo de monthlyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685939"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="02148-104">Tipo complejo de monthlyScheduleType</span><span class="sxs-lookup"><span data-stu-id="02148-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="02148-105">Define los elementos secundarios y la información de secuenciación para el elemento [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="02148-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="02148-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02148-106">Child elements</span></span>



| <span data-ttu-id="02148-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="02148-107">Element</span></span>                                                                            | <span data-ttu-id="02148-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="02148-108">Type</span></span>                                                                       | <span data-ttu-id="02148-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="02148-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02148-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="02148-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="02148-111">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="02148-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="02148-112">Especifica los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="02148-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="02148-113">**Partir**</span><span class="sxs-lookup"><span data-stu-id="02148-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="02148-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="02148-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="02148-115">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="02148-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="02148-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02148-116">Requirements</span></span>



| <span data-ttu-id="02148-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="02148-117">Requirement</span></span> | <span data-ttu-id="02148-118">Value</span><span class="sxs-lookup"><span data-stu-id="02148-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02148-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02148-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02148-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="02148-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02148-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02148-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02148-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="02148-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02148-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="02148-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02148-124">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="02148-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="02148-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="02148-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





