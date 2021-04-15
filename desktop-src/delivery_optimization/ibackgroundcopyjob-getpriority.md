---
title: Método IBackgroundCopyJob GetPriority ((Deliveryoptimization. h)
description: Recupera el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Método GetPriority (
- Método GetPriority (, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetPriority (
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695946"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="f5d57-107">IBackgroundCopyJob:: GetPriority ((método)</span><span class="sxs-lookup"><span data-stu-id="f5d57-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="f5d57-108">Recupera el nivel de prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f5d57-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="f5d57-109">El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="f5d57-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d57-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d57-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="f5d57-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5d57-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d57-112">*pPriority* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f5d57-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d57-113">Prioridad del trabajo en relación con otros trabajos de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="f5d57-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d57-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d57-114">Return value</span></span>

<span data-ttu-id="f5d57-115">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="f5d57-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="f5d57-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d57-116">Return code</span></span>                                                                              | <span data-ttu-id="f5d57-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5d57-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="f5d57-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f5d57-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f5d57-119">El nivel de prioridad se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5d57-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f5d57-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d57-120">Requirements</span></span>



| <span data-ttu-id="f5d57-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d57-121">Requirement</span></span> | <span data-ttu-id="f5d57-122">Value</span><span class="sxs-lookup"><span data-stu-id="f5d57-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d57-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d57-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d57-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5d57-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f5d57-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d57-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d57-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="f5d57-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f5d57-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5d57-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d57-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d57-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5d57-129">IDL</span><span class="sxs-lookup"><span data-stu-id="f5d57-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5d57-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5d57-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f5d57-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5d57-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5d57-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5d57-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f5d57-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5d57-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d57-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d57-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f5d57-135">IID</span><span class="sxs-lookup"><span data-stu-id="f5d57-135">IID</span></span><br/>                      | <span data-ttu-id="f5d57-136">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="f5d57-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f5d57-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d57-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d57-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="f5d57-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="f5d57-139">**IBackgroundCopyJob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="f5d57-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





