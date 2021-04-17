---
title: 'IDeliveryOptimizationFile2:: SetProperty (método)'
description: 'Este método devuelve una única propiedad del archivo DO. | IDeliveryOptimizationFile2:: SetProperty (método)'
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717491"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="62dac-107">IDeliveryOptimizationFile2:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="62dac-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="62dac-108">Este método devuelve una única propiedad del archivo DO.</span><span class="sxs-lookup"><span data-stu-id="62dac-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62dac-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="62dac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62dac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dac-111">*propId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62dac-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dac-112">El identificador de propiedad necesario para establecer de tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="62dac-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="62dac-113">*propValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62dac-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dac-114">Valor de propiedad que se va a establecer, de tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="62dac-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62dac-115">Return value</span></span>

<span data-ttu-id="62dac-116">Este método devuelve los siguientes valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="62dac-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="62dac-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="62dac-117">Return code</span></span>                  | <span data-ttu-id="62dac-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="62dac-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="62dac-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="62dac-119">**S_OK**</span></span>                     | <span data-ttu-id="62dac-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="62dac-120">Success</span></span>                                                            |
| <span data-ttu-id="62dac-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="62dac-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="62dac-122">IDENTIFICADOR de propiedad desconocido</span><span class="sxs-lookup"><span data-stu-id="62dac-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="62dac-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="62dac-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="62dac-124">El trabajo no está actualmente en un estado que permita una configuración de propiedad</span><span class="sxs-lookup"><span data-stu-id="62dac-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="62dac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62dac-125">Requirements</span></span>

| <span data-ttu-id="62dac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="62dac-126">Requirement</span></span> | <span data-ttu-id="62dac-127">Value</span><span class="sxs-lookup"><span data-stu-id="62dac-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62dac-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62dac-128">Minimum supported client</span></span>  | <span data-ttu-id="62dac-129">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="62dac-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="62dac-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62dac-130">Minimum supported server</span></span>  | <span data-ttu-id="62dac-131">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="62dac-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="62dac-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62dac-132">Header</span></span>                    | <span data-ttu-id="62dac-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="62dac-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="62dac-134">IDL</span><span class="sxs-lookup"><span data-stu-id="62dac-134">IDL</span></span>                       | <span data-ttu-id="62dac-135">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="62dac-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="62dac-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62dac-136">Library</span></span>                   | <span data-ttu-id="62dac-137">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="62dac-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="62dac-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62dac-138">DLL</span></span>                       | <span data-ttu-id="62dac-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="62dac-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="62dac-140">IID</span><span class="sxs-lookup"><span data-stu-id="62dac-140">IID</span></span>                       | <span data-ttu-id="62dac-141">IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="62dac-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="62dac-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="62dac-142">See also</span></span>

[<span data-ttu-id="62dac-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="62dac-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
