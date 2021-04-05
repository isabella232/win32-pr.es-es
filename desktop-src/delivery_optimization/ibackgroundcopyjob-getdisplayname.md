---
title: Método GetDisplayName IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el nombre para mostrar del trabajo. Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (método)
- GetDisplayName (método), interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996872"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="08b59-107">IBackgroundCopyJob:: GetDisplayName (método)</span><span class="sxs-lookup"><span data-stu-id="08b59-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="08b59-108">Recupera el nombre para mostrar del trabajo.</span><span class="sxs-lookup"><span data-stu-id="08b59-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="08b59-109">Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="08b59-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b59-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08b59-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="08b59-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08b59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b59-112">*ppDisplayName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="08b59-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08b59-113">Cadena terminada en null que contiene el nombre para mostrar que identifica el trabajo.</span><span class="sxs-lookup"><span data-stu-id="08b59-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="08b59-114">Más de un trabajo puede tener el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="08b59-114">More than one job can have the same display name.</span></span> <span data-ttu-id="08b59-115">Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppDisplayName* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="08b59-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b59-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08b59-116">Return value</span></span>

<span data-ttu-id="08b59-117">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="08b59-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="08b59-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="08b59-118">Return code</span></span>                                                                                  | <span data-ttu-id="08b59-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b59-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="08b59-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="08b59-121">El nombre para mostrar se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="08b59-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="08b59-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="08b59-123">El parámetro *ppDisplayName* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="08b59-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="08b59-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b59-124">Requirements</span></span>



| <span data-ttu-id="08b59-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b59-125">Requirement</span></span> | <span data-ttu-id="08b59-126">Value</span><span class="sxs-lookup"><span data-stu-id="08b59-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b59-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b59-127">Minimum supported client</span></span><br/> | <span data-ttu-id="08b59-128">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="08b59-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08b59-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b59-129">Minimum supported server</span></span><br/> | <span data-ttu-id="08b59-130">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="08b59-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="08b59-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08b59-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b59-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="08b59-133">IDL</span><span class="sxs-lookup"><span data-stu-id="08b59-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08b59-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="08b59-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08b59-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="08b59-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="08b59-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08b59-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b59-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b59-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="08b59-139">IID</span><span class="sxs-lookup"><span data-stu-id="08b59-139">IID</span></span><br/>                      | <span data-ttu-id="08b59-140">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="08b59-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="08b59-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b59-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b59-142">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="08b59-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

