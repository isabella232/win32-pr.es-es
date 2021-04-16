---
title: Enumeración BG_JOB_STATE (Deliveryoptimization. h)
description: La enumeración BG_JOB_STATE define valores constantes para los distintos Estados de un trabajo.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumeración BG_JOB_STATE
- Enumeración BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714550"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="e0394-105">Enumeración BG_JOB_STATE</span><span class="sxs-lookup"><span data-stu-id="e0394-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="e0394-106">La enumeración **BG_JOB_STATE** define valores constantes para los distintos Estados de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="e0394-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0394-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0394-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="e0394-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e0394-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e0394-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="e0394-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-110">Especifica que el trabajo está en la cola y en espera de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e0394-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="e0394-111">Si un usuario cierra la sesión mientras su trabajo está transfiriendo, el trabajo pasa al estado en cola.</span><span class="sxs-lookup"><span data-stu-id="e0394-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="e0394-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="e0394-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="e0394-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-115">Especifica que es la transferencia de datos para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e0394-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="e0394-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-117">Especifica que el trabajo se ha suspendido (en pausa).</span><span class="sxs-lookup"><span data-stu-id="e0394-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="e0394-118">Para suspender un trabajo, llame al método [**IBackgroundCopyJob:: Suspend**](ibackgroundcopyjob-suspend.md) .</span><span class="sxs-lookup"><span data-stu-id="e0394-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="e0394-119">El trabajo permanece suspendido hasta que se llama al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md)o [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="e0394-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="e0394-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-121">Especifica que se ha producido un error irrecuperable (el servicio no puede transferir el archivo).</span><span class="sxs-lookup"><span data-stu-id="e0394-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="e0394-122">Si se puede corregir el error, como un error de acceso denegado, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) una vez corregido el error.</span><span class="sxs-lookup"><span data-stu-id="e0394-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="e0394-123">Sin embargo, si el error no se puede corregir, llame al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo o llame al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para aceptar la parte de un trabajo de descarga que se transfirió correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0394-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="e0394-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-125">Especifica que se ha producido un error recuperable.</span><span class="sxs-lookup"><span data-stu-id="e0394-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="e0394-126">Se reintentarán los trabajos en el estado de error transitorio en función de la configuración interna de reintento.</span><span class="sxs-lookup"><span data-stu-id="e0394-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="e0394-127">El estado del trabajo cambia a **BG_JOB_STATE_ERROR** si el trabajo no puede realizar el progreso (vea [**IBackgroundCopyJob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="e0394-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e0394-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="e0394-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-129">Especifica que el trabajo se ha procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0394-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="e0394-130">Debe llamar al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar la finalización del trabajo y hacer que los archivos estén disponibles para el cliente.</span><span class="sxs-lookup"><span data-stu-id="e0394-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="e0394-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-132">Especifica que se llamó al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que el trabajo se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0394-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="e0394-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="e0394-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="e0394-134">Especifica que se llamó al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo (quitar el trabajo de la cola de transferencia).</span><span class="sxs-lookup"><span data-stu-id="e0394-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0394-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0394-135">Requirements</span></span>



| <span data-ttu-id="e0394-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0394-136">Requirement</span></span> | <span data-ttu-id="e0394-137">Value</span><span class="sxs-lookup"><span data-stu-id="e0394-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0394-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0394-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e0394-139">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0394-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0394-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0394-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e0394-141">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="e0394-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0394-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0394-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0394-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0394-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0394-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0394-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0394-145">**IBackgroundCopyJob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="e0394-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





