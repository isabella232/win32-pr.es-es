---
title: Método IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Recupera los intervalos que desea descargar del archivo remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Método GetFileRanges
- Método GetFileRanges, interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, método GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422240"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="81843-106">IBackgroundCopyFile2:: GetFileRanges (método)</span><span class="sxs-lookup"><span data-stu-id="81843-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="81843-107">Recupera los intervalos que desea descargar del archivo remoto.</span><span class="sxs-lookup"><span data-stu-id="81843-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81843-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81843-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="81843-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81843-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81843-110">*RangeCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81843-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81843-111">Número de elementos de *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="81843-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="81843-112">*Intervalos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="81843-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81843-113">Matriz de estructuras [**BG_FILE_RANGE**](bg-file-range.md) que especifican los intervalos que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="81843-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="81843-114">Cuando haya terminado, llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="81843-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81843-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81843-115">Return value</span></span>

<span data-ttu-id="81843-116">Este método devuelve los siguientes valores devueltos, así como otros.</span><span class="sxs-lookup"><span data-stu-id="81843-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="81843-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="81843-117">Return code</span></span>                                                                              | <span data-ttu-id="81843-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="81843-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81843-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="81843-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="81843-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="81843-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="81843-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="81843-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="81843-122">No se especificó ningún intervalo o el trabajo es un trabajo de carga o de carga-respuesta.</span><span class="sxs-lookup"><span data-stu-id="81843-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="81843-123">*RangeCount* se establece en cero y *Ranges* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="81843-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81843-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81843-124">Requirements</span></span>



| <span data-ttu-id="81843-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="81843-125">Requirement</span></span> | <span data-ttu-id="81843-126">Value</span><span class="sxs-lookup"><span data-stu-id="81843-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81843-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81843-127">Minimum supported client</span></span><br/> | <span data-ttu-id="81843-128">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="81843-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="81843-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81843-129">Minimum supported server</span></span><br/> | <span data-ttu-id="81843-130">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="81843-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="81843-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81843-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="81843-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="81843-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="81843-133">IDL</span><span class="sxs-lookup"><span data-stu-id="81843-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81843-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81843-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="81843-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81843-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="81843-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81843-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="81843-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81843-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81843-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81843-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="81843-139">IID</span><span class="sxs-lookup"><span data-stu-id="81843-139">IID</span></span><br/>                      | <span data-ttu-id="81843-140">IID_IBackgroundCopyFile2 se define como 83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="81843-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="81843-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="81843-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81843-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="81843-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="81843-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="81843-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

