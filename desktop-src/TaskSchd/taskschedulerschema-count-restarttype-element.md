---
title: Count (restartType) (elemento)
description: Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Elemento Count Programador de tareas
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489862"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="1fca3-104">Count (restartType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="1fca3-104">Count (restartType) Element</span></span>

<span data-ttu-id="1fca3-105">Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="1fca3-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1fca3-106">El elemento se define mediante el tipo complejo de [**restartType**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1fca3-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1fca3-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1fca3-107">Parent element</span></span>



| <span data-ttu-id="1fca3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1fca3-108">Element</span></span>                                                                               | <span data-ttu-id="1fca3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1fca3-109">Derived from</span></span>                                                       | <span data-ttu-id="1fca3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fca3-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fca3-111">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="1fca3-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="1fca3-112">**restartType**</span><span class="sxs-lookup"><span data-stu-id="1fca3-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="1fca3-113">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="1fca3-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1fca3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fca3-114">Remarks</span></span>

<span data-ttu-id="1fca3-115">Si se especifica este elemento, también se debe especificar el elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) para indicar al programador de tareas cuánto tiempo se intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="1fca3-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="1fca3-116">Para el desarrollo de C++, consulte la [**propiedad RestartCount de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="1fca3-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="1fca3-117">Para el desarrollo de scripts, vea [**TaskSettings. RestartCount**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="1fca3-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fca3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fca3-118">Requirements</span></span>



| <span data-ttu-id="1fca3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fca3-119">Requirement</span></span> | <span data-ttu-id="1fca3-120">Value</span><span class="sxs-lookup"><span data-stu-id="1fca3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1fca3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fca3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1fca3-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fca3-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1fca3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fca3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1fca3-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fca3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fca3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fca3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fca3-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="1fca3-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





