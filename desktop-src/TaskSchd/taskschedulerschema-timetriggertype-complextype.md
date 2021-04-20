---
title: tipo complejo timeTriggerType
description: Define el tipo base para el elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Tipo complejo timeTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734140"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="2a1b3-104">tipo complejo timeTriggerType</span><span class="sxs-lookup"><span data-stu-id="2a1b3-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="2a1b3-105">Define el tipo base para el [**elemento TimeTrigger.**](taskschedulerschema-timetrigger-triggergroup-element.md)</span><span class="sxs-lookup"><span data-stu-id="2a1b3-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="2a1b3-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a1b3-106">Child elements</span></span>



| <span data-ttu-id="2a1b3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2a1b3-107">Element</span></span>                                                                        | <span data-ttu-id="2a1b3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a1b3-108">Type</span></span>     | <span data-ttu-id="2a1b3-109">Description</span><span class="sxs-lookup"><span data-stu-id="2a1b3-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a1b3-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="2a1b3-111">duration</span><span class="sxs-lookup"><span data-stu-id="2a1b3-111">duration</span></span> | <span data-ttu-id="2a1b3-112">Especifica el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="2a1b3-113">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="2a1b3-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="2a1b3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a1b3-114">Remarks</span></span>

<span data-ttu-id="2a1b3-115">Tenga en cuenta que este elemento no agrega ningún elemento secundario a los definidos por el tipo complejo [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="2a1b3-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a1b3-116">Requirements</span></span>



| <span data-ttu-id="2a1b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1b3-117">Requirement</span></span> | <span data-ttu-id="2a1b3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2a1b3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a1b3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a1b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1b3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a1b3-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a1b3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a1b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1b3-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a1b3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a1b3-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a1b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1b3-124">Programador de tareas tipos complejos de esquema</span><span class="sxs-lookup"><span data-stu-id="2a1b3-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="2a1b3-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2a1b3-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





