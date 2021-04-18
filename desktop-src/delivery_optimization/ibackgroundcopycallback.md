---
title: Interfaz IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implemente la interfaz IBackgroundCopyCallback para recibir la notificación de que un trabajo se ha completado, se ha modificado o tiene un error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714575"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="ef39c-106">Interfaz IBackgroundCopyCallback</span><span class="sxs-lookup"><span data-stu-id="ef39c-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="ef39c-107">Implemente la interfaz **IBackgroundCopyCallback** para recibir la notificación de que un trabajo se ha completado, se ha modificado o tiene un error.</span><span class="sxs-lookup"><span data-stu-id="ef39c-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="ef39c-108">Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="ef39c-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="ef39c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef39c-109">Members</span></span>

<span data-ttu-id="ef39c-110">La interfaz **IBackgroundCopyCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ef39c-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ef39c-111">**IBackgroundCopyCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ef39c-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ef39c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef39c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef39c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef39c-113">Methods</span></span>

<span data-ttu-id="ef39c-114">La interfaz **IBackgroundCopyCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ef39c-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="ef39c-115">Método</span><span class="sxs-lookup"><span data-stu-id="ef39c-115">Method</span></span>                                                                    | <span data-ttu-id="ef39c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef39c-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="ef39c-117">**JobError**</span><span class="sxs-lookup"><span data-stu-id="ef39c-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="ef39c-118">Se le llama cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ef39c-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="ef39c-119">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="ef39c-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="ef39c-120">Se le llama cuando se modifica un trabajo.</span><span class="sxs-lookup"><span data-stu-id="ef39c-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="ef39c-121">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="ef39c-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="ef39c-122">Se le llama cuando todos los archivos del trabajo se han transferido correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef39c-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef39c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef39c-123">Remarks</span></span>

<span data-ttu-id="ef39c-124">Para recibir notificaciones, llame al método [**IBackgroundCopyJob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar el puntero de interfaz a la implementación de **IBackgroundCopyCallback** .</span><span class="sxs-lookup"><span data-stu-id="ef39c-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="ef39c-125">Para especificar las notificaciones que desea recibir, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .</span><span class="sxs-lookup"><span data-stu-id="ef39c-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="ef39c-126">Realizará llamadas a las devoluciones de llamada siempre que el puntero de interfaz sea válido.</span><span class="sxs-lookup"><span data-stu-id="ef39c-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="ef39c-127">La interfaz de notificación ya no es válida cuando finaliza la aplicación; No conserva la interfaz de notificación.</span><span class="sxs-lookup"><span data-stu-id="ef39c-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="ef39c-128">Como resultado, el proceso de inicialización de la aplicación debe llamar al método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) en los trabajos existentes para los que desea recibir la notificación.</span><span class="sxs-lookup"><span data-stu-id="ef39c-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef39c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef39c-129">Requirements</span></span>



| <span data-ttu-id="ef39c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef39c-130">Requirement</span></span> | <span data-ttu-id="ef39c-131">Value</span><span class="sxs-lookup"><span data-stu-id="ef39c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef39c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef39c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ef39c-133">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef39c-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef39c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef39c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ef39c-135">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ef39c-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef39c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef39c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef39c-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef39c-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef39c-138">IDL</span><span class="sxs-lookup"><span data-stu-id="ef39c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef39c-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef39c-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef39c-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef39c-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef39c-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef39c-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ef39c-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef39c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef39c-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef39c-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ef39c-144">IID</span><span class="sxs-lookup"><span data-stu-id="ef39c-144">IID</span></span><br/>                      | <span data-ttu-id="ef39c-145">IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="ef39c-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ef39c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef39c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef39c-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="ef39c-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ef39c-148">**IBackgroundCopyJob::SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="ef39c-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="ef39c-149">**IBackgroundCopyJob::SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="ef39c-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

