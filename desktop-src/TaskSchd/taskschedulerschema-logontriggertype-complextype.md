---
title: Tipo complejo de logonTriggerType
description: Define los elementos secundarios y la información de secuenciación para el elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- tipo complejo de logonTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686228"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="60ee7-104">Tipo complejo de logonTriggerType</span><span class="sxs-lookup"><span data-stu-id="60ee7-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="60ee7-105">Define los elementos secundarios y la información de secuenciación para el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="60ee7-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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

## <a name="child-elements"></a><span data-ttu-id="60ee7-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60ee7-106">Child elements</span></span>



| <span data-ttu-id="60ee7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="60ee7-107">Element</span></span>                                                               | <span data-ttu-id="60ee7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="60ee7-108">Type</span></span>                                                                    | <span data-ttu-id="60ee7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="60ee7-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60ee7-110">**Delay**</span><span class="sxs-lookup"><span data-stu-id="60ee7-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="60ee7-111">duration</span><span class="sxs-lookup"><span data-stu-id="60ee7-111">duration</span></span>                                                                | <span data-ttu-id="60ee7-112">Cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="60ee7-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="60ee7-113">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="60ee7-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="60ee7-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="60ee7-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="60ee7-115">Identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="60ee7-115">Identifier of the user.</span></span> <span data-ttu-id="60ee7-116">La tarea se inicia cuando este usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="60ee7-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60ee7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60ee7-117">Remarks</span></span>

<span data-ttu-id="60ee7-118">Además de los elementos secundarios definidos aquí, el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) también utiliza elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="60ee7-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ee7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ee7-119">Requirements</span></span>



| <span data-ttu-id="60ee7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ee7-120">Requirement</span></span> | <span data-ttu-id="60ee7-121">Value</span><span class="sxs-lookup"><span data-stu-id="60ee7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60ee7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60ee7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60ee7-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="60ee7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60ee7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60ee7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60ee7-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="60ee7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60ee7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="60ee7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ee7-127">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="60ee7-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="60ee7-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="60ee7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





