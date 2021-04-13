---
title: Elemento period
description: Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Elemento period Programador de tareas
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493121"
---
# <a name="period-element"></a><span data-ttu-id="77028-104">Elemento period</span><span class="sxs-lookup"><span data-stu-id="77028-104">Period Element</span></span>

<span data-ttu-id="77028-105">Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="77028-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="77028-106">El formato de esta cadena es *PnYnMnDTnHnMnS*, donde *NY* es el número de años. nm es el número de meses, *ND* es el número de días, *T* es el separador de fecha y hora, *NH* es el número de horas, *nm* es el número de minutos y *NS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="77028-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="77028-107">El valor mínimo es un minuto.</span><span class="sxs-lookup"><span data-stu-id="77028-107">The minimum value is one minute.</span></span> <span data-ttu-id="77028-108">Para obtener más información sobre el tipo de duración, vea [esquema XML parte 2: tipos de datos segunda edición](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="77028-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

<span data-ttu-id="77028-109">El elemento de **punto** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="77028-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="77028-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="77028-110">Parent element</span></span>



| <span data-ttu-id="77028-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="77028-111">Element</span></span>                                                                                                                          | <span data-ttu-id="77028-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="77028-112">Derived from</span></span>                                                                               | <span data-ttu-id="77028-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="77028-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77028-114">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="77028-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="77028-115">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="77028-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="77028-116">Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="77028-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77028-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77028-117">Remarks</span></span>

<span data-ttu-id="77028-118">Para la programación en C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings::P Eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .</span><span class="sxs-lookup"><span data-stu-id="77028-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="77028-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="77028-119">Examples</span></span>

<span data-ttu-id="77028-120">El siguiente código XML define la tarea de mantenimiento con el requisito de periodicidad establecido en 5 días.</span><span class="sxs-lookup"><span data-stu-id="77028-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="77028-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77028-121">Requirements</span></span>



| <span data-ttu-id="77028-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="77028-122">Requirement</span></span> | <span data-ttu-id="77028-123">Value</span><span class="sxs-lookup"><span data-stu-id="77028-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77028-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77028-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77028-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="77028-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="77028-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77028-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77028-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="77028-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77028-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="77028-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77028-129">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="77028-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="77028-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="77028-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





