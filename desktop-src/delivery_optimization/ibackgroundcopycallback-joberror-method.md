---
title: Método IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: La optimización de entrega (DO) llama a la implementación del método JobError cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Método JobError
- Método JobError, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422242"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="5b0fe-106">IBackgroundCopyCallback:: JobError (método)</span><span class="sxs-lookup"><span data-stu-id="5b0fe-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="5b0fe-107">La optimización de entrega (DO) llama a la implementación del método [**JobError**](https://www.bing.com/search?q=**JobError**) cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0fe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b0fe-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="5b0fe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b0fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0fe-110">*pJob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b0fe-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fe-111">Contiene información relacionada con el trabajo, como el número de bytes y archivos transferidos antes de que se produjera el error.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="5b0fe-112">También contiene los métodos para reanudar y cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="5b0fe-113">No libere *pJob*; Libera la interfaz cuando el método [**JobError**](https://www.bing.com/search?q=**JobError**) devuelve.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="5b0fe-114">*perror* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b0fe-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0fe-115">Contiene información de error, como el archivo que se está procesando en el momento en que se produjo el error irrecuperable y una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="5b0fe-116">No liberar el *perror*; Libera la interfaz cuando el método [**JobError**](https://www.bing.com/search?q=**JobError**) devuelve.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0fe-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b0fe-117">Return value</span></span>

<span data-ttu-id="5b0fe-118">Este método debe devolver **S_OK**; de lo contrario, sigue llamando a este método hasta que se devuelva **S_OK** .</span><span class="sxs-lookup"><span data-stu-id="5b0fe-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="5b0fe-119">Por motivos de rendimiento, debe limitar el número de veces que se devuelve un valor distinto de **S_OK** a varias veces.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="5b0fe-120">Como alternativa a la devolución de un código de error, considere la posibilidad de devolver siempre **S_OK** y de controlar el error internamente.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="5b0fe-121">El intervalo en el que se llama a este método es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0fe-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b0fe-122">Remarks</span></span>

<span data-ttu-id="5b0fe-123">Después de determinar la causa del error, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5b0fe-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="5b0fe-124">Para cancelar el trabajo, llame al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0fe-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="5b0fe-125">Para aceptar la parte del trabajo que se transfirió correctamente antes de que se produjera el error, llame al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0fe-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="5b0fe-126">Esta opción no se aplica a los trabajos de carga; no se puede completar una parte de un trabajo de carga.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="5b0fe-127">Para finalizar el procesamiento del trabajo, corrija el problema y, a continuación, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0fe-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="5b0fe-128">Los errores transitorios no generan llamadas al método [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="5b0fe-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="5b0fe-129">Devuelve BG_ERROR_CONTEXT_REMOTE_FILE si el trabajo ha alcanzado un error HTTP 403, BG_ERROR_CONTEXT_NONE de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5b0fe-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0fe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b0fe-130">Requirements</span></span>



| <span data-ttu-id="5b0fe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0fe-131">Requirement</span></span> | <span data-ttu-id="5b0fe-132">Value</span><span class="sxs-lookup"><span data-stu-id="5b0fe-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0fe-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b0fe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5b0fe-134">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b0fe-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b0fe-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b0fe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5b0fe-136">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="5b0fe-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b0fe-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b0fe-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b0fe-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fe-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b0fe-139">IDL</span><span class="sxs-lookup"><span data-stu-id="5b0fe-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b0fe-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fe-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5b0fe-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b0fe-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b0fe-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fe-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5b0fe-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b0fe-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b0fe-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fe-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5b0fe-145">IID</span><span class="sxs-lookup"><span data-stu-id="5b0fe-145">IID</span></span><br/>                      | <span data-ttu-id="5b0fe-146">IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="5b0fe-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5b0fe-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b0fe-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0fe-148">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="5b0fe-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="5b0fe-149">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="5b0fe-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="5b0fe-150">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="5b0fe-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5b0fe-151">**IBackgroundCopyJob:: CANCEL**</span><span class="sxs-lookup"><span data-stu-id="5b0fe-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="5b0fe-152">**IBackgroundCopyJob:: resume**</span><span class="sxs-lookup"><span data-stu-id="5b0fe-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





