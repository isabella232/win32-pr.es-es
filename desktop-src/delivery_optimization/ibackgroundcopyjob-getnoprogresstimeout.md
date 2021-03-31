---
title: Método IBackgroundCopyJob GetNoProgressTimeout (Deliveryoptimization. h)
description: Recupera la cantidad de tiempo que el servicio intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Método GetNoProgressTimeout
- Método GetNoProgressTimeout, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490925"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="7e8a4-107">IBackgroundCopyJob:: GetNoProgressTimeout (método)</span><span class="sxs-lookup"><span data-stu-id="7e8a4-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="7e8a4-108">Recupera la cantidad de tiempo que el servicio intenta transferir el archivo después de que se produzca una condición de error transitorio.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="7e8a4-109">Si hay progreso, se restablece el temporizador.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8a4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e8a4-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="7e8a4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e8a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e8a4-112">*pRetryPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e8a4-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e8a4-113">Período de tiempo, en segundos, que el servicio intenta transferir el archivo después de que se produzca un error transitorio.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e8a4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e8a4-114">Return value</span></span>

<span data-ttu-id="7e8a4-115">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="7e8a4-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7e8a4-116">Return code</span></span>                                                                              | <span data-ttu-id="7e8a4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e8a4-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7e8a4-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7e8a4-119">Se recuperó correctamente el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="7e8a4-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7e8a4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e8a4-120">Requirements</span></span>



| <span data-ttu-id="7e8a4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e8a4-121">Requirement</span></span> | <span data-ttu-id="7e8a4-122">Value</span><span class="sxs-lookup"><span data-stu-id="7e8a4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8a4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e8a4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7e8a4-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e8a4-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e8a4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e8a4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7e8a4-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="7e8a4-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7e8a4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e8a4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e8a4-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e8a4-129">IDL</span><span class="sxs-lookup"><span data-stu-id="7e8a4-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e8a4-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7e8a4-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e8a4-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e8a4-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7e8a4-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e8a4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e8a4-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e8a4-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7e8a4-135">IID</span><span class="sxs-lookup"><span data-stu-id="7e8a4-135">IID</span></span><br/>                      | <span data-ttu-id="7e8a4-136">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="7e8a4-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7e8a4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e8a4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8a4-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="7e8a4-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="7e8a4-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





