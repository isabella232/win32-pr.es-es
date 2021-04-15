---
title: Objeto IdleSettings
description: Objeto de scripting que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Objeto IdleSettings Programador de tareas
- Programador de tareas de objeto IdleSettings, descrito
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422167"
---
# <a name="idlesettings-object"></a><span data-ttu-id="f3471-105">Objeto IdleSettings</span><span class="sxs-lookup"><span data-stu-id="f3471-105">IdleSettings object</span></span>

<span data-ttu-id="f3471-106">Objeto de scripting que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f3471-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="f3471-107">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="f3471-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="f3471-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3471-108">Members</span></span>

<span data-ttu-id="f3471-109">El objeto **IdleSettings** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3471-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="f3471-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3471-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3471-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3471-111">Properties</span></span>

<span data-ttu-id="f3471-112">El objeto **IdleSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3471-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="f3471-113">La configuración de *IdleDuration* y *WaitTimeout* está en desuso.</span><span class="sxs-lookup"><span data-stu-id="f3471-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="f3471-114">Todavía están presentes en la interfaz de usuario de Programador de tareas y sus métodos de interfaz todavía pueden devolver valores válidos, pero ya no se usan.</span><span class="sxs-lookup"><span data-stu-id="f3471-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="f3471-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3471-115">Property</span></span>                                                       | <span data-ttu-id="f3471-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f3471-116">Access type</span></span>           | <span data-ttu-id="f3471-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3471-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3471-118">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="f3471-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="f3471-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3471-119">Read/write</span></span><br/> | <span data-ttu-id="f3471-120">Obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.</span><span class="sxs-lookup"><span data-stu-id="f3471-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="f3471-121">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="f3471-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="f3471-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3471-122">Read/write</span></span><br/> | <span data-ttu-id="f3471-123">Obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="f3471-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="f3471-124">En **desuso**: [ **IdleDuration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="f3471-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="f3471-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3471-125">Read/write</span></span><br/> | <span data-ttu-id="f3471-126">Obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.</span><span class="sxs-lookup"><span data-stu-id="f3471-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="f3471-127">En **desuso**: [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="f3471-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="f3471-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3471-128">Read/write</span></span><br/> | <span data-ttu-id="f3471-129">Obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="f3471-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="f3471-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3471-130">Remarks</span></span>

<span data-ttu-id="f3471-131">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="f3471-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="f3471-132">Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="f3471-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="f3471-133">*IdleSettings. IdleDuration* y *IdleSettings. WaitTimeout* están desusados.</span><span class="sxs-lookup"><span data-stu-id="f3471-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3471-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3471-134">Requirements</span></span>

| <span data-ttu-id="f3471-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3471-135">Requirement</span></span> | <span data-ttu-id="f3471-136">Value</span><span class="sxs-lookup"><span data-stu-id="f3471-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3471-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3471-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3471-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3471-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3471-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3471-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3471-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3471-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3471-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f3471-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3471-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f3471-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f3471-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3471-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3471-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3471-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="f3471-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3471-145">See also</span></span>

[<span data-ttu-id="f3471-146">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f3471-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="f3471-147">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f3471-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
