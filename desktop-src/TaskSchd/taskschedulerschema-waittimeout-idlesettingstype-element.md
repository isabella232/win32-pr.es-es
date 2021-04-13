---
title: Elemento WaitTimeout (idleSettingsType)
description: Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Programador de tareas del elemento WaitTimeout
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534864"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="9932a-104">Elemento WaitTimeout (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="9932a-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="9932a-105">Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9932a-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="9932a-106">Si no se especifica ningún valor para este elemento, el servicio Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9932a-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="9932a-107">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="9932a-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="9932a-108">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="9932a-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="9932a-109">El tiempo mínimo permitido es 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="9932a-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="9932a-110">El elemento se define mediante el tipo complejo de [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9932a-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9932a-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9932a-111">Parent element</span></span>



| <span data-ttu-id="9932a-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="9932a-112">Element</span></span>                                                                       | <span data-ttu-id="9932a-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9932a-113">Derived from</span></span>                                                                 | <span data-ttu-id="9932a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9932a-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9932a-115">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="9932a-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="9932a-116">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="9932a-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="9932a-117">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9932a-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9932a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9932a-118">Remarks</span></span>

<span data-ttu-id="9932a-119">Para el desarrollo de scripts, este valor de inactividad se especifica mediante la propiedad [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="9932a-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="9932a-120">En el desarrollo de C++, este valor de inactividad se especifica mediante la propiedad [**IIdleSettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .</span><span class="sxs-lookup"><span data-stu-id="9932a-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9932a-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9932a-121">Examples</span></span>

<span data-ttu-id="9932a-122">En el código XML siguiente se define un valor de inactivo que espera 24 horas para que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9932a-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="9932a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9932a-123">Requirements</span></span>



| <span data-ttu-id="9932a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9932a-124">Requirement</span></span> | <span data-ttu-id="9932a-125">Value</span><span class="sxs-lookup"><span data-stu-id="9932a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9932a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9932a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9932a-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9932a-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9932a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9932a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9932a-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9932a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9932a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9932a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9932a-131">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="9932a-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9932a-132">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9932a-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





