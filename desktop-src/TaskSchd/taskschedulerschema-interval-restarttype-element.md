---
title: Elemento Interval (restartType)
description: Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Programador de tareas de elemento Interval
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996031"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="e5fc6-104">Elemento Interval (restartType)</span><span class="sxs-lookup"><span data-stu-id="e5fc6-104">Interval (restartType) Element</span></span>

<span data-ttu-id="e5fc6-105">Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="e5fc6-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="e5fc6-106">El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, "PT5M" es de 5 minutos, "PT1H" es 1 hora y "PT20M" es de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="e5fc6-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="e5fc6-107">El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="e5fc6-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
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
```

<span data-ttu-id="e5fc6-108">El elemento se define mediante el tipo complejo de [**restartType**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fc6-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e5fc6-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e5fc6-109">Parent element</span></span>



| <span data-ttu-id="e5fc6-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e5fc6-110">Element</span></span>                                                                               | <span data-ttu-id="e5fc6-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e5fc6-111">Derived from</span></span>                                                       | <span data-ttu-id="e5fc6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5fc6-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5fc6-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="e5fc6-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="e5fc6-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="e5fc6-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="e5fc6-115">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="e5fc6-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5fc6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5fc6-116">Remarks</span></span>

<span data-ttu-id="e5fc6-117">Si se especifica este elemento, también se debe especificar el elemento [**Count**](taskschedulerschema-count-restarttype-element.md) para indicar al programador de tareas cuántas veces debe intentar reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="e5fc6-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="e5fc6-118">Para el desarrollo de C++, consulte la [**propiedad RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span><span class="sxs-lookup"><span data-stu-id="e5fc6-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="e5fc6-119">Para el desarrollo de scripts, vea [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="e5fc6-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fc6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5fc6-120">Requirements</span></span>



| <span data-ttu-id="e5fc6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5fc6-121">Requirement</span></span> | <span data-ttu-id="e5fc6-122">Value</span><span class="sxs-lookup"><span data-stu-id="e5fc6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5fc6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5fc6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fc6-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e5fc6-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5fc6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5fc6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fc6-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5fc6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5fc6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5fc6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5fc6-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e5fc6-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





