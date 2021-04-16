---
title: Elemento exclusivo
description: Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Programador de tareas de elemento exclusivo
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685884"
---
# <a name="exclusive-element"></a><span data-ttu-id="a11b3-104">Elemento exclusivo</span><span class="sxs-lookup"><span data-stu-id="a11b3-104">Exclusive Element</span></span>

<span data-ttu-id="a11b3-105">Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a11b3-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="a11b3-106">La exclusividad solo está garantizada entre otras tareas de mantenimiento y no concede ninguna prioridad de ordenación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a11b3-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="a11b3-107">Si no se especifica la exclusividad, la tarea se inicia en paralelo con otras tareas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="a11b3-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="a11b3-108">El elemento **Exclusive** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a11b3-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a11b3-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a11b3-109">Parent element</span></span>



| <span data-ttu-id="a11b3-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a11b3-110">Element</span></span>                                                                                                                          | <span data-ttu-id="a11b3-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a11b3-111">Derived from</span></span>                                                                               | <span data-ttu-id="a11b3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a11b3-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a11b3-113">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="a11b3-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="a11b3-114">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a11b3-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="a11b3-115">Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="a11b3-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a11b3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a11b3-116">Remarks</span></span>

<span data-ttu-id="a11b3-117">En la programación de C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .</span><span class="sxs-lookup"><span data-stu-id="a11b3-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a11b3-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a11b3-118">Examples</span></span>

<span data-ttu-id="a11b3-119">El siguiente código XML define la tarea de mantenimiento con el requisito de fecha límite establecido en 15 días.</span><span class="sxs-lookup"><span data-stu-id="a11b3-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="a11b3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11b3-120">Requirements</span></span>



| <span data-ttu-id="a11b3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11b3-121">Requirement</span></span> | <span data-ttu-id="a11b3-122">Value</span><span class="sxs-lookup"><span data-stu-id="a11b3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a11b3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a11b3-124">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a11b3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a11b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a11b3-126">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a11b3-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a11b3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a11b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11b3-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="a11b3-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a11b3-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a11b3-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





