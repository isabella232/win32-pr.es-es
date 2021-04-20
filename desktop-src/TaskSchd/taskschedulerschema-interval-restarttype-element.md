---
title: Elemento Interval (restartType)
description: Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Intervalo de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734190"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="53ccb-104">Elemento Interval (restartType)</span><span class="sxs-lookup"><span data-stu-id="53ccb-104">Interval (restartType) Element</span></span>

<span data-ttu-id="53ccb-105">Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="53ccb-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="53ccb-106">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="53ccb-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="53ccb-107">El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="53ccb-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="53ccb-108">El elemento se define mediante el [**tipo complejo restartType.**](taskschedulerschema-restarttype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="53ccb-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="53ccb-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="53ccb-109">Parent element</span></span>



| <span data-ttu-id="53ccb-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="53ccb-110">Element</span></span>                                                                               | <span data-ttu-id="53ccb-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="53ccb-111">Derived from</span></span>                                                       | <span data-ttu-id="53ccb-112">Description</span><span class="sxs-lookup"><span data-stu-id="53ccb-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53ccb-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="53ccb-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="53ccb-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="53ccb-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="53ccb-115">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="53ccb-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="53ccb-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53ccb-116">Remarks</span></span>

<span data-ttu-id="53ccb-117">Si se especifica este elemento, también se debe especificar el elemento [**Count**](taskschedulerschema-count-restarttype-element.md) para que el Programador de tareas el número de veces que debe intentar reiniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="53ccb-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="53ccb-118">Para el desarrollo de C++, [**vea Propiedad RestartInterval de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)</span><span class="sxs-lookup"><span data-stu-id="53ccb-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="53ccb-119">Para el desarrollo de scripts, [**vea TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="53ccb-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53ccb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53ccb-120">Requirements</span></span>



| <span data-ttu-id="53ccb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53ccb-121">Requirement</span></span> | <span data-ttu-id="53ccb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53ccb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53ccb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53ccb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53ccb-124">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="53ccb-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53ccb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53ccb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53ccb-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53ccb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53ccb-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53ccb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ccb-128">Programador de tareas de esquema</span><span class="sxs-lookup"><span data-stu-id="53ccb-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





