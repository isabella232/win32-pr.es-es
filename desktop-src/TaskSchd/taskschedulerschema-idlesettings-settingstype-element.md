---
title: Elemento IdleSettings (settingsType)
description: Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Programador de tareas del elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150799"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="8430f-104">Elemento IdleSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="8430f-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="8430f-105">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="8430f-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="8430f-106">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="8430f-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="8430f-107">El elemento **IdleSettings** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8430f-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8430f-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8430f-108">Parent element</span></span>

| <span data-ttu-id="8430f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8430f-109">Element</span></span>                                                           | <span data-ttu-id="8430f-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8430f-110">Derived from</span></span>                                                         | <span data-ttu-id="8430f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8430f-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8430f-112">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="8430f-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="8430f-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="8430f-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="8430f-114">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8430f-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="8430f-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8430f-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="8430f-116">La configuración de *Duration* y *WaitTimeout* está en desuso.</span><span class="sxs-lookup"><span data-stu-id="8430f-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="8430f-117">Todavía están presentes en la interfaz de usuario de Programador de tareas y sus métodos de interfaz todavía pueden devolver valores válidos, pero ya no se usan.</span><span class="sxs-lookup"><span data-stu-id="8430f-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="8430f-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="8430f-118">Element</span></span>                                                                                  | <span data-ttu-id="8430f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8430f-119">Type</span></span>     | <span data-ttu-id="8430f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8430f-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8430f-121">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="8430f-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="8430f-122">boolean</span><span class="sxs-lookup"><span data-stu-id="8430f-122">boolean</span></span>  | <span data-ttu-id="8430f-123">Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.</span><span class="sxs-lookup"><span data-stu-id="8430f-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="8430f-124">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="8430f-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="8430f-125">boolean</span><span class="sxs-lookup"><span data-stu-id="8430f-125">boolean</span></span>  | <span data-ttu-id="8430f-126">Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="8430f-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="8430f-127">En **desuso**: [ **duración**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="8430f-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="8430f-128">duration</span><span class="sxs-lookup"><span data-stu-id="8430f-128">duration</span></span> | <span data-ttu-id="8430f-129">Especifica cuánto tiempo el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.</span><span class="sxs-lookup"><span data-stu-id="8430f-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="8430f-130">En **desuso**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="8430f-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="8430f-131">duration</span><span class="sxs-lookup"><span data-stu-id="8430f-131">duration</span></span> | <span data-ttu-id="8430f-132">Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="8430f-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="8430f-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8430f-133">Remarks</span></span>

<span data-ttu-id="8430f-134">Para el desarrollo de scripts, la configuración inactiva se especifica mediante la propiedad [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="8430f-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="8430f-135">En el desarrollo de C++, la configuración inactiva se especifica mediante la propiedad [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .</span><span class="sxs-lookup"><span data-stu-id="8430f-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="8430f-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8430f-136">Examples</span></span>

<span data-ttu-id="8430f-137">En el código XML siguiente se define un elemento de configuración que permite a Programador de tareas esperar 24 horas por una condición de inactividad y, a continuación, solo permite 10 minutos {IdleDuration) para iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8430f-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="8430f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8430f-138">Requirements</span></span>

| <span data-ttu-id="8430f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8430f-139">Requirement</span></span> | <span data-ttu-id="8430f-140">Value</span><span class="sxs-lookup"><span data-stu-id="8430f-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8430f-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8430f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8430f-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8430f-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8430f-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8430f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8430f-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8430f-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="8430f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8430f-145">See also</span></span>

[<span data-ttu-id="8430f-146">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8430f-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="8430f-147">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8430f-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
