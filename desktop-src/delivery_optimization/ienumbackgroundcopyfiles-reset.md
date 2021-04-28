---
title: Método de restablecimiento de IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: 'Método IEnumBackgroundCopyFiles::Reset: restablece la secuencia de enumeración al principio.'
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset (método)
- Método Reset, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6800095d0a6f20ef8b632830a224d4da27356bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105493"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="e70c7-106">IEnumBackgroundCopyFiles::Reset (Método)</span><span class="sxs-lookup"><span data-stu-id="e70c7-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="e70c7-107">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="e70c7-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e70c7-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="e70c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e70c7-109">Parameters</span></span>

<span data-ttu-id="e70c7-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e70c7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e70c7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e70c7-111">Return value</span></span>

<span data-ttu-id="e70c7-112">Este método devuelve **S_OK** correcto o uno de los valores **HRESULT COM** estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="e70c7-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70c7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70c7-113">Requirements</span></span>



| <span data-ttu-id="e70c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70c7-114">Requirement</span></span> | <span data-ttu-id="e70c7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e70c7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70c7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e70c7-117">Windows 10, versión 1709 solo para \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="e70c7-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e70c7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e70c7-119">Windows Server, solo aplicaciones de escritorio de la versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e70c7-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e70c7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e70c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e70c7-121"><dt>Deliveryoptimization.h</dt></span><span class="sxs-lookup"><span data-stu-id="e70c7-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e70c7-122">Idl</span><span class="sxs-lookup"><span data-stu-id="e70c7-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e70c7-123"><dt>DeliveryOptimization.idl</dt></span><span class="sxs-lookup"><span data-stu-id="e70c7-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e70c7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e70c7-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e70c7-125"><dt>Dosvc.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e70c7-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e70c7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e70c7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70c7-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e70c7-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e70c7-128">IID</span><span class="sxs-lookup"><span data-stu-id="e70c7-128">IID</span></span><br/>                      | <span data-ttu-id="e70c7-129">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="e70c7-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="e70c7-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e70c7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70c7-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="e70c7-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





