---
title: Método CANCEL IBackgroundCopyJob (Deliveryoptimization. h)
description: Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y del servidor (cargas).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método CANCEL, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método CANCEL
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905186"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="ce660-106">IBackgroundCopyJob:: CANCEL (método)</span><span class="sxs-lookup"><span data-stu-id="ce660-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="ce660-107">Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y del servidor (cargas).</span><span class="sxs-lookup"><span data-stu-id="ce660-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce660-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce660-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="ce660-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce660-109">Parameters</span></span>

<span data-ttu-id="ce660-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce660-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce660-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce660-111">Return value</span></span>

<span data-ttu-id="ce660-112">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="ce660-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ce660-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ce660-113">Return code</span></span>                                                                                          | <span data-ttu-id="ce660-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce660-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce660-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="ce660-116">El trabajo se canceló correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce660-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ce660-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="ce660-118">No se puede cancelar un trabajo cuyo estado sea BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="ce660-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce660-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce660-119">Remarks</span></span>

<span data-ttu-id="ce660-120">Puede cancelar un trabajo en cualquier momento; sin embargo, el trabajo no se puede recuperar una vez cancelado.</span><span class="sxs-lookup"><span data-stu-id="ce660-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce660-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce660-121">Requirements</span></span>



| <span data-ttu-id="ce660-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce660-122">Requirement</span></span> | <span data-ttu-id="ce660-123">Value</span><span class="sxs-lookup"><span data-stu-id="ce660-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce660-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce660-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce660-125">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce660-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce660-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce660-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce660-127">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ce660-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ce660-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce660-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce660-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce660-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ce660-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce660-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ce660-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce660-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce660-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ce660-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce660-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce660-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce660-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ce660-136">IID</span><span class="sxs-lookup"><span data-stu-id="ce660-136">IID</span></span><br/>                      | <span data-ttu-id="ce660-137">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ce660-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ce660-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce660-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce660-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="ce660-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ce660-140">**IBackgroundCopyJob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="ce660-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="ce660-141">**IBackgroundCopyJob:: resume**</span><span class="sxs-lookup"><span data-stu-id="ce660-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="ce660-142">**IBackgroundCopyJob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="ce660-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





