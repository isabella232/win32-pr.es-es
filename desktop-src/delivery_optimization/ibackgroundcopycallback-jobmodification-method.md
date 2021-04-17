---
title: Método IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: La optimización de entrega (DO) llama a la implementación del método JobModification cuando se ha modificado el trabajo.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Método JobModification
- Método JobModification, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714576"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="0384f-106">IBackgroundCopyCallback:: JobModification (método)</span><span class="sxs-lookup"><span data-stu-id="0384f-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="0384f-107">La optimización de entrega (DO) llama a la implementación del método [**JobModification**](https://www.bing.com/search?q=**JobModification**) cuando se ha modificado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="0384f-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="0384f-108">El servicio genera este evento cuando se transfieren bytes, se han agregado archivos al trabajo, se han modificado las propiedades o el estado del trabajo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="0384f-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0384f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0384f-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="0384f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0384f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0384f-111">*pJob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0384f-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0384f-112">Contiene los métodos para tener acceso a la información de la propiedad, el progreso y el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="0384f-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="0384f-113">No libere *pJob*; Libera la interfaz cuando el método [**JobModification**](https://www.bing.com/search?q=**JobModification**) devuelve.</span><span class="sxs-lookup"><span data-stu-id="0384f-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="0384f-114">*dwReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0384f-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0384f-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0384f-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0384f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0384f-116">Return value</span></span>

<span data-ttu-id="0384f-117">Este método debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="0384f-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0384f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0384f-118">Requirements</span></span>



| <span data-ttu-id="0384f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0384f-119">Requirement</span></span> | <span data-ttu-id="0384f-120">Value</span><span class="sxs-lookup"><span data-stu-id="0384f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0384f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0384f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0384f-122">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0384f-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0384f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0384f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0384f-124">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0384f-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0384f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0384f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0384f-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0384f-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0384f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0384f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0384f-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0384f-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0384f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0384f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0384f-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0384f-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0384f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0384f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0384f-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0384f-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0384f-133">IID</span><span class="sxs-lookup"><span data-stu-id="0384f-133">IID</span></span><br/>                      | <span data-ttu-id="0384f-134">IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="0384f-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0384f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0384f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0384f-136">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="0384f-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="0384f-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="0384f-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





