---
title: Método IBackgroundCopyJob Enumfiles ((Deliveryoptimization. h)
description: Recupera un puntero de la interfaz IEnumBackgroundCopyFiles que se usa para enumerar los archivos de un trabajo.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método Enumfiles (
- Método Enumfiles (, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Enumfiles (
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150417"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="83aee-106">IBackgroundCopyJob:: Enumfiles ((método)</span><span class="sxs-lookup"><span data-stu-id="83aee-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="83aee-107">Recupera un puntero de la interfaz [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="83aee-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="83aee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83aee-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="83aee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83aee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83aee-110">*ppEnumFiles* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="83aee-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83aee-111">Puntero de interfaz [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="83aee-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="83aee-112">Suelte *ppEnumFiles* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="83aee-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83aee-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83aee-113">Return value</span></span>

<span data-ttu-id="83aee-114">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="83aee-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="83aee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83aee-115">Requirements</span></span>



| <span data-ttu-id="83aee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83aee-116">Requirement</span></span> | <span data-ttu-id="83aee-117">Value</span><span class="sxs-lookup"><span data-stu-id="83aee-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83aee-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83aee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83aee-119">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="83aee-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83aee-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83aee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83aee-121">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="83aee-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="83aee-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83aee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83aee-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="83aee-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="83aee-124">IDL</span><span class="sxs-lookup"><span data-stu-id="83aee-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83aee-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83aee-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="83aee-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83aee-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="83aee-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83aee-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="83aee-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83aee-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83aee-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83aee-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="83aee-130">IID</span><span class="sxs-lookup"><span data-stu-id="83aee-130">IID</span></span><br/>                      | <span data-ttu-id="83aee-131">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="83aee-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="83aee-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="83aee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83aee-133">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="83aee-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="83aee-134">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="83aee-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





