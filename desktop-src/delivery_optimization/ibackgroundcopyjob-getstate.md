---
title: Método IBackgroundCopyJob GetState (Deliveryoptimization. h)
description: Recupera el estado del trabajo.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Método GetState
- Método GetState, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802438"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="ba66a-106">IBackgroundCopyJob:: GetState (método)</span><span class="sxs-lookup"><span data-stu-id="ba66a-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="ba66a-107">Recupera el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="ba66a-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba66a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba66a-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="ba66a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba66a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba66a-110">*pJobState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ba66a-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba66a-111">Estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="ba66a-111">The state of the job.</span></span> <span data-ttu-id="ba66a-112">Por ejemplo, el estado refleja si el trabajo es un error, si se transfieren datos o si se suspende.</span><span class="sxs-lookup"><span data-stu-id="ba66a-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="ba66a-113">Para obtener una lista de Estados de trabajo, consulte la enumeración [**BG_JOB_STATE**](bg-job-state-.md) .</span><span class="sxs-lookup"><span data-stu-id="ba66a-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba66a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba66a-114">Return value</span></span>

<span data-ttu-id="ba66a-115">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="ba66a-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ba66a-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ba66a-116">Return code</span></span>                                                                              | <span data-ttu-id="ba66a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba66a-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="ba66a-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ba66a-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="ba66a-119">El estado del trabajo se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba66a-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba66a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba66a-120">Remarks</span></span>

<span data-ttu-id="ba66a-121">Si desea saber cuándo se produce un error en un trabajo o si ha transferido todos los archivos en el trabajo, puede usar este método para sondear el estado del trabajo o puede registrarse para recibir notificaciones cuando se produzcan eventos.</span><span class="sxs-lookup"><span data-stu-id="ba66a-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="ba66a-122">Para más información sobre el registro para recibir notificaciones de eventos, consulte la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="ba66a-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba66a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba66a-123">Requirements</span></span>



| <span data-ttu-id="ba66a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba66a-124">Requirement</span></span> | <span data-ttu-id="ba66a-125">Value</span><span class="sxs-lookup"><span data-stu-id="ba66a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba66a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba66a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba66a-127">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba66a-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ba66a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba66a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba66a-129">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ba66a-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ba66a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba66a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba66a-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba66a-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba66a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ba66a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba66a-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba66a-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ba66a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba66a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba66a-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba66a-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ba66a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba66a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba66a-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba66a-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ba66a-138">IID</span><span class="sxs-lookup"><span data-stu-id="ba66a-138">IID</span></span><br/>                      | <span data-ttu-id="ba66a-139">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ba66a-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ba66a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba66a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba66a-141">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="ba66a-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ba66a-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="ba66a-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="ba66a-143">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="ba66a-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





