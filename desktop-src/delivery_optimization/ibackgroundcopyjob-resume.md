---
title: Método de reanudación de IBackgroundCopyJob (Deliveryoptimization. h)
description: Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Método Resume
- Método resume, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150074"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="74b92-106">IBackgroundCopyJob:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="74b92-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="74b92-107">Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.</span><span class="sxs-lookup"><span data-stu-id="74b92-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b92-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74b92-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="74b92-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74b92-109">Parameters</span></span>

<span data-ttu-id="74b92-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="74b92-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74b92-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74b92-111">Return value</span></span>

<span data-ttu-id="74b92-112">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="74b92-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="74b92-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="74b92-113">Return code</span></span>                                                                                          | <span data-ttu-id="74b92-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="74b92-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74b92-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="74b92-116">El trabajo se ha reiniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="74b92-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="74b92-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="74b92-118">No hay archivos para transferir.</span><span class="sxs-lookup"><span data-stu-id="74b92-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="74b92-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="74b92-120">El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="74b92-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74b92-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74b92-121">Remarks</span></span>

<span data-ttu-id="74b92-122">Al crear un trabajo, el trabajo se suspende inicialmente.</span><span class="sxs-lookup"><span data-stu-id="74b92-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="74b92-123">La llamada a **resume** mueve el trabajo al estado transfiriendo.</span><span class="sxs-lookup"><span data-stu-id="74b92-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="74b92-124">Tenga en cuenta que el trabajo debe contener uno o más archivos antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="74b92-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="74b92-125">Si un trabajo se encuentra en el estado BG_JOB_STATE_TRANSIENT_ERROR o BG_JOB_STATE_ERROR, llame al método **resume** para reiniciar el trabajo después de corregir el error.</span><span class="sxs-lookup"><span data-stu-id="74b92-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b92-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b92-126">Requirements</span></span>



| <span data-ttu-id="74b92-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b92-127">Requirement</span></span> | <span data-ttu-id="74b92-128">Value</span><span class="sxs-lookup"><span data-stu-id="74b92-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b92-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b92-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74b92-130">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="74b92-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="74b92-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b92-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74b92-132">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="74b92-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="74b92-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74b92-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="74b92-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="74b92-135">IDL</span><span class="sxs-lookup"><span data-stu-id="74b92-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74b92-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="74b92-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74b92-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="74b92-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="74b92-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74b92-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b92-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b92-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="74b92-141">IID</span><span class="sxs-lookup"><span data-stu-id="74b92-141">IID</span></span><br/>                      | <span data-ttu-id="74b92-142">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="74b92-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="74b92-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="74b92-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b92-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="74b92-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="74b92-145">**IBackgroundCopyJob:: CANCEL**</span><span class="sxs-lookup"><span data-stu-id="74b92-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="74b92-146">**IBackgroundCopyJob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="74b92-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





