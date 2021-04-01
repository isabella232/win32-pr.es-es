---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Especifica cómo realiza el Programador de tareas las tareas durante el mantenimiento automático.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Programador de tareas del elemento MaintenanceSettings
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150798"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="e4018-104">Elemento MaintenanceSettings (maintenanceSettingsType)</span><span class="sxs-lookup"><span data-stu-id="e4018-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="e4018-105">Especifica cómo realiza el Programador de tareas las tareas durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="e4018-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="e4018-106">El elemento **MaintenanceSettings** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e4018-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e4018-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e4018-107">Parent element</span></span>



| <span data-ttu-id="e4018-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e4018-108">Element</span></span>                                                           | <span data-ttu-id="e4018-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e4018-109">Derived from</span></span>                                                         | <span data-ttu-id="e4018-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4018-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4018-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e4018-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e4018-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e4018-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e4018-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="e4018-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e4018-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e4018-114">Child elements</span></span>



| <span data-ttu-id="e4018-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e4018-115">Element</span></span>                                                    | <span data-ttu-id="e4018-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4018-116">Type</span></span>    | <span data-ttu-id="e4018-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4018-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4018-118">**Fecha límite**</span><span class="sxs-lookup"><span data-stu-id="e4018-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="e4018-119">Especifica la cantidad de tiempo después de la cual el programador de tareas intentará iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento normal.</span><span class="sxs-lookup"><span data-stu-id="e4018-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="e4018-120">**Exclusivo**</span><span class="sxs-lookup"><span data-stu-id="e4018-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="e4018-121">boolean</span><span class="sxs-lookup"><span data-stu-id="e4018-121">boolean</span></span> | <span data-ttu-id="e4018-122">Si se establece en true, la tarea se iniciará exclusivamente entre otras tareas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="e4018-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="e4018-123">**Período**</span><span class="sxs-lookup"><span data-stu-id="e4018-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="e4018-124">Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="e4018-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="e4018-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4018-125">Remarks</span></span>

<span data-ttu-id="e4018-126">En la programación de C++, esta configuración de inactividad se especifica mediante la propiedad [**ITaskSettings3:: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .</span><span class="sxs-lookup"><span data-stu-id="e4018-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e4018-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e4018-127">Examples</span></span>

<span data-ttu-id="e4018-128">En el código XML siguiente se define un elemento de configuración que indica a Programador de tareas que ejecute la tarea una vez en 5 días durante el mantenimiento automático regular y, si se produce un error durante 15 días, empiece a intentar la tarea durante el mantenimiento automático de emergencia.</span><span class="sxs-lookup"><span data-stu-id="e4018-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e4018-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4018-129">Requirements</span></span>



| <span data-ttu-id="e4018-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4018-130">Requirement</span></span> | <span data-ttu-id="e4018-131">Value</span><span class="sxs-lookup"><span data-stu-id="e4018-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4018-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4018-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e4018-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4018-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="e4018-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4018-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e4018-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4018-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4018-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4018-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4018-137">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e4018-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e4018-138">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e4018-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





