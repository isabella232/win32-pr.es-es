---
title: Programador de tareas constantes de error y de éxito (WinError. h)
description: Si se produce un error, las API de Programador de tareas pueden devolver uno de los siguientes códigos de error como un valor HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Programador de tareas las constantes Programador de tareas, Reference, error y Success
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679059"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="3a150-104">Programador de tareas las constantes de error y Success</span><span class="sxs-lookup"><span data-stu-id="3a150-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="3a150-105">Si se produce un error, las API de Programador de tareas pueden devolver uno de los siguientes códigos de error como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a150-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="3a150-106">Las constantes que comienzan por SCHEd \_ S \_ son constantes correctas y las constantes que comienzan por sched \_ e \_ son constantes de error.</span><span class="sxs-lookup"><span data-stu-id="3a150-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="3a150-107">Ejemplo de [código de C/C++: recuperar el estado](c-c-code-example-retrieving-task-status.md)de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="3a150-108">Algunas API de Programador de tareas pueden devolver códigos de error del sistema y de la red (por ejemplo, 64).</span><span class="sxs-lookup"><span data-stu-id="3a150-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="3a150-109">Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="3a150-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="3a150-110">Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3a150-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="3a150-111">Para obtener más información sobre eventos y mensajes de error, consulte [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a150-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="3a150-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**tarea SCHEd \_ S \_ \_ lista**</span><span class="sxs-lookup"><span data-stu-id="3a150-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="3a150-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="3a150-114">La tarea está lista para ejecutarse en la siguiente hora programada.</span><span class="sxs-lookup"><span data-stu-id="3a150-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**tarea SCHEd \_ S en \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="3a150-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="3a150-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="3a150-117">La tarea está en ejecución.</span><span class="sxs-lookup"><span data-stu-id="3a150-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**tarea SCHEd \_ S \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="3a150-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="3a150-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="3a150-120">La tarea no se ejecutará a las horas programadas porque se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3a150-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**la \_ tarea sched \_ \_ no se ha \_ \_ ejecutado**</span><span class="sxs-lookup"><span data-stu-id="3a150-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="3a150-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="3a150-123">La tarea aún no se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="3a150-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**la \_ tarea sched S \_ \_ no hay \_ más \_ ejecuciones**</span><span class="sxs-lookup"><span data-stu-id="3a150-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="3a150-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="3a150-126">No hay más ejecuciones programadas para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**tarea SCHEd \_ S \_ \_ no \_ programada**</span><span class="sxs-lookup"><span data-stu-id="3a150-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="3a150-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="3a150-129">No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea en una programación.</span><span class="sxs-lookup"><span data-stu-id="3a150-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_tarea esq \_ S \_ finalizada**</span><span class="sxs-lookup"><span data-stu-id="3a150-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="3a150-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="3a150-132">El usuario finalizó la última ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**\_ \_ \_ no hay \_ \_ desencadenadores VÁLIDOs en la tarea sched S**</span><span class="sxs-lookup"><span data-stu-id="3a150-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="3a150-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="3a150-135">La tarea no tiene desencadenadores o los desencadenadores existentes están deshabilitados o no se han establecido.</span><span class="sxs-lookup"><span data-stu-id="3a150-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_ \_ desencadenador de evento sched S \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="3a150-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="3a150-138">Los desencadenadores de eventos no tienen tiempos de ejecución establecidos.</span><span class="sxs-lookup"><span data-stu-id="3a150-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ no \_ se encontró el desencadenador sched E**</span><span class="sxs-lookup"><span data-stu-id="3a150-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="3a150-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="3a150-141">No se encuentra el desencadenador de una tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**tarea SCHEd \_ E \_ \_ no \_ preparada**</span><span class="sxs-lookup"><span data-stu-id="3a150-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="3a150-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="3a150-144">No se han establecido una o varias de las propiedades necesarias para ejecutar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**tarea SCHEd \_ E \_ no se \_ \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="3a150-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="3a150-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="3a150-147">No hay ninguna instancia en ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**el \_ servicio sched E \_ \_ no \_ está instalado**</span><span class="sxs-lookup"><span data-stu-id="3a150-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="3a150-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="3a150-150">El servicio de Programador de tareas no está instalado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="3a150-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHEd \_ E \_ no puede \_ abrir la \_ tarea**</span><span class="sxs-lookup"><span data-stu-id="3a150-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="3a150-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="3a150-153">No se pudo abrir el objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHEd \_ E \_ tarea no válida \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="3a150-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="3a150-156">El objeto es un objeto de tarea no válido o no es un objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_información de cuenta de E/s \_ \_ \_ no \_ establecida**</span><span class="sxs-lookup"><span data-stu-id="3a150-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="3a150-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="3a150-159">No se encontró ninguna información de cuenta en la base de datos de Programador de tareas Security para la tarea indicada.</span><span class="sxs-lookup"><span data-stu-id="3a150-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ no se encontró el nombre \_ de cuenta de sched**</span><span class="sxs-lookup"><span data-stu-id="3a150-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="3a150-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="3a150-162">No se puede establecer la existencia de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="3a150-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHEd \_ E \_ cuenta \_ dBase \_ dañada**</span><span class="sxs-lookup"><span data-stu-id="3a150-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="3a150-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="3a150-165">Se detectaron daños en la base de datos de seguridad de Programador de tareas; la base de datos se ha restablecido.</span><span class="sxs-lookup"><span data-stu-id="3a150-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHEd \_ E \_ sin \_ servicios de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="3a150-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="3a150-168">Programador de tareas servicios de seguridad solo están disponibles en Windows NT.</span><span class="sxs-lookup"><span data-stu-id="3a150-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**\_versión de \_ \_ objeto desconocido \_ de sched E**</span><span class="sxs-lookup"><span data-stu-id="3a150-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="3a150-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="3a150-171">La versión del objeto de tarea no es compatible o no es válida.</span><span class="sxs-lookup"><span data-stu-id="3a150-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opción de \_ cuenta no admitida de \_ sched E \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="3a150-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="3a150-174">La tarea se ha configurado con una combinación no admitida de opciones de tiempo de ejecución y configuración de cuenta.</span><span class="sxs-lookup"><span data-stu-id="3a150-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**el \_ servicio sched E \_ no se \_ \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="3a150-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="3a150-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="3a150-177">El servicio Programador de tareas no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3a150-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHEd \_ E \_ UNEXPECTEDNODE**</span><span class="sxs-lookup"><span data-stu-id="3a150-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="3a150-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="3a150-180">El XML de la tarea contiene un nodo inesperado.</span><span class="sxs-lookup"><span data-stu-id="3a150-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**espacio de nombres SCHEd \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="3a150-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="3a150-183">El XML de la tarea contiene un elemento o un atributo de un espacio de nombres inesperado.</span><span class="sxs-lookup"><span data-stu-id="3a150-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHEd \_ E \_ INVALIDVALUE**</span><span class="sxs-lookup"><span data-stu-id="3a150-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="3a150-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="3a150-186">El XML de la tarea contiene un valor que tiene un formato incorrecto o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="3a150-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHEd \_ E \_ MISSINGNODE**</span><span class="sxs-lookup"><span data-stu-id="3a150-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="3a150-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="3a150-189">Falta un elemento o atributo obligatorio en el XML de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHEd \_ E \_ MALFORMEDXML**</span><span class="sxs-lookup"><span data-stu-id="3a150-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="3a150-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="3a150-192">El XML de la tarea tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="3a150-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHEd \_ S \_ algunos \_ desencadenadores con \_ errores**</span><span class="sxs-lookup"><span data-stu-id="3a150-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="3a150-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="3a150-195">La tarea está registrada, pero no todos los desencadenadores especificados iniciarán la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema de \_ Inicio de \_ sesión por lotes \_ de sched S**</span><span class="sxs-lookup"><span data-stu-id="3a150-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="3a150-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="3a150-198">La tarea está registrada, pero puede que no se inicie.</span><span class="sxs-lookup"><span data-stu-id="3a150-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="3a150-199">El privilegio de inicio de sesión por lotes debe estar habilitado para la entidad de seguridad de tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHEd \_ E \_ demasiados \_ \_ nodos**</span><span class="sxs-lookup"><span data-stu-id="3a150-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="3a150-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="3a150-202">El XML de la tarea contiene demasiados nodos del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="3a150-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_ \_ \_ límite final de sched E \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="3a150-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="3a150-205">No se puede iniciar la tarea después del límite final del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="3a150-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHEd \_ E \_ ya se \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="3a150-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="3a150-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="3a150-208">Ya se está ejecutando una instancia de esta tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHEd \_ E \_ usuario \_ sin \_ iniciar sesión \_**</span><span class="sxs-lookup"><span data-stu-id="3a150-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="3a150-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="3a150-211">La tarea no se ejecutará porque el usuario no ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3a150-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHEd \_ E \_ \_ \_ valor hash de tarea no válido**</span><span class="sxs-lookup"><span data-stu-id="3a150-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="3a150-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="3a150-214">La imagen de tarea está dañada o se ha alterado.</span><span class="sxs-lookup"><span data-stu-id="3a150-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**el \_ servicio sched E \_ \_ no \_ está disponible**</span><span class="sxs-lookup"><span data-stu-id="3a150-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="3a150-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="3a150-217">El servicio Programador de tareas no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3a150-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**el \_ servicio sched E está \_ \_ demasiado \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="3a150-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="3a150-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="3a150-220">El servicio de Programador de tareas está demasiado ocupado para atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a150-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="3a150-221">Vuelva a intentarlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="3a150-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**tarea SCHEd \_ E \_ \_ intentada**</span><span class="sxs-lookup"><span data-stu-id="3a150-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="3a150-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="3a150-224">El servicio Programador de tareas intentó ejecutar la tarea, pero la tarea no se ejecutó debido a una de las restricciones de la definición de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**tarea SCHEd \_ S \_ \_ en cola**</span><span class="sxs-lookup"><span data-stu-id="3a150-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="3a150-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="3a150-227">El servicio Programador de tareas solicitó la ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3a150-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**tarea SCHEd \_ E \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="3a150-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="3a150-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="3a150-230">La tarea está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="3a150-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Tarea SCHEd \_ E \_ \_ no \_ \_ compatible v1**</span><span class="sxs-lookup"><span data-stu-id="3a150-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="3a150-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="3a150-233">La tarea tiene propiedades que no son compatibles con versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a150-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a150-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHEd \_ E \_ Inicio \_ a \_ petición**</span><span class="sxs-lookup"><span data-stu-id="3a150-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a150-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="3a150-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="3a150-236">La configuración de la tarea no permite que la tarea se inicie a petición.</span><span class="sxs-lookup"><span data-stu-id="3a150-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a150-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a150-237">Requirements</span></span>



| <span data-ttu-id="3a150-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a150-238">Requirement</span></span> | <span data-ttu-id="3a150-239">Value</span><span class="sxs-lookup"><span data-stu-id="3a150-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a150-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a150-240">Minimum supported client</span></span><br/> | <span data-ttu-id="3a150-241">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a150-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a150-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a150-242">Minimum supported server</span></span><br/> | <span data-ttu-id="3a150-243">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a150-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a150-244">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a150-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a150-245"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a150-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





