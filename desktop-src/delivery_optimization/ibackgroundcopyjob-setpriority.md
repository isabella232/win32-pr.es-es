---
title: Método SetPriority IBackgroundCopyJob (Deliveryoptimization. h)
description: Especifica el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority (método)
- Método SetPriority, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802437"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="30546-107">IBackgroundCopyJob:: SetPriority (método)</span><span class="sxs-lookup"><span data-stu-id="30546-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="30546-108">Especifica el nivel de prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="30546-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="30546-109">El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="30546-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="30546-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30546-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="30546-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30546-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30546-112">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="30546-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30546-113">Especifica el nivel de prioridad del trabajo en relación con otros trabajos de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="30546-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="30546-114">El valor predeterminado es BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="30546-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="30546-115">Para obtener una lista de los niveles de prioridad, vea la enumeración [**BG_JOB_PRIORITY**](bg-job-priority-.md) .</span><span class="sxs-lookup"><span data-stu-id="30546-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30546-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30546-116">Return value</span></span>

<span data-ttu-id="30546-117">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="30546-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="30546-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30546-118">Return code</span></span>                                                                              | <span data-ttu-id="30546-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="30546-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="30546-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="30546-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="30546-121">La prioridad del trabajo se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="30546-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30546-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30546-122">Requirements</span></span>



| <span data-ttu-id="30546-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30546-123">Requirement</span></span> | <span data-ttu-id="30546-124">Value</span><span class="sxs-lookup"><span data-stu-id="30546-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30546-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30546-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30546-126">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="30546-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="30546-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30546-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30546-128">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="30546-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30546-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30546-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="30546-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="30546-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="30546-131">IDL</span><span class="sxs-lookup"><span data-stu-id="30546-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30546-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30546-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="30546-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30546-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="30546-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30546-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="30546-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30546-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30546-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30546-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="30546-137">IID</span><span class="sxs-lookup"><span data-stu-id="30546-137">IID</span></span><br/>                      | <span data-ttu-id="30546-138">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="30546-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="30546-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="30546-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30546-140">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="30546-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="30546-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="30546-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="30546-142">**IBackgroundCopyJob:: GetPriority (**</span><span class="sxs-lookup"><span data-stu-id="30546-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





