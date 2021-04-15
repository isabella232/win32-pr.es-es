---
title: Elemento StopAtDurationEnd (repetitionType)
description: Especifica que las instancias en ejecución de la tarea se detienen al final de la duración del patrón de repetición.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Programador de tareas del elemento StopAtDurationEnd
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676993"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="2e86e-104">Elemento StopAtDurationEnd (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="2e86e-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="2e86e-105">Especifica que una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.</span><span class="sxs-lookup"><span data-stu-id="2e86e-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="2e86e-106">Esto solo es aplicable si se han establecido las repeticiones.</span><span class="sxs-lookup"><span data-stu-id="2e86e-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="2e86e-107">El elemento **StopAtDurationEnd** se define mediante el tipo complejo de [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2e86e-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2e86e-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2e86e-108">Parent element</span></span>

| <span data-ttu-id="2e86e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e86e-109">Element</span></span> | <span data-ttu-id="2e86e-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2e86e-110">Derived from</span></span> | <span data-ttu-id="2e86e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e86e-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="2e86e-112">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="2e86e-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="2e86e-113">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="2e86e-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="2e86e-114">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="2e86e-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="2e86e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e86e-115">Remarks</span></span>

<span data-ttu-id="2e86e-116">Para el desarrollo de scripting, este valor se especifica mediante la propiedad [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .</span><span class="sxs-lookup"><span data-stu-id="2e86e-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="2e86e-117">En el desarrollo de C++, este valor se especifica mediante la propiedad [**IRepetitionPattern:: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .</span><span class="sxs-lookup"><span data-stu-id="2e86e-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e86e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e86e-118">Requirements</span></span>

| <span data-ttu-id="2e86e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e86e-119">Requirement</span></span> | <span data-ttu-id="2e86e-120">Value</span><span class="sxs-lookup"><span data-stu-id="2e86e-120">Value</span></span> |
|-|-|
| <span data-ttu-id="2e86e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e86e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e86e-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e86e-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e86e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e86e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e86e-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e86e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="2e86e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e86e-125">See also</span></span>

[<span data-ttu-id="2e86e-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="2e86e-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="2e86e-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2e86e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
