---
title: TriggerCollection. Create (método)
description: En el caso de scripting, crea un nuevo desencadenador para la tarea.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- desencadenadores Programador de tareas, crear
- Crear método Programador de tareas
- Create Method Programador de tareas, TriggerCollection Object
- Programador de tareas de objeto TriggerCollection, Create (método)
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676677"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="9db1d-107">TriggerCollection. Create (método)</span><span class="sxs-lookup"><span data-stu-id="9db1d-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="9db1d-108">En el caso de scripting, crea un nuevo desencadenador para la tarea.</span><span class="sxs-lookup"><span data-stu-id="9db1d-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db1d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9db1d-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="9db1d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9db1d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db1d-111">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9db1d-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db1d-112">Este parámetro se establece en una de las constantes de enumeración [**\_ \_ tipo2 de desencadenador de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="9db1d-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="9db1d-113">Value</span><span class="sxs-lookup"><span data-stu-id="9db1d-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="9db1d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9db1d-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="9db1d-115"><dt>**Tarea \_ de DESENCADENAr \_ evento**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9db1d-116">Desencadena la tarea cuando se produce un evento específico.</span><span class="sxs-lookup"><span data-stu-id="9db1d-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="9db1d-117"><dt>**Tarea \_ de \_Hora del desencadenador**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="9db1d-118">Desencadena la tarea a una hora específica del día.</span><span class="sxs-lookup"><span data-stu-id="9db1d-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="9db1d-119"><dt>**Tarea \_ de DESENCADENAr \_ diariamente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9db1d-120">Desencadena la tarea según una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="9db1d-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="9db1d-121">Por ejemplo, la tarea se inicia a una hora específica cada día, cada día, cada tres días, etc.</span><span class="sxs-lookup"><span data-stu-id="9db1d-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="9db1d-122"><dt>**Tarea \_ de DESENCADENAr \_ semanalmente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="9db1d-123">Desencadena la tarea según una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="9db1d-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="9db1d-124">Por ejemplo, la tarea comienza a las 8:00 A.M. de un día específico cada semana u otra semana.</span><span class="sxs-lookup"><span data-stu-id="9db1d-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="9db1d-125"><dt>**Tarea \_ de DESENCADENAr \_ mensualmente**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="9db1d-126">Desencadena la tarea según una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="9db1d-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="9db1d-127">Por ejemplo, la tarea se inicia en días específicos de meses específicos.</span><span class="sxs-lookup"><span data-stu-id="9db1d-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="9db1d-128"><dt>**Tarea \_ de DESENCADENAdor \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="9db1d-129">Desencadena la tarea en una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="9db1d-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="9db1d-130">Por ejemplo, la tarea se inicia en un determinado día de la semana, las semanas del mes y los meses del año.</span><span class="sxs-lookup"><span data-stu-id="9db1d-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="9db1d-131"><dt>**Tarea \_ de DESENCADENAdor \_ inactivo**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="9db1d-132">Desencadena la tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9db1d-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="9db1d-133"><dt>**Tarea \_ de DESENCADENAr \_ registro**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="9db1d-134">Desencadena la tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="9db1d-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="9db1d-135"><dt>**Tarea \_ de DESENCADENAdor de \_ arranque**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="9db1d-136">Desencadena la tarea cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="9db1d-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="9db1d-137"><dt>**Tarea \_ de DESENCADENAr \_ Inicio de sesión**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9db1d-138">Desencadena la tarea cuando un usuario específico inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="9db1d-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="9db1d-139"><dt>**Tarea \_ de \_Cambio de \_ estado \_ de sesión de desencadenador**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="9db1d-140">Desencadena la tarea cuando cambia un estado de sesión específico.</span><span class="sxs-lookup"><span data-stu-id="9db1d-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db1d-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9db1d-141">Return value</span></span>

<span data-ttu-id="9db1d-142">Objeto [**desencadenador**](trigger.md) que representa el nuevo desencadenador.</span><span class="sxs-lookup"><span data-stu-id="9db1d-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db1d-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9db1d-143">Remarks</span></span>

<span data-ttu-id="9db1d-144">Para obtener información acerca de cada tipo de desencadenador, consulte [tipos de desencadenador](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="9db1d-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9db1d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9db1d-145">Requirements</span></span>



| <span data-ttu-id="9db1d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db1d-146">Requirement</span></span> | <span data-ttu-id="9db1d-147">Value</span><span class="sxs-lookup"><span data-stu-id="9db1d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db1d-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9db1d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9db1d-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9db1d-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9db1d-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9db1d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9db1d-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9db1d-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9db1d-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9db1d-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="9db1d-153"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9db1d-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9db1d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db1d-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db1d-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db1d-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="9db1d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db1d-157">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9db1d-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="9db1d-158">**Activado**</span><span class="sxs-lookup"><span data-stu-id="9db1d-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





