---
title: Método Next IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un número especificado de elementos en la secuencia de enumeración. Si hay menos del número solicitado de elementos que quedan en la secuencia, recupera los elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Método Next
- Método siguiente, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996869"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="756fa-107">IEnumBackgroundCopyFiles:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="756fa-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="756fa-108">Recupera un número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="756fa-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="756fa-109">Si hay menos del número solicitado de elementos que quedan en la secuencia, recupera los elementos restantes.</span><span class="sxs-lookup"><span data-stu-id="756fa-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="756fa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="756fa-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="756fa-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="756fa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="756fa-112">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="756fa-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="756fa-113">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="756fa-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="756fa-114">*rgelt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="756fa-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="756fa-115">Matriz de objetos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="756fa-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="756fa-116">Debe liberar cada objeto en *rgelt* cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="756fa-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="756fa-117">*pceltFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="756fa-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="756fa-118">Número de elementos devueltos en *rgelt*.</span><span class="sxs-lookup"><span data-stu-id="756fa-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="756fa-119">Puede establecer *pceltFetched* en **null** si *Celt* es uno.</span><span class="sxs-lookup"><span data-stu-id="756fa-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="756fa-120">De lo contrario, inicialice el valor de *pceltFetched* en 0 antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="756fa-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="756fa-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="756fa-121">Return value</span></span>

<span data-ttu-id="756fa-122">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="756fa-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="756fa-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="756fa-123">Return code</span></span>                                                                              | <span data-ttu-id="756fa-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="756fa-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="756fa-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="756fa-126">El número de elementos solicitados se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="756fa-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="756fa-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="756fa-128">Devuelve un valor menor que el número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="756fa-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="756fa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756fa-129">Requirements</span></span>



| <span data-ttu-id="756fa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="756fa-130">Requirement</span></span> | <span data-ttu-id="756fa-131">Value</span><span class="sxs-lookup"><span data-stu-id="756fa-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756fa-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="756fa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="756fa-133">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="756fa-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="756fa-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="756fa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="756fa-135">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="756fa-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="756fa-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="756fa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="756fa-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="756fa-138">IDL</span><span class="sxs-lookup"><span data-stu-id="756fa-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="756fa-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="756fa-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="756fa-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="756fa-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="756fa-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="756fa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="756fa-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756fa-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="756fa-144">IID</span><span class="sxs-lookup"><span data-stu-id="756fa-144">IID</span></span><br/>                      | <span data-ttu-id="756fa-145">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="756fa-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="756fa-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="756fa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756fa-147">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="756fa-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





