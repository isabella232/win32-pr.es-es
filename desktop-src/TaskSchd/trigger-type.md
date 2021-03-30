---
title: Trigger. Type (propiedad)
description: En el caso de scripting, obtiene el tipo del desencadenador.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Propiedad Type Programador de tareas
- Propiedad de tipo Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad Type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801742"
---
# <a name="triggertype-property"></a><span data-ttu-id="9ee64-106">Trigger. Type (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9ee64-106">Trigger.Type property</span></span>

<span data-ttu-id="9ee64-107">En el caso de scripting, obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="9ee64-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="9ee64-108">El tipo de desencadenador se define cuando se crea el desencadenador y no se puede cambiar más adelante.</span><span class="sxs-lookup"><span data-stu-id="9ee64-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="9ee64-109">Para obtener información sobre cómo crear un desencadenador, vea [**TriggerCollection. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="9ee64-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee64-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ee64-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="9ee64-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9ee64-111">Property value</span></span>

<span data-ttu-id="9ee64-112">Uno de los siguientes valores de enumeración [**\_ \_ tipo2 del desencadenador de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .</span><span class="sxs-lookup"><span data-stu-id="9ee64-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="9ee64-113">Value</span><span class="sxs-lookup"><span data-stu-id="9ee64-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="9ee64-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9ee64-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="9ee64-115"><dt>**Tarea \_ de DESENCADENAr \_ evento**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9ee64-116">Inicia la tarea cuando se produce un evento específico.</span><span class="sxs-lookup"><span data-stu-id="9ee64-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="9ee64-117"><dt>**Tarea \_ de \_Hora del desencadenador**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="9ee64-118">Inicia la tarea a una hora específica del día.</span><span class="sxs-lookup"><span data-stu-id="9ee64-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="9ee64-119"><dt>**Tarea \_ de DESENCADENAr \_ diariamente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9ee64-120">Inicia la tarea diariamente.</span><span class="sxs-lookup"><span data-stu-id="9ee64-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="9ee64-121"><dt>**Tarea \_ de DESENCADENAr \_ semanalmente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="9ee64-122">Inicia la tarea semanalmente.</span><span class="sxs-lookup"><span data-stu-id="9ee64-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="9ee64-123"><dt>**Tarea \_ de DESENCADENAr \_ mensualmente**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="9ee64-124">Inicia la tarea mensualmente.</span><span class="sxs-lookup"><span data-stu-id="9ee64-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="9ee64-125"><dt>**Tarea \_ de DESENCADENAdor \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="9ee64-126">Inicia la tarea cada mes en un determinado día de la semana.</span><span class="sxs-lookup"><span data-stu-id="9ee64-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="9ee64-127"><dt>**Tarea \_ de DESENCADENAdor \_ inactivo**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="9ee64-128">Inicia la tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="9ee64-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="9ee64-129"><dt>**Tarea \_ de DESENCADENAr \_ registro**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="9ee64-130">Inicia la tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="9ee64-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="9ee64-131"><dt>**Tarea \_ de DESENCADENAdor de \_ arranque**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="9ee64-132">Inicia la tarea cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="9ee64-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="9ee64-133"><dt>**Tarea \_ de DESENCADENAr \_ Inicio de sesión**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9ee64-134">Inicia la tarea cuando un usuario específico inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="9ee64-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="9ee64-135"><dt>**Tarea \_ de \_Cambio de \_ estado \_ de sesión de desencadenador**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="9ee64-136">Desencadena la tarea cuando cambia un estado de sesión específico.</span><span class="sxs-lookup"><span data-stu-id="9ee64-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="9ee64-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ee64-137">Requirements</span></span>



| <span data-ttu-id="9ee64-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ee64-138">Requirement</span></span> | <span data-ttu-id="9ee64-139">Value</span><span class="sxs-lookup"><span data-stu-id="9ee64-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee64-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ee64-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee64-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9ee64-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9ee64-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ee64-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee64-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ee64-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ee64-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9ee64-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ee64-145"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ee64-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ee64-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ee64-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee64-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee64-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ee64-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee64-149">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="9ee64-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="9ee64-150">**\_Tipo2 de desencadenador de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="9ee64-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="9ee64-151">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="9ee64-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





