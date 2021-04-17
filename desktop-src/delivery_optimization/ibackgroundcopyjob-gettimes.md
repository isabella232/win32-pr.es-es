---
title: Método IBackgroundCopyJob GetTimes (Deliveryoptimization. h)
description: Recupera las marcas de tiempo relacionadas con el trabajo, como la hora en que se creó o modificó por última vez el trabajo.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Método GetTimes
- Método GetTimes, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetTimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490924"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="03e91-106">IBackgroundCopyJob:: GetTimes (método)</span><span class="sxs-lookup"><span data-stu-id="03e91-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="03e91-107">Recupera las marcas de tiempo relacionadas con el trabajo, como la hora en que se creó o modificó por última vez el trabajo.</span><span class="sxs-lookup"><span data-stu-id="03e91-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e91-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03e91-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="03e91-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03e91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03e91-110">*pTimes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="03e91-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03e91-111">Contiene marcas de tiempo relacionadas con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="03e91-111">Contains job-related time stamps.</span></span> <span data-ttu-id="03e91-112">Para obtener las marcas de tiempo disponibles, consulte la estructura [**BG_JOB_TIMES**](bg-job-times.md) .</span><span class="sxs-lookup"><span data-stu-id="03e91-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03e91-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03e91-113">Return value</span></span>

<span data-ttu-id="03e91-114">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="03e91-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="03e91-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="03e91-115">Return code</span></span>                                                                              | <span data-ttu-id="03e91-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="03e91-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="03e91-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="03e91-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="03e91-118">Las marcas de tiempo se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="03e91-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="03e91-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03e91-119">Requirements</span></span>



| <span data-ttu-id="03e91-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e91-120">Requirement</span></span> | <span data-ttu-id="03e91-121">Value</span><span class="sxs-lookup"><span data-stu-id="03e91-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e91-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e91-122">Minimum supported client</span></span><br/> | <span data-ttu-id="03e91-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="03e91-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03e91-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e91-124">Minimum supported server</span></span><br/> | <span data-ttu-id="03e91-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="03e91-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="03e91-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03e91-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="03e91-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e91-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="03e91-128">IDL</span><span class="sxs-lookup"><span data-stu-id="03e91-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03e91-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03e91-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="03e91-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03e91-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="03e91-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03e91-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="03e91-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03e91-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03e91-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03e91-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="03e91-134">IID</span><span class="sxs-lookup"><span data-stu-id="03e91-134">IID</span></span><br/>                      | <span data-ttu-id="03e91-135">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="03e91-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="03e91-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e91-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="03e91-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="03e91-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="03e91-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





