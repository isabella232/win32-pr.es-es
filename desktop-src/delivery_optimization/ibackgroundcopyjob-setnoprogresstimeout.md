---
title: Método IBackgroundCopyJob SetNoProgressTimeout (Deliveryoptimization. h)
description: Establece el período de tiempo durante el cual la optimización de entrega (DO) intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Método SetNoProgressTimeout
- Método SetNoProgressTimeout, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079438"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="3e693-107">IBackgroundCopyJob:: SetNoProgressTimeout (método)</span><span class="sxs-lookup"><span data-stu-id="3e693-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="3e693-108">Establece el período de tiempo durante el cual la optimización de entrega (DO) intenta transferir el archivo después de que se produzca una condición de error transitorio.</span><span class="sxs-lookup"><span data-stu-id="3e693-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="3e693-109">Si hay progreso, se restablece el temporizador.</span><span class="sxs-lookup"><span data-stu-id="3e693-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e693-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e693-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3e693-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e693-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e693-112">*RetryPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e693-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e693-113">Período de tiempo, en segundos, que intenta transferir el archivo después de que no se haya realizado ningún progreso.</span><span class="sxs-lookup"><span data-stu-id="3e693-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="3e693-114">El período de reintento predeterminado para el trabajo de prioridad alta es de 3600 segundos (1 hora) y para el trabajo de prioridad baja es 86400 segundos (24 horas).</span><span class="sxs-lookup"><span data-stu-id="3e693-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e693-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e693-115">Return value</span></span>

<span data-ttu-id="3e693-116">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="3e693-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="3e693-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e693-117">Return code</span></span>                                                                                          | <span data-ttu-id="3e693-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e693-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e693-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="3e693-120">El período de reintento se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e693-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="3e693-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="3e693-122">El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="3e693-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e693-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e693-123">Remarks</span></span>

<span data-ttu-id="3e693-124">Si no realiza el progreso durante el período de reintento, mueve el estado del trabajo de BG_JOB_STATE_TRANSIENT_ERROR a BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="3e693-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="3e693-125">Si solicita la notificación de errores, entonces llama a la devolución de llamada de [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="3e693-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e693-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e693-126">Requirements</span></span>



| <span data-ttu-id="3e693-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e693-127">Requirement</span></span> | <span data-ttu-id="3e693-128">Value</span><span class="sxs-lookup"><span data-stu-id="3e693-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e693-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e693-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3e693-130">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e693-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e693-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e693-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3e693-132">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3e693-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e693-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e693-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e693-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e693-135">IDL</span><span class="sxs-lookup"><span data-stu-id="3e693-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e693-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e693-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e693-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e693-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3e693-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e693-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e693-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3e693-141">IID</span><span class="sxs-lookup"><span data-stu-id="3e693-141">IID</span></span><br/>                      | <span data-ttu-id="3e693-142">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="3e693-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3e693-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e693-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e693-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="3e693-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3e693-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="3e693-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





