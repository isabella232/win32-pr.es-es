---
title: Objeto RepetitionPattern
description: Objeto de scripting que define la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- desencadenadores Programador de tareas, objeto de patrón de repetición
- patrón de repetición Programador de tareas, objeto
- Objeto RepetitionPattern Programador de tareas
- Programador de tareas de objeto RepetitionPattern, descrito
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489868"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="04552-107">Objeto RepetitionPattern</span><span class="sxs-lookup"><span data-stu-id="04552-107">RepetitionPattern object</span></span>

<span data-ttu-id="04552-108">Objeto de scripting que define la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="04552-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="04552-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="04552-109">Members</span></span>

<span data-ttu-id="04552-110">El objeto **RepetitionPattern** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="04552-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="04552-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04552-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04552-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04552-112">Properties</span></span>

<span data-ttu-id="04552-113">El objeto **RepetitionPattern** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="04552-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="04552-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04552-114">Property</span></span>                                                                    | <span data-ttu-id="04552-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="04552-115">Access type</span></span>           | <span data-ttu-id="04552-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="04552-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04552-117">**Duration**</span><span class="sxs-lookup"><span data-stu-id="04552-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="04552-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04552-118">Read/write</span></span><br/> | <span data-ttu-id="04552-119">Obtiene o establece el tiempo que se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="04552-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="04552-120">**Interval**</span><span class="sxs-lookup"><span data-stu-id="04552-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="04552-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04552-121">Read/write</span></span><br/> | <span data-ttu-id="04552-122">Obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="04552-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="04552-123">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="04552-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="04552-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="04552-124">Read/write</span></span><br/> | <span data-ttu-id="04552-125">Obtiene o establece un valor booleano que indica si una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.</span><span class="sxs-lookup"><span data-stu-id="04552-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04552-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04552-126">Remarks</span></span>

<span data-ttu-id="04552-127">Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.</span><span class="sxs-lookup"><span data-stu-id="04552-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="04552-128">Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces.</span><span class="sxs-lookup"><span data-stu-id="04552-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="04552-129">Las cinco repeticiones se pueden definir con el siguiente patrón.</span><span class="sxs-lookup"><span data-stu-id="04552-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="04552-130">Una tarea comienza al principio del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="04552-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="04552-131">La siguiente tarea comienza al final del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="04552-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="04552-132">La siguiente tarea comienza al final del segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="04552-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="04552-133">La siguiente tarea comienza al final del tercer minuto.</span><span class="sxs-lookup"><span data-stu-id="04552-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="04552-134">La siguiente tarea comienza al final del cuarto minuto.</span><span class="sxs-lookup"><span data-stu-id="04552-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="04552-135">**Windows Server 2003, Windows XP y windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.</span><span class="sxs-lookup"><span data-stu-id="04552-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="04552-136">Al leer o escribir XML para una tarea, el patrón de repetición se especifica mediante el elemento [**repite**](taskschedulerschema-repetition-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="04552-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="04552-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="04552-137">Examples</span></span>

<span data-ttu-id="04552-138">Para obtener más información y código de ejemplo para esta propiedad, vea [ejemplo de desencadenador diario (scripting)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="04552-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04552-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04552-139">Requirements</span></span>



| <span data-ttu-id="04552-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="04552-140">Requirement</span></span> | <span data-ttu-id="04552-141">Value</span><span class="sxs-lookup"><span data-stu-id="04552-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04552-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04552-142">Minimum supported client</span></span><br/> | <span data-ttu-id="04552-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="04552-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="04552-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04552-144">Minimum supported server</span></span><br/> | <span data-ttu-id="04552-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="04552-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04552-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="04552-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="04552-147"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04552-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04552-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04552-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04552-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04552-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04552-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="04552-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04552-151">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="04552-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="04552-152">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="04552-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





