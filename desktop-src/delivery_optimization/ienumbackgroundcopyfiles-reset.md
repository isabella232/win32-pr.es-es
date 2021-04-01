---
title: Método de restablecimiento de IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Restablece la secuencia de enumeración al principio.
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
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905150"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="15922-106">IEnumBackgroundCopyFiles:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="15922-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="15922-107">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="15922-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="15922-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15922-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="15922-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15922-109">Parameters</span></span>

<span data-ttu-id="15922-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="15922-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15922-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15922-111">Return value</span></span>

<span data-ttu-id="15922-112">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="15922-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="15922-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15922-113">Requirements</span></span>



| <span data-ttu-id="15922-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15922-114">Requirement</span></span> | <span data-ttu-id="15922-115">Value</span><span class="sxs-lookup"><span data-stu-id="15922-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15922-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15922-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15922-117">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="15922-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="15922-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15922-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15922-119">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="15922-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="15922-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15922-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15922-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="15922-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="15922-122">IDL</span><span class="sxs-lookup"><span data-stu-id="15922-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15922-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15922-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="15922-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15922-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="15922-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15922-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="15922-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15922-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15922-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15922-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="15922-128">IID</span><span class="sxs-lookup"><span data-stu-id="15922-128">IID</span></span><br/>                      | <span data-ttu-id="15922-129">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="15922-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="15922-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="15922-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15922-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="15922-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





