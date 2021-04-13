---
title: Tipo complejo de weeklyScheduleType
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- tipo complejo de weeklyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422158"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="e0284-104">Tipo complejo de weeklyScheduleType</span><span class="sxs-lookup"><span data-stu-id="e0284-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="e0284-105">Define los elementos secundarios y la información de secuenciación para el elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e0284-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e0284-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0284-106">Child elements</span></span>



| <span data-ttu-id="e0284-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e0284-107">Element</span></span>                                                                               | <span data-ttu-id="e0284-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0284-108">Type</span></span>                                                                     | <span data-ttu-id="e0284-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0284-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="e0284-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e0284-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="e0284-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="e0284-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="e0284-112">Especifica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="e0284-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="e0284-113">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="e0284-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="e0284-114">Especifica el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="e0284-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e0284-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0284-115">Requirements</span></span>



| <span data-ttu-id="e0284-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0284-116">Requirement</span></span> | <span data-ttu-id="e0284-117">Value</span><span class="sxs-lookup"><span data-stu-id="e0284-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0284-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0284-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0284-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0284-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0284-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0284-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0284-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0284-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0284-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0284-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0284-123">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e0284-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





