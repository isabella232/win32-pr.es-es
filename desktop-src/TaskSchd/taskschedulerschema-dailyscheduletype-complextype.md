---
title: Tipo complejo de dailyScheduleType
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- tipo complejo de dailyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686101"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="7a346-104">Tipo complejo de dailyScheduleType</span><span class="sxs-lookup"><span data-stu-id="7a346-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="7a346-105">Define los elementos secundarios y la información de secuenciación para el elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7a346-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7a346-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7a346-106">Child elements</span></span>



| <span data-ttu-id="7a346-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a346-107">Element</span></span>                                                                            | <span data-ttu-id="7a346-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a346-108">Type</span></span> | <span data-ttu-id="7a346-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a346-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="7a346-110">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="7a346-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="7a346-111">Especifica el intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="7a346-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7a346-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a346-112">Requirements</span></span>



| <span data-ttu-id="7a346-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a346-113">Requirement</span></span> | <span data-ttu-id="7a346-114">Value</span><span class="sxs-lookup"><span data-stu-id="7a346-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a346-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a346-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7a346-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a346-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a346-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a346-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7a346-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a346-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a346-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a346-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a346-120">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7a346-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7a346-121">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7a346-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





