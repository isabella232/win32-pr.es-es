---
title: Método IBackgroundCopyJob SetNotifyFlags (Deliveryoptimization. h)
description: Especifica el tipo de notificación de eventos que desea recibir, como los eventos transferidos del trabajo.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Método SetNotifyFlags
- Método SetNotifyFlags, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534234"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="d50dc-106">IBackgroundCopyJob:: SetNotifyFlags (método)</span><span class="sxs-lookup"><span data-stu-id="d50dc-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="d50dc-107">Especifica el tipo de notificación de eventos que desea recibir, como los eventos transferidos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d50dc-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d50dc-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d50dc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d50dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50dc-110">*NotifyFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d50dc-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d50dc-111">Establezca una o varias de las marcas siguientes para identificar los eventos que desea recibir.</span><span class="sxs-lookup"><span data-stu-id="d50dc-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="d50dc-112">Value</span><span class="sxs-lookup"><span data-stu-id="d50dc-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="d50dc-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d50dc-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="d50dc-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="d50dc-115">Todos los archivos del trabajo se han transferido.</span><span class="sxs-lookup"><span data-stu-id="d50dc-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="d50dc-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="d50dc-117">Se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="d50dc-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="d50dc-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="d50dc-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="d50dc-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="d50dc-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="d50dc-121">El trabajo se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="d50dc-121">The job has been modified.</span></span> <span data-ttu-id="d50dc-122">Por ejemplo, un valor de propiedad cambiado, el estado del trabajo ha cambiado o el progreso se realiza transfiriendo los archivos.</span><span class="sxs-lookup"><span data-stu-id="d50dc-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="d50dc-123">Esta marca se omite si se especifica la notificación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d50dc-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="d50dc-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="d50dc-125">Se ha transferido un archivo en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d50dc-125">A file in the job has been transferred.</span></span> <span data-ttu-id="d50dc-126">Esta marca se omite si se especifica la notificación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d50dc-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="d50dc-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="d50dc-128">No se admite.</span><span class="sxs-lookup"><span data-stu-id="d50dc-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d50dc-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d50dc-129">Return value</span></span>

<span data-ttu-id="d50dc-130">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="d50dc-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="d50dc-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d50dc-131">Return code</span></span>                                                                                          | <span data-ttu-id="d50dc-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d50dc-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d50dc-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="d50dc-134">El tipo de notificación de eventos se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="d50dc-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="d50dc-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="d50dc-136">El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="d50dc-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d50dc-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d50dc-137">Remarks</span></span>

<span data-ttu-id="d50dc-138">Use el método **SetNotifyFlags** junto con [**IBackgroundCopyJob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span><span class="sxs-lookup"><span data-stu-id="d50dc-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d50dc-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d50dc-139">Requirements</span></span>



| <span data-ttu-id="d50dc-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50dc-140">Requirement</span></span> | <span data-ttu-id="d50dc-141">Value</span><span class="sxs-lookup"><span data-stu-id="d50dc-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50dc-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d50dc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d50dc-143">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d50dc-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d50dc-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d50dc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d50dc-145">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d50dc-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d50dc-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d50dc-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d50dc-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d50dc-148">IDL</span><span class="sxs-lookup"><span data-stu-id="d50dc-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d50dc-149"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d50dc-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d50dc-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="d50dc-151"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d50dc-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d50dc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d50dc-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d50dc-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d50dc-154">IID</span><span class="sxs-lookup"><span data-stu-id="d50dc-154">IID</span></span><br/>                      | <span data-ttu-id="d50dc-155">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="d50dc-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d50dc-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="d50dc-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50dc-157">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="d50dc-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d50dc-158">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="d50dc-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="d50dc-159">**IBackgroundCopyJob::GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="d50dc-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="d50dc-160">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="d50dc-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





