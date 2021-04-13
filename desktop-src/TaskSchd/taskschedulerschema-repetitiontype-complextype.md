---
title: Tipo complejo de repetitionType
description: Define los elementos secundarios y la información de secuencia para el elemento repite (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- tipo complejo de repetitionType Programador de tareas
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422482"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="7e206-104">Tipo complejo de repetitionType</span><span class="sxs-lookup"><span data-stu-id="7e206-104">repetitionType Complex Type</span></span>

<span data-ttu-id="7e206-105">Define los elementos secundarios y la información de secuencia para el elemento [**repite (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7e206-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
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
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7e206-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e206-106">Child elements</span></span>



| <span data-ttu-id="7e206-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e206-107">Element</span></span>                                                                                   | <span data-ttu-id="7e206-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e206-108">Type</span></span>    | <span data-ttu-id="7e206-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e206-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e206-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="7e206-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="7e206-111">Especifica cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="7e206-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="7e206-112">Si no se especifica ningún valor, el patrón se repite indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="7e206-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="7e206-113">**Interval**</span><span class="sxs-lookup"><span data-stu-id="7e206-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="7e206-114">Especifica la cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7e206-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="7e206-115">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="7e206-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="7e206-116">boolean</span><span class="sxs-lookup"><span data-stu-id="7e206-116">boolean</span></span> | <span data-ttu-id="7e206-117">Especifica que una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.</span><span class="sxs-lookup"><span data-stu-id="7e206-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="7e206-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e206-118">Requirements</span></span>



| <span data-ttu-id="7e206-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e206-119">Requirement</span></span> | <span data-ttu-id="7e206-120">Value</span><span class="sxs-lookup"><span data-stu-id="7e206-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e206-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e206-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e206-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e206-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e206-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e206-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e206-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e206-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e206-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e206-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e206-126">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7e206-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7e206-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7e206-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





