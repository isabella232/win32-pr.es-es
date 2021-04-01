---
title: Método IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: La optimización de entrega (DO) llama a la implementación del método JobTransferred cuando todos los archivos del trabajo se han transferido correctamente.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Método JobTransferred
- Método JobTransferred, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150210"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="d69fc-106">IBackgroundCopyCallback:: JobTransferred (método)</span><span class="sxs-lookup"><span data-stu-id="d69fc-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="d69fc-107">La optimización de entrega (DO) llama a la implementación del método **JobTransferred** cuando todos los archivos del trabajo se han transferido correctamente.</span><span class="sxs-lookup"><span data-stu-id="d69fc-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69fc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d69fc-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="d69fc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d69fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69fc-110">*pJob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d69fc-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69fc-111">Contiene información relacionada con el trabajo, como la hora en que se completó el trabajo, el número de bytes transferidos y el número de archivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="d69fc-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="d69fc-112">No libere *pJob*; Libera la interfaz cuando el método devuelve.</span><span class="sxs-lookup"><span data-stu-id="d69fc-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69fc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d69fc-113">Return value</span></span>

<span data-ttu-id="d69fc-114">Este método debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="d69fc-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d69fc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d69fc-115">Remarks</span></span>

<span data-ttu-id="d69fc-116">Normalmente, la implementación debe llamar al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que los archivos se transfirieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="d69fc-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="d69fc-117">Los archivos de descarga y el archivo de respuesta no están disponibles en el cliente hasta que se llama al método **Complete** .</span><span class="sxs-lookup"><span data-stu-id="d69fc-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="d69fc-118">Si no llama al método [**Complete**](ibackgroundcopyjob-complete.md) o el método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) cancela el trabajo después de 30 días y elimina los archivos incompletos.</span><span class="sxs-lookup"><span data-stu-id="d69fc-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69fc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d69fc-119">Requirements</span></span>



| <span data-ttu-id="d69fc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69fc-120">Requirement</span></span> | <span data-ttu-id="d69fc-121">Value</span><span class="sxs-lookup"><span data-stu-id="d69fc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69fc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d69fc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d69fc-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d69fc-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d69fc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d69fc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d69fc-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d69fc-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d69fc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d69fc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69fc-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69fc-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d69fc-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d69fc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d69fc-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d69fc-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d69fc-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d69fc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d69fc-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d69fc-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d69fc-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d69fc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69fc-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d69fc-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d69fc-134">IID</span><span class="sxs-lookup"><span data-stu-id="d69fc-134">IID</span></span><br/>                      | <span data-ttu-id="d69fc-135">IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="d69fc-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d69fc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d69fc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69fc-137">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="d69fc-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="d69fc-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="d69fc-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d69fc-139">**IBackgroundCopyJob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="d69fc-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="d69fc-140">**IBackgroundCopyJob:: CANCEL**</span><span class="sxs-lookup"><span data-stu-id="d69fc-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





