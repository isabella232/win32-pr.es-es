---
title: Método IBackgroundCopyJob GetProgress (Deliveryoptimization. h)
description: Recupera información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Método GetProgress
- Método GetProgress, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150377"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="b85b9-106">IBackgroundCopyJob:: GetProgress (método)</span><span class="sxs-lookup"><span data-stu-id="b85b9-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="b85b9-107">Recupera información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="b85b9-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b85b9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b85b9-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="b85b9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b85b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b85b9-110">*pProgress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b85b9-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b85b9-111">Contiene datos que se pueden usar para calcular el porcentaje del trabajo que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="b85b9-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b85b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b85b9-112">Return value</span></span>

<span data-ttu-id="b85b9-113">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="b85b9-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b85b9-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b85b9-114">Return code</span></span>                                                                              | <span data-ttu-id="b85b9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b85b9-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="b85b9-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b85b9-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b85b9-117">La información de progreso se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b85b9-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b85b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b85b9-118">Requirements</span></span>



| <span data-ttu-id="b85b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b85b9-119">Requirement</span></span> | <span data-ttu-id="b85b9-120">Value</span><span class="sxs-lookup"><span data-stu-id="b85b9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b85b9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b85b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b85b9-122">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b85b9-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b85b9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b85b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b85b9-124">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="b85b9-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b85b9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b85b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b85b9-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b85b9-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b85b9-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b85b9-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b85b9-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b85b9-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b85b9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b85b9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b85b9-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b85b9-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b85b9-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b85b9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b85b9-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b85b9-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b85b9-133">IID</span><span class="sxs-lookup"><span data-stu-id="b85b9-133">IID</span></span><br/>                      | <span data-ttu-id="b85b9-134">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="b85b9-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b85b9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b85b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b85b9-136">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="b85b9-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





