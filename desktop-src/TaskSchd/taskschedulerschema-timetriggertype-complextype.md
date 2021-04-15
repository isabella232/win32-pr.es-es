---
title: Tipo complejo de timeTriggerType
description: Define el tipo base para el elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- tipo complejo de timeTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676622"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="6a5ca-104">Tipo complejo de timeTriggerType</span><span class="sxs-lookup"><span data-stu-id="6a5ca-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="6a5ca-105">Define el tipo base para el elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6a5ca-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6a5ca-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a5ca-106">Child elements</span></span>



| <span data-ttu-id="6a5ca-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a5ca-107">Element</span></span>                                                                        | <span data-ttu-id="6a5ca-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a5ca-108">Type</span></span>     | <span data-ttu-id="6a5ca-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a5ca-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a5ca-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="6a5ca-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="6a5ca-111">duration</span><span class="sxs-lookup"><span data-stu-id="6a5ca-111">duration</span></span> | <span data-ttu-id="6a5ca-112">Especifica el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a5ca-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="6a5ca-113">El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="6a5ca-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a5ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a5ca-114">Remarks</span></span>

<span data-ttu-id="6a5ca-115">Tenga en cuenta que este elemento no agrega ningún elemento secundario a los definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a5ca-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a5ca-116">Requirements</span></span>



| <span data-ttu-id="6a5ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a5ca-117">Requirement</span></span> | <span data-ttu-id="6a5ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="6a5ca-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a5ca-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a5ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5ca-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a5ca-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a5ca-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a5ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5ca-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a5ca-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a5ca-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a5ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5ca-124">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6a5ca-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6a5ca-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6a5ca-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





