---
title: Método IBackgroundCopyJob GetNotifyFlags (Deliveryoptimization. h)
description: Recupera las marcas de notificación de eventos para el trabajo.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Método GetNotifyFlags
- Método GetNotifyFlags, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359733"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="1c6b3-106">IBackgroundCopyJob:: GetNotifyFlags (método)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="1c6b3-107">Recupera las marcas de notificación de eventos para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6b3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c6b3-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1c6b3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c6b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6b3-110">*pNotifyFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c6b3-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6b3-111">Identifica los eventos que recibe la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="1c6b3-112">En la tabla siguiente se enumeran los valores de marca de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="1c6b3-113">Value</span><span class="sxs-lookup"><span data-stu-id="1c6b3-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="1c6b3-114">Significado</span><span class="sxs-lookup"><span data-stu-id="1c6b3-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="1c6b3-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="1c6b3-116">Todos los archivos del trabajo se han transferido.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="1c6b3-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="1c6b3-118">Se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="1c6b3-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="1c6b3-120">La notificación de eventos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-120">Event notification is disabled.</span></span> <span data-ttu-id="1c6b3-121">Si se establece, se omiten las demás marcas.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="1c6b3-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="1c6b3-123">El trabajo se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6b3-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c6b3-124">Return value</span></span>

<span data-ttu-id="1c6b3-125">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="1c6b3-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1c6b3-126">Return code</span></span>                                                                              | <span data-ttu-id="1c6b3-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c6b3-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="1c6b3-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="1c6b3-129">Las marcas de notificación de eventos se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c6b3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c6b3-130">Requirements</span></span>



| <span data-ttu-id="1c6b3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c6b3-131">Requirement</span></span> | <span data-ttu-id="1c6b3-132">Value</span><span class="sxs-lookup"><span data-stu-id="1c6b3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6b3-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c6b3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6b3-134">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c6b3-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1c6b3-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c6b3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6b3-136">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="1c6b3-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1c6b3-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c6b3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c6b3-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c6b3-139">IDL</span><span class="sxs-lookup"><span data-stu-id="1c6b3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c6b3-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1c6b3-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c6b3-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c6b3-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1c6b3-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c6b3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c6b3-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c6b3-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1c6b3-145">IID</span><span class="sxs-lookup"><span data-stu-id="1c6b3-145">IID</span></span><br/>                      | <span data-ttu-id="1c6b3-146">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="1c6b3-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1c6b3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c6b3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6b3-148">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="1c6b3-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="1c6b3-149">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="1c6b3-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="1c6b3-150">**IBackgroundCopyJob::GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="1c6b3-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="1c6b3-151">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="1c6b3-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





