---
title: Tipo complejo de registrationTriggerType
description: Define elementos secundarios e información de secuenciación para el elemento RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- tipo complejo de registrationTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422483"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="345c8-104">Tipo complejo de registrationTriggerType</span><span class="sxs-lookup"><span data-stu-id="345c8-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="345c8-105">Define elementos secundarios e información de secuenciación para el elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="345c8-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="345c8-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="345c8-106">Child elements</span></span>



| <span data-ttu-id="345c8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="345c8-107">Element</span></span>                                                                    | <span data-ttu-id="345c8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="345c8-108">Type</span></span>     | <span data-ttu-id="345c8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="345c8-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="345c8-110">**Delay**</span><span class="sxs-lookup"><span data-stu-id="345c8-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="345c8-111">duration</span><span class="sxs-lookup"><span data-stu-id="345c8-111">duration</span></span> | <span data-ttu-id="345c8-112">Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="345c8-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="345c8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="345c8-113">Remarks</span></span>

<span data-ttu-id="345c8-114">Además de los elementos secundarios definidos aquí, el elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) también utiliza elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="345c8-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="345c8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345c8-115">Requirements</span></span>



| <span data-ttu-id="345c8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="345c8-116">Requirement</span></span> | <span data-ttu-id="345c8-117">Value</span><span class="sxs-lookup"><span data-stu-id="345c8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="345c8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="345c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="345c8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="345c8-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="345c8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="345c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="345c8-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="345c8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="345c8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="345c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345c8-123">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="345c8-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="345c8-124">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="345c8-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





