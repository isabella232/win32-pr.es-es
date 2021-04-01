---
title: Método complete IBackgroundCopyJob (Deliveryoptimization. h)
description: Finaliza el trabajo y guarda los archivos transferidos en el cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete (método)
- Método complete, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150278"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="db261-106">IBackgroundCopyJob:: Complete (método)</span><span class="sxs-lookup"><span data-stu-id="db261-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="db261-107">Finaliza el trabajo y guarda los archivos transferidos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="db261-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="db261-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db261-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="db261-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db261-109">Parameters</span></span>

<span data-ttu-id="db261-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="db261-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db261-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db261-111">Return value</span></span>

<span data-ttu-id="db261-112">Este método devuelve los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db261-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="db261-113">El método también puede devolver errores relacionados con el cambio de nombre de las copias temporales de los archivos transferidos a sus nombres determinados.</span><span class="sxs-lookup"><span data-stu-id="db261-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="db261-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="db261-114">Return code</span></span>                                                                                          | <span data-ttu-id="db261-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="db261-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db261-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="db261-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="db261-117">Todos los archivos se transfirieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="db261-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="db261-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="db261-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="db261-119">En el caso de las descargas, el estado del trabajo no puede ser BG_JOB_STATE_CANCELLED ni BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="db261-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="db261-120">En el caso de las cargas, el estado del trabajo debe ser BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="db261-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db261-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db261-121">Remarks</span></span>

<span data-ttu-id="db261-122">Todos los archivos se transfirieron correctamente si el estado del trabajo es **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="db261-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="db261-123">Para comprobar el estado del trabajo, llame al método [**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="db261-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="db261-124">También puede implementar la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para recibir notificaciones cuando todos los archivos se hayan transferido al cliente.</span><span class="sxs-lookup"><span data-stu-id="db261-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="db261-125">Conserva los trabajos que solo son inferiores a 30 días.</span><span class="sxs-lookup"><span data-stu-id="db261-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="db261-126">Se quitarán todos los trabajos anteriores.</span><span class="sxs-lookup"><span data-stu-id="db261-126">All older jobs will be removed.</span></span> <span data-ttu-id="db261-127">No admite el directiva de grupo [valor jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) .</span><span class="sxs-lookup"><span data-stu-id="db261-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="db261-128">En el caso de los trabajos de descarga, puede llamar al método **Complete** en cualquier momento durante el proceso de transferencia; sin embargo, solo se guardan los archivos que se transfirieron correctamente al cliente antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="db261-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="db261-129">Por ejemplo, si llama al método **Complete** mientras está procesando el tercer archivo, solo se guardan los dos primeros archivos.</span><span class="sxs-lookup"><span data-stu-id="db261-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="db261-130">Para determinar qué archivos se han transferido, llame al método [**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) y compare el miembro **BytesTransferred** con el miembro **bytesTotal** de la estructura [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="db261-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="db261-131">En el caso de los trabajos de carga, puede llamar al método **Complete** solo cuando el estado del trabajo es **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="db261-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="db261-132">El propietario del archivo es el usuario que realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="db261-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="db261-133">Por ejemplo, si un administrador completa el trabajo de otro usuario, el administrador no es el propietario del trabajo.</span><span class="sxs-lookup"><span data-stu-id="db261-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="db261-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db261-134">Requirements</span></span>



| <span data-ttu-id="db261-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="db261-135">Requirement</span></span> | <span data-ttu-id="db261-136">Value</span><span class="sxs-lookup"><span data-stu-id="db261-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db261-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db261-137">Minimum supported client</span></span><br/> | <span data-ttu-id="db261-138">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="db261-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db261-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db261-139">Minimum supported server</span></span><br/> | <span data-ttu-id="db261-140">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="db261-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="db261-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db261-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="db261-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="db261-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="db261-143">IDL</span><span class="sxs-lookup"><span data-stu-id="db261-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db261-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db261-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="db261-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db261-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="db261-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db261-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="db261-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db261-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db261-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db261-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="db261-149">IID</span><span class="sxs-lookup"><span data-stu-id="db261-149">IID</span></span><br/>                      | <span data-ttu-id="db261-150">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="db261-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="db261-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="db261-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db261-152">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="db261-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="db261-153">**IBackgroundCopyJob:: CANCEL**</span><span class="sxs-lookup"><span data-stu-id="db261-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="db261-154">**IBackgroundCopyJob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="db261-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





