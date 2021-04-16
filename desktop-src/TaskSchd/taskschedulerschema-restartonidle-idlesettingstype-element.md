---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Programador de tareas del elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686224"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="2fa41-104">Elemento RestartOnIdle (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="2fa41-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="2fa41-105">Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.</span><span class="sxs-lookup"><span data-stu-id="2fa41-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="2fa41-106">El elemento **RestartOnIdle** se define mediante el tipo complejo de [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa41-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2fa41-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2fa41-107">Parent element</span></span>



| <span data-ttu-id="2fa41-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2fa41-108">Element</span></span>                                                                       | <span data-ttu-id="2fa41-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2fa41-109">Derived from</span></span>                                                                 | <span data-ttu-id="2fa41-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fa41-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fa41-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="2fa41-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="2fa41-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="2fa41-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="2fa41-113">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="2fa41-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2fa41-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fa41-114">Remarks</span></span>

<span data-ttu-id="2fa41-115">Este elemento solo se utiliza si el elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="2fa41-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="2fa41-116">Para el desarrollo de scripts, esta configuración de tarea se especifica mediante la propiedad [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa41-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="2fa41-117">En el desarrollo de C++, esta configuración de tarea se especifica mediante la propiedad [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .</span><span class="sxs-lookup"><span data-stu-id="2fa41-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2fa41-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2fa41-118">Examples</span></span>

<span data-ttu-id="2fa41-119">El siguiente código XML define un valor de inactivo que indica que la tarea no debe reiniciarse cuando la condición de inactividad se repite.</span><span class="sxs-lookup"><span data-stu-id="2fa41-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="2fa41-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fa41-120">Requirements</span></span>



| <span data-ttu-id="2fa41-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa41-121">Requirement</span></span> | <span data-ttu-id="2fa41-122">Value</span><span class="sxs-lookup"><span data-stu-id="2fa41-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2fa41-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fa41-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa41-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2fa41-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2fa41-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fa41-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa41-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fa41-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2fa41-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fa41-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa41-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="2fa41-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2fa41-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2fa41-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





