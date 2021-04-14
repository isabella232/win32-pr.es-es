---
title: Duration (idleSettingsType), elemento
description: Especifica cuánto tiempo el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Elemento Duration Programador de tareas
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533951"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="8e79f-104">Duration (idleSettingsType), elemento</span><span class="sxs-lookup"><span data-stu-id="8e79f-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="8e79f-105">Especifica cuánto tiempo el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.</span><span class="sxs-lookup"><span data-stu-id="8e79f-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="8e79f-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="8e79f-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="8e79f-107">El valor mínimo es un minuto.</span><span class="sxs-lookup"><span data-stu-id="8e79f-107">The minimum value is one minute.</span></span> <span data-ttu-id="8e79f-108">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="8e79f-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8e79f-109">El elemento se define mediante el tipo complejo de [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8e79f-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8e79f-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8e79f-110">Parent element</span></span>



| <span data-ttu-id="8e79f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8e79f-111">Element</span></span>                                                                       | <span data-ttu-id="8e79f-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8e79f-112">Derived from</span></span>                                                                 | <span data-ttu-id="8e79f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e79f-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e79f-114">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="8e79f-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="8e79f-115">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="8e79f-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="8e79f-116">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="8e79f-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8e79f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e79f-117">Remarks</span></span>

<span data-ttu-id="8e79f-118">Para la programación de scripts, este valor de inactividad se especifica mediante la propiedad [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) .</span><span class="sxs-lookup"><span data-stu-id="8e79f-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="8e79f-119">En la programación de C++, esta configuración de inactividad se especifica mediante la propiedad [**IIdleSettings:: IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .</span><span class="sxs-lookup"><span data-stu-id="8e79f-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="8e79f-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8e79f-120">Examples</span></span>

<span data-ttu-id="8e79f-121">En el código XML siguiente se define un valor de inactivo que permite que se inicie la tarea 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="8e79f-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="8e79f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e79f-122">Requirements</span></span>



| <span data-ttu-id="8e79f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e79f-123">Requirement</span></span> | <span data-ttu-id="8e79f-124">Value</span><span class="sxs-lookup"><span data-stu-id="8e79f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e79f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e79f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e79f-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e79f-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e79f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e79f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e79f-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e79f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e79f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e79f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e79f-130">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8e79f-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8e79f-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8e79f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





