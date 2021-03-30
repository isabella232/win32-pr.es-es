---
title: Elemento fecha límite
description: Especifica el momento en que el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Programador de tareas de elementos de fecha límite
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801772"
---
# <a name="deadline-element"></a><span data-ttu-id="280a1-104">Elemento fecha límite</span><span class="sxs-lookup"><span data-stu-id="280a1-104">Deadline Element</span></span>

<span data-ttu-id="280a1-105">Especifica el momento en que el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.</span><span class="sxs-lookup"><span data-stu-id="280a1-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="280a1-106">El formato de esta cadena es *PnYnMnDTnHnMnS*, donde *NY* es el número de años. nm es el número de meses, *ND* es el número de días, *T* es el separador de fecha y hora, *NH* es el número de horas, *nm* es el número de minutos y *NS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="280a1-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="280a1-107">El valor mínimo es un minuto.</span><span class="sxs-lookup"><span data-stu-id="280a1-107">The minimum value is one minute.</span></span> <span data-ttu-id="280a1-108">Para obtener más información sobre el tipo de duración, vea [esquema XML parte 2: tipos de datos segunda edición](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="280a1-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="280a1-109">Fecha límite mínima que una tarea puede usar es 1 día.</span><span class="sxs-lookup"><span data-stu-id="280a1-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="280a1-110">El valor del elemento **fecha límite** debe ser mayor que el valor del elemento [**period**](taskschedulerschema-period-element.md) .</span><span class="sxs-lookup"><span data-stu-id="280a1-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="280a1-111">Si no se especifica la fecha límite, la tarea no se iniciará durante el mantenimiento automático de emergencia.</span><span class="sxs-lookup"><span data-stu-id="280a1-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="280a1-112">El elemento de **fecha límite** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="280a1-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="280a1-113">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="280a1-113">Parent element</span></span>



| <span data-ttu-id="280a1-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="280a1-114">Element</span></span>                                                                                                                          | <span data-ttu-id="280a1-115">Derivado de</span><span class="sxs-lookup"><span data-stu-id="280a1-115">Derived from</span></span>                                                                               | <span data-ttu-id="280a1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="280a1-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="280a1-117">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="280a1-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="280a1-118">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="280a1-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="280a1-119">Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="280a1-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="280a1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="280a1-120">Remarks</span></span>

<span data-ttu-id="280a1-121">Para la programación en C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .</span><span class="sxs-lookup"><span data-stu-id="280a1-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="280a1-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="280a1-122">Examples</span></span>

<span data-ttu-id="280a1-123">El siguiente código XML define un calendario de meses que ejecuta la tarea en marzo.</span><span class="sxs-lookup"><span data-stu-id="280a1-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="280a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="280a1-124">Requirements</span></span>



| <span data-ttu-id="280a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="280a1-125">Requirement</span></span> | <span data-ttu-id="280a1-126">Value</span><span class="sxs-lookup"><span data-stu-id="280a1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="280a1-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="280a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="280a1-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="280a1-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="280a1-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="280a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="280a1-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="280a1-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="280a1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="280a1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280a1-132">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="280a1-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="280a1-133">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="280a1-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





