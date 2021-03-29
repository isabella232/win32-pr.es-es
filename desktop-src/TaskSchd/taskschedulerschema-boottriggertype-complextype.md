---
title: Tipo complejo de bootTriggerType
description: Define el elemento secundario y la información de secuenciación para el elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- tipo complejo de bootTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492083"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="c5ded-104">Tipo complejo de bootTriggerType</span><span class="sxs-lookup"><span data-stu-id="c5ded-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="c5ded-105">Define el elemento secundario y la información de secuenciación para el elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ded-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c5ded-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5ded-106">Child elements</span></span>



| <span data-ttu-id="c5ded-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5ded-107">Element</span></span>                                                            | <span data-ttu-id="c5ded-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5ded-108">Type</span></span>     | <span data-ttu-id="c5ded-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ded-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5ded-110">**Delay**</span><span class="sxs-lookup"><span data-stu-id="c5ded-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="c5ded-111">duration</span><span class="sxs-lookup"><span data-stu-id="c5ded-111">duration</span></span> | <span data-ttu-id="c5ded-112">Cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c5ded-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c5ded-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5ded-113">Remarks</span></span>

<span data-ttu-id="c5ded-114">Además del elemento secundario que se define aquí, el elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) también utiliza elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ded-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ded-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ded-115">Requirements</span></span>



| <span data-ttu-id="c5ded-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ded-116">Requirement</span></span> | <span data-ttu-id="c5ded-117">Value</span><span class="sxs-lookup"><span data-stu-id="c5ded-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5ded-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ded-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ded-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ded-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5ded-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ded-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ded-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ded-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5ded-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5ded-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ded-123">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c5ded-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c5ded-124">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c5ded-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





