---
title: Método GetType IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el tipo de transferencia que se realiza, por ejemplo, una descarga o carga de archivos.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType (método)
- Método GetType, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079017"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="3e60e-106">IBackgroundCopyJob:: GetType (método)</span><span class="sxs-lookup"><span data-stu-id="3e60e-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="3e60e-107">Recupera el tipo de transferencia que se realiza, por ejemplo, una descarga o carga de archivos.</span><span class="sxs-lookup"><span data-stu-id="3e60e-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e60e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e60e-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="3e60e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e60e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e60e-110">*pJobType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3e60e-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e60e-111">Tipo de transferencia que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="3e60e-111">Type of transfer being performed.</span></span> <span data-ttu-id="3e60e-112">Para obtener una lista de tipos de transferencia, vea la enumeración [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="3e60e-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e60e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e60e-113">Return value</span></span>

<span data-ttu-id="3e60e-114">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="3e60e-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="3e60e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e60e-115">Return code</span></span>                                                                              | <span data-ttu-id="3e60e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e60e-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3e60e-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3e60e-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="3e60e-118">El tipo de transferencia se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e60e-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e60e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e60e-119">Remarks</span></span>

<span data-ttu-id="3e60e-120">Especifique el tipo de transferencia al crear el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3e60e-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e60e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e60e-121">Requirements</span></span>



| <span data-ttu-id="3e60e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e60e-122">Requirement</span></span> | <span data-ttu-id="3e60e-123">Value</span><span class="sxs-lookup"><span data-stu-id="3e60e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e60e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e60e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3e60e-125">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e60e-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e60e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e60e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3e60e-127">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3e60e-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e60e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e60e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e60e-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e60e-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e60e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="3e60e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e60e-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e60e-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e60e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e60e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e60e-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e60e-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3e60e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e60e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e60e-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e60e-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3e60e-136">IID</span><span class="sxs-lookup"><span data-stu-id="3e60e-136">IID</span></span><br/>                      | <span data-ttu-id="3e60e-137">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="3e60e-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3e60e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e60e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e60e-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="3e60e-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3e60e-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="3e60e-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="3e60e-141">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="3e60e-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





