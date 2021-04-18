---
title: 'IDeliveryOptimizationJob2:: SetProperty (método)'
description: Este método no se utiliza.
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422372"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="e133b-106">IDeliveryOptimizationJob2:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="e133b-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="e133b-107">Este método no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e133b-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="e133b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e133b-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="e133b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e133b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e133b-110">*propId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e133b-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e133b-111">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e133b-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e133b-112">*propValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e133b-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e133b-113">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e133b-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e133b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e133b-114">Return value</span></span>

<span data-ttu-id="e133b-115">Si propId es **DOJobPropertyId_ExtendedErrorInfo**, el valor devuelto es **DO_E_READ_ONLY_PROPERTY**; en caso contrario, la función devuelve **DO_E_UNKNOWN_PROPERTY_ID**.</span><span class="sxs-lookup"><span data-stu-id="e133b-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e133b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e133b-116">Requirements</span></span>

| <span data-ttu-id="e133b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e133b-117">Requirement</span></span> | <span data-ttu-id="e133b-118">Value</span><span class="sxs-lookup"><span data-stu-id="e133b-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e133b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e133b-119">Minimum supported client</span></span>  | <span data-ttu-id="e133b-120">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="e133b-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="e133b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e133b-121">Minimum supported server</span></span>  | <span data-ttu-id="e133b-122">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="e133b-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="e133b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e133b-123">Header</span></span>                    | <span data-ttu-id="e133b-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="e133b-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="e133b-125">IDL</span><span class="sxs-lookup"><span data-stu-id="e133b-125">IDL</span></span>                       | <span data-ttu-id="e133b-126">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="e133b-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="e133b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e133b-127">Library</span></span>                   | <span data-ttu-id="e133b-128">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="e133b-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="e133b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e133b-129">DLL</span></span>                       | <span data-ttu-id="e133b-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="e133b-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="e133b-131">IID</span><span class="sxs-lookup"><span data-stu-id="e133b-131">IID</span></span>                       | <span data-ttu-id="e133b-132">IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="e133b-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="e133b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e133b-133">See also</span></span>

[<span data-ttu-id="e133b-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="e133b-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
