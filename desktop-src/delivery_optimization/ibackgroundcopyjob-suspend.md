---
title: Método Suspend de IBackgroundCopyJob (Deliveryoptimization. h)
description: Suspende un trabajo. Los nuevos trabajos, los trabajos que tienen errores y los trabajos que han terminado de transferir archivos se suspenden automáticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Método Suspend
- Método Suspend, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422311"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="d5f5d-107">IBackgroundCopyJob:: Suspend (método)</span><span class="sxs-lookup"><span data-stu-id="d5f5d-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="d5f5d-108">Suspende un trabajo.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-108">Suspends a job.</span></span> <span data-ttu-id="d5f5d-109">Los nuevos trabajos, los trabajos que tienen errores y los trabajos que han terminado de transferir archivos se suspenden automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f5d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5f5d-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="d5f5d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5f5d-111">Parameters</span></span>

<span data-ttu-id="d5f5d-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5f5d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5f5d-113">Return value</span></span>

<span data-ttu-id="d5f5d-114">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="d5f5d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d5f5d-115">Return code</span></span>                                                                                          | <span data-ttu-id="d5f5d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5f5d-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5f5d-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="d5f5d-118">El trabajo se suspendió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="d5f5d-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="d5f5d-120">El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="d5f5d-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5f5d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f5d-121">Requirements</span></span>



| <span data-ttu-id="d5f5d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f5d-122">Requirement</span></span> | <span data-ttu-id="d5f5d-123">Value</span><span class="sxs-lookup"><span data-stu-id="d5f5d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f5d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5f5d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f5d-125">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5f5d-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5f5d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5f5d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f5d-127">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d5f5d-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d5f5d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5f5d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f5d-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5f5d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d5f5d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5f5d-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d5f5d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5f5d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5f5d-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d5f5d-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5f5d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f5d-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5d-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d5f5d-136">IID</span><span class="sxs-lookup"><span data-stu-id="d5f5d-136">IID</span></span><br/>                      | <span data-ttu-id="d5f5d-137">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="d5f5d-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d5f5d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5f5d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f5d-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="d5f5d-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d5f5d-140">**IBackgroundCopyJob:: CANCEL**</span><span class="sxs-lookup"><span data-stu-id="d5f5d-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="d5f5d-141">**IBackgroundCopyJob:: resume**</span><span class="sxs-lookup"><span data-stu-id="d5f5d-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





