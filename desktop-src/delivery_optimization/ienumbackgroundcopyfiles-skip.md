---
title: IEnumBackgroundCopyFiles SKIP (método) (Deliveryoptimization. h)
description: Omite el siguiente número de elementos especificado en la secuencia de enumeración. Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, se omite el último elemento de la secuencia.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (método)
- SKIP (método), IEnumBackgroundCopyFiles (interfaz)
- IEnumBackgroundCopyFiles (interfaz), SKIP (método)
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079016"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="be24f-107">IEnumBackgroundCopyFiles:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="be24f-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="be24f-108">Omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="be24f-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="be24f-109">Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, se omite el último elemento de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="be24f-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="be24f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be24f-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="be24f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be24f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be24f-112">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be24f-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be24f-113">Número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="be24f-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be24f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be24f-114">Return value</span></span>

<span data-ttu-id="be24f-115">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="be24f-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="be24f-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="be24f-116">Return code</span></span>                                                                              | <span data-ttu-id="be24f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="be24f-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="be24f-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="be24f-119">Se omitió correctamente el número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="be24f-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="be24f-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="be24f-121">Se omitió un valor menor que el número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="be24f-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="be24f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be24f-122">Requirements</span></span>



| <span data-ttu-id="be24f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be24f-123">Requirement</span></span> | <span data-ttu-id="be24f-124">Value</span><span class="sxs-lookup"><span data-stu-id="be24f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be24f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be24f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be24f-126">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="be24f-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="be24f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be24f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be24f-128">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="be24f-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be24f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be24f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be24f-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="be24f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="be24f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be24f-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="be24f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be24f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="be24f-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="be24f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be24f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be24f-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be24f-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="be24f-137">IID</span><span class="sxs-lookup"><span data-stu-id="be24f-137">IID</span></span><br/>                      | <span data-ttu-id="be24f-138">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="be24f-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="be24f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="be24f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be24f-140">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="be24f-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





