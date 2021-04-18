---
title: Método IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera un trabajo especificado de la cola de transferencia. Normalmente, la aplicación conserva el identificador del trabajo, por lo que posteriormente puede recuperar el trabajo de la cola.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Método GetJob
- Método GetJob, interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, método GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714595"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="c9927-107">IBackgroundCopyManager:: GetJob (método)</span><span class="sxs-lookup"><span data-stu-id="c9927-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="c9927-108">Recupera un trabajo especificado de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="c9927-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="c9927-109">Normalmente, la aplicación conserva el identificador del trabajo, por lo que posteriormente puede recuperar el trabajo de la cola.</span><span class="sxs-lookup"><span data-stu-id="c9927-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9927-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9927-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="c9927-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9927-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9927-112">*JobID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9927-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9927-113">Identifica el trabajo que se va a recuperar de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="c9927-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="c9927-114">El método [**CreateJob**](ibackgroundcopymanager-createjob.md) devuelve el identificador del trabajo.</span><span class="sxs-lookup"><span data-stu-id="c9927-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c9927-115">*ppJob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9927-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9927-116">Un puntero de interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) al trabajo especificado por *JobID*.</span><span class="sxs-lookup"><span data-stu-id="c9927-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="c9927-117">Cuando termine, libere *ppJob*.</span><span class="sxs-lookup"><span data-stu-id="c9927-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9927-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9927-118">Return value</span></span>

<span data-ttu-id="c9927-119">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="c9927-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="c9927-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c9927-120">Return code</span></span>                                                                                      | <span data-ttu-id="c9927-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9927-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9927-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="c9927-123">El trabajo se recuperó correctamente de la cola de transferencia.</span><span class="sxs-lookup"><span data-stu-id="c9927-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="c9927-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c9927-125">No se encontró el trabajo en la cola.</span><span class="sxs-lookup"><span data-stu-id="c9927-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="c9927-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="c9927-127">El usuario no tiene permiso para recuperar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="c9927-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="c9927-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9927-128">Requirements</span></span>



| <span data-ttu-id="c9927-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9927-129">Requirement</span></span> | <span data-ttu-id="c9927-130">Value</span><span class="sxs-lookup"><span data-stu-id="c9927-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9927-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9927-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9927-132">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9927-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9927-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9927-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9927-134">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="c9927-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c9927-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9927-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9927-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9927-137">IDL</span><span class="sxs-lookup"><span data-stu-id="c9927-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9927-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9927-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9927-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9927-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c9927-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9927-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9927-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9927-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c9927-143">IID</span><span class="sxs-lookup"><span data-stu-id="c9927-143">IID</span></span><br/>                      | <span data-ttu-id="c9927-144">IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="c9927-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c9927-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9927-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9927-146">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="c9927-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="c9927-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="c9927-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c9927-148">**IBackgroundCopyJob:: GetId**</span><span class="sxs-lookup"><span data-stu-id="c9927-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="c9927-149">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="c9927-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





