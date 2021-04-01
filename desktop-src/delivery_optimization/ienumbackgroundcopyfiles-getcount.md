---
title: Método GetCount IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un recuento del número de archivos de la enumeración.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (método)
- Método GetCount, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802252"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="d94e0-106">IEnumBackgroundCopyFiles:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="d94e0-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="d94e0-107">Recupera un recuento del número de archivos de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d94e0-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94e0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d94e0-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d94e0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d94e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94e0-110">*pCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d94e0-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d94e0-111">Número de archivos de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d94e0-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94e0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d94e0-112">Return value</span></span>

<span data-ttu-id="d94e0-113">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="d94e0-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d94e0-114">Requirements</span></span>



| <span data-ttu-id="d94e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94e0-115">Requirement</span></span> | <span data-ttu-id="d94e0-116">Value</span><span class="sxs-lookup"><span data-stu-id="d94e0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d94e0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d94e0-118">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d94e0-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d94e0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d94e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d94e0-120">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d94e0-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d94e0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d94e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d94e0-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d94e0-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d94e0-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d94e0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d94e0-124"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d94e0-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d94e0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d94e0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d94e0-126"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d94e0-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d94e0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d94e0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d94e0-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d94e0-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d94e0-129">IID</span><span class="sxs-lookup"><span data-stu-id="d94e0-129">IID</span></span><br/>                      | <span data-ttu-id="d94e0-130">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="d94e0-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d94e0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d94e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94e0-132">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="d94e0-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





