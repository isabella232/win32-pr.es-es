---
title: Método IBackgroundCopyJob GetError (Deliveryoptimization. h)
description: Recupera la interfaz de error después de que se produzca un error.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Método GetError
- Método GetError, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422313"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="9b203-106">IBackgroundCopyJob:: GetError (método)</span><span class="sxs-lookup"><span data-stu-id="9b203-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="9b203-107">Recupera la interfaz de error después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="9b203-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="9b203-108">La optimización de entrega (DO) genera un objeto de error cuando el estado del trabajo es BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9b203-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="9b203-109">El servicio no crea un objeto de error cuando se produce un error en una llamada a un método de interfaz **IBackgroundCopyXXXX** .</span><span class="sxs-lookup"><span data-stu-id="9b203-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="9b203-110">El objeto de error está disponible hasta que comienza la transferencia de datos (el estado del trabajo cambia a BG_JOB_STATE_TRANSFERRING) para el trabajo o hasta que se cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b203-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b203-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b203-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="9b203-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b203-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b203-113">*ppError* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b203-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b203-114">Interfaz de error que proporciona el código de error, una descripción del error y el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="9b203-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="9b203-115">Este parámetro también identifica el archivo que se transfiere en el momento en que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="9b203-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="9b203-116">Suelte *ppError* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="9b203-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b203-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b203-117">Return value</span></span>

<span data-ttu-id="9b203-118">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="9b203-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9b203-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9b203-119">Return code</span></span>                                                                                                           | <span data-ttu-id="9b203-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b203-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b203-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="9b203-122">El objeto de error se generó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b203-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="9b203-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="9b203-124">La interfaz de error solo está disponible después de que se produzca un error (BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR) y antes de que inicien la transferencia de datos (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="9b203-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b203-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b203-125">Remarks</span></span>

<span data-ttu-id="9b203-126">El trabajo se coloca en un estado de error cuando se producen errores irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="9b203-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="9b203-127">Use una de las siguientes opciones para determinar si el trabajo es erróneo:</span><span class="sxs-lookup"><span data-stu-id="9b203-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="9b203-128">Para sondear el estado del trabajo, llame al método [**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="9b203-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="9b203-129">El trabajo es erróneo si el estado es BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9b203-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="9b203-130">Para recibir una notificación cuando se produce un error, implemente la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (concretamente, el método [**JobError**](https://www.bing.com/search?q=**JobError**) ).</span><span class="sxs-lookup"><span data-stu-id="9b203-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="9b203-131">A continuación, llame al método [**IBackgroundCopyJob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para registrar la devolución de llamada y el método [**IBackgroundCopyJob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para establecer la marca de BG_NOTIFY_JOB_ERROR.</span><span class="sxs-lookup"><span data-stu-id="9b203-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="9b203-132">La interfaz [**IBackgroundCopyError**](ibackgroundcopyerror.md) contiene información que se usa para determinar la causa del error y si el proceso de transferencia puede continuar.</span><span class="sxs-lookup"><span data-stu-id="9b203-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="9b203-133">Después de determinar la causa del error, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="9b203-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="9b203-134">Para cancelar el trabajo, llame al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="9b203-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="9b203-135">Para guardar los archivos transferidos correctamente antes de que se produjera el error, llame al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="9b203-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="9b203-136">Para finalizar el procesamiento del trabajo, corrija el problema y, a continuación, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="9b203-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b203-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b203-137">Requirements</span></span>



| <span data-ttu-id="9b203-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b203-138">Requirement</span></span> | <span data-ttu-id="9b203-139">Value</span><span class="sxs-lookup"><span data-stu-id="9b203-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b203-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b203-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9b203-141">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b203-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9b203-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b203-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9b203-143">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="9b203-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9b203-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b203-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b203-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b203-146">IDL</span><span class="sxs-lookup"><span data-stu-id="9b203-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b203-147"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b203-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b203-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b203-149"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9b203-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b203-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b203-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b203-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9b203-152">IID</span><span class="sxs-lookup"><span data-stu-id="9b203-152">IID</span></span><br/>                      | <span data-ttu-id="9b203-153">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="9b203-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9b203-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b203-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b203-155">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="9b203-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9b203-156">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="9b203-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="9b203-157">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="9b203-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="9b203-158">**IBackgroundCopyJob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="9b203-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





