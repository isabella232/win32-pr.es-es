---
title: Método IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica la implementación de la interfaz IBackgroundCopyCallback que se va a realizar. Use la interfaz IBackgroundCopyCallback para recibir notificaciones de eventos relacionados con el trabajo.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Método SetNotifyInterface
- Método SetNotifyInterface, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359722"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="dd5de-107">IBackgroundCopyJob:: SetNotifyInterface (método)</span><span class="sxs-lookup"><span data-stu-id="dd5de-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="dd5de-108">Identifica la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="dd5de-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="dd5de-109">Use la interfaz **IBackgroundCopyCallback** para recibir notificaciones de eventos relacionados con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="dd5de-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5de-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd5de-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="dd5de-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd5de-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5de-112">*pNotifyInterface*</span><span class="sxs-lookup"><span data-stu-id="dd5de-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5de-113">Puntero a la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5de-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="dd5de-114">Para quitar el puntero de interfaz de devolución de llamada actual, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="dd5de-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5de-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd5de-115">Return value</span></span>

<span data-ttu-id="dd5de-116">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="dd5de-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="dd5de-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dd5de-117">Return code</span></span>                                                                              | <span data-ttu-id="dd5de-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd5de-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dd5de-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="dd5de-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="dd5de-120">El puntero de la interfaz de notificación se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd5de-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dd5de-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd5de-121">Remarks</span></span>

<span data-ttu-id="dd5de-122">Llame a este método solo si implementa la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5de-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="dd5de-123">Use el método **SetNotifyInterface** junto con el método [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar el tipo de notificación que desea recibir.</span><span class="sxs-lookup"><span data-stu-id="dd5de-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="dd5de-124">La interfaz de notificación deja de ser válida cuando finaliza la aplicación; No conserva la interfaz de notificación.</span><span class="sxs-lookup"><span data-stu-id="dd5de-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="dd5de-125">Como resultado, el proceso de inicialización de la aplicación debe llamar al método **SetNotifyInterface** en los trabajos existentes para los que desea recibir la notificación.</span><span class="sxs-lookup"><span data-stu-id="dd5de-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="dd5de-126">Si necesita capturar información sobre el estado y el progreso que se produjeron desde la última vez que se ejecutó la aplicación, sondee la información sobre el estado y el progreso durante la inicialización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd5de-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="dd5de-127">Solo el propietario o creador del trabajo o un administrador pueden registrarse para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="dd5de-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5de-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd5de-128">Requirements</span></span>



| <span data-ttu-id="dd5de-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd5de-129">Requirement</span></span> | <span data-ttu-id="dd5de-130">Value</span><span class="sxs-lookup"><span data-stu-id="dd5de-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5de-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5de-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5de-132">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd5de-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd5de-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5de-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5de-134">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="dd5de-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dd5de-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd5de-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd5de-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd5de-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd5de-137">IDL</span><span class="sxs-lookup"><span data-stu-id="dd5de-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd5de-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd5de-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd5de-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd5de-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd5de-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd5de-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="dd5de-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd5de-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd5de-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd5de-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="dd5de-143">IID</span><span class="sxs-lookup"><span data-stu-id="dd5de-143">IID</span></span><br/>                      | <span data-ttu-id="dd5de-144">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="dd5de-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dd5de-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd5de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5de-146">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="dd5de-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="dd5de-147">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="dd5de-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="dd5de-148">**IBackgroundCopyJob::GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="dd5de-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="dd5de-149">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="dd5de-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





