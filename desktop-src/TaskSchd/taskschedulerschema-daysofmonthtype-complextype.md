---
title: Tipo complejo de daysOfMonthType
description: Define el elemento secundario y la información de secuenciación para el elemento DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- tipo complejo de daysOfMonthType Programador de tareas
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422520"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="67446-104">Tipo complejo de daysOfMonthType</span><span class="sxs-lookup"><span data-stu-id="67446-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="67446-105">Define el elemento secundario y la información de secuenciación para el elemento [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="67446-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="67446-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67446-106">Child elements</span></span>



| <span data-ttu-id="67446-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="67446-107">Element</span></span>                                                        | <span data-ttu-id="67446-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="67446-108">Type</span></span>                                                                    | <span data-ttu-id="67446-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="67446-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="67446-110">**Diariamente**</span><span class="sxs-lookup"><span data-stu-id="67446-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="67446-111">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="67446-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="67446-112">Especifica un día del mes durante el que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="67446-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="67446-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67446-113">Requirements</span></span>



| <span data-ttu-id="67446-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67446-114">Requirement</span></span> | <span data-ttu-id="67446-115">Value</span><span class="sxs-lookup"><span data-stu-id="67446-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67446-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67446-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67446-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67446-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67446-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67446-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67446-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67446-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67446-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="67446-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67446-121">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="67446-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="67446-122">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="67446-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





