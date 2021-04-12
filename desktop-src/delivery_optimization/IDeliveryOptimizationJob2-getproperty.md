---
title: 'IDeliveryOptimizationJob2:: GetProperty (método)'
description: Devuelve una única propiedad del trabajo.
keywords:
- Método GetProperty
- Método GetProperty, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489826"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="4ecc0-106">IDeliveryOptimizationJob2:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="4ecc0-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="4ecc0-107">Este método devuelve una única propiedad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecc0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ecc0-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="4ecc0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ecc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecc0-110">*propId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ecc0-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc0-111">IDENTIFICADOR de propiedad necesario que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-111">The required property ID to get.</span></span> <span data-ttu-id="4ecc0-112">Solo se admite **DOJobPropertyId_ExtendedErrorInfo** de tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="4ecc0-113">*propValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ecc0-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc0-114">Valor de propiedad resultante, almacenado en un tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecc0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ecc0-115">Return value</span></span>

<span data-ttu-id="4ecc0-116">Este método devuelve los siguientes valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="4ecc0-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4ecc0-117">Return code</span></span>                  | <span data-ttu-id="4ecc0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ecc0-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="4ecc0-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="4ecc0-119">**S_OK**</span></span>                     | <span data-ttu-id="4ecc0-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="4ecc0-120">Success</span></span>              |
| <span data-ttu-id="4ecc0-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="4ecc0-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="4ecc0-122">IDENTIFICADOR de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="4ecc0-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="4ecc0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ecc0-123">Requirements</span></span>

| <span data-ttu-id="4ecc0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ecc0-124">Requirement</span></span> | <span data-ttu-id="4ecc0-125">Value</span><span class="sxs-lookup"><span data-stu-id="4ecc0-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4ecc0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ecc0-126">Minimum supported client</span></span>  | <span data-ttu-id="4ecc0-127">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ecc0-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="4ecc0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ecc0-128">Minimum supported server</span></span>  | <span data-ttu-id="4ecc0-129">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="4ecc0-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="4ecc0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ecc0-130">Header</span></span>                    | <span data-ttu-id="4ecc0-131">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="4ecc0-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="4ecc0-132">IDL</span><span class="sxs-lookup"><span data-stu-id="4ecc0-132">IDL</span></span>                       | <span data-ttu-id="4ecc0-133">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="4ecc0-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="4ecc0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ecc0-134">Library</span></span>                   | <span data-ttu-id="4ecc0-135">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="4ecc0-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="4ecc0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ecc0-136">DLL</span></span>                       | <span data-ttu-id="4ecc0-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="4ecc0-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="4ecc0-138">IID</span><span class="sxs-lookup"><span data-stu-id="4ecc0-138">IID</span></span>                       | <span data-ttu-id="4ecc0-139">IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="4ecc0-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="4ecc0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ecc0-140">See also</span></span>

[<span data-ttu-id="4ecc0-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="4ecc0-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
