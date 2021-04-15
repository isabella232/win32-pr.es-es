---
title: Método IBackgroundCopyJob GetNotifyInterface (Deliveryoptimization. h)
description: Recupera el puntero de interfaz a la implementación de la interfaz IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Método GetNotifyInterface
- Método GetNotifyInterface, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696052"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="6f200-106">IBackgroundCopyJob:: GetNotifyInterface (método)</span><span class="sxs-lookup"><span data-stu-id="6f200-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="6f200-107">Recupera el puntero de interfaz a la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="6f200-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f200-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f200-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="6f200-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f200-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f200-110">*ppNotifyInterface* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f200-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f200-111">Puntero de interfaz a la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="6f200-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="6f200-112">Cuando termine, libere *ppNotifyInterface*.</span><span class="sxs-lookup"><span data-stu-id="6f200-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f200-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f200-113">Return value</span></span>

<span data-ttu-id="6f200-114">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="6f200-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="6f200-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6f200-115">Return code</span></span>                                                                              | <span data-ttu-id="6f200-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f200-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f200-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6f200-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6f200-118">El puntero de la interfaz de notificación se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f200-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f200-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f200-119">Requirements</span></span>



| <span data-ttu-id="6f200-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f200-120">Requirement</span></span> | <span data-ttu-id="6f200-121">Value</span><span class="sxs-lookup"><span data-stu-id="6f200-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f200-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f200-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f200-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f200-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6f200-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f200-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f200-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6f200-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6f200-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f200-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f200-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f200-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f200-128">IDL</span><span class="sxs-lookup"><span data-stu-id="6f200-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f200-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f200-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6f200-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f200-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f200-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f200-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6f200-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f200-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f200-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f200-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6f200-134">IID</span><span class="sxs-lookup"><span data-stu-id="6f200-134">IID</span></span><br/>                      | <span data-ttu-id="6f200-135">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="6f200-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6f200-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f200-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f200-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="6f200-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="6f200-138">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="6f200-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="6f200-139">**IBackgroundCopyJob::GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="6f200-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="6f200-140">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="6f200-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





