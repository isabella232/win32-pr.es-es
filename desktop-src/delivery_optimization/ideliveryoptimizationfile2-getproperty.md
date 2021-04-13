---
title: 'IDeliveryOptimizationFile2:: GetProperty (método)'
description: 'Este método devuelve una única propiedad del archivo DO. | IDeliveryOptimizationFile2:: GetProperty (método)'
keywords:
- Método GetProperty
- Método GetProperty, interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362344"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="690db-107">IDeliveryOptimizationFile2:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="690db-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="690db-108">Este método devuelve una única propiedad del archivo DO.</span><span class="sxs-lookup"><span data-stu-id="690db-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="690db-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="690db-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="690db-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="690db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="690db-111">*propId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="690db-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="690db-112">El identificador de propiedad necesario para obtener de tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="690db-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="690db-113">*propValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="690db-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="690db-114">Valor de propiedad almacenado en una variante.</span><span class="sxs-lookup"><span data-stu-id="690db-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="690db-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="690db-115">Return value</span></span>

<span data-ttu-id="690db-116">Este método devuelve los siguientes valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="690db-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="690db-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="690db-117">Return code</span></span>                  | <span data-ttu-id="690db-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="690db-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="690db-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="690db-119">**S_OK**</span></span>                     | <span data-ttu-id="690db-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="690db-120">Success</span></span>                                             |
| <span data-ttu-id="690db-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="690db-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="690db-122">IDENTIFICADOR de propiedad desconocido.</span><span class="sxs-lookup"><span data-stu-id="690db-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="690db-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="690db-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="690db-124">La propiedad es de solo escritura y no se puede leer.</span><span class="sxs-lookup"><span data-stu-id="690db-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="690db-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="690db-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="690db-126">No se estableció ninguna propiedad mediante el método SetProperty.</span><span class="sxs-lookup"><span data-stu-id="690db-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="690db-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="690db-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="690db-128">Error de asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="690db-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="690db-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="690db-129">Requirements</span></span>

| <span data-ttu-id="690db-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="690db-130">Requirement</span></span> | <span data-ttu-id="690db-131">Value</span><span class="sxs-lookup"><span data-stu-id="690db-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="690db-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="690db-132">Minimum supported client</span></span>  | <span data-ttu-id="690db-133">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="690db-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="690db-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="690db-134">Minimum supported server</span></span>  | <span data-ttu-id="690db-135">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="690db-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="690db-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="690db-136">Header</span></span>                    | <span data-ttu-id="690db-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="690db-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="690db-138">IDL</span><span class="sxs-lookup"><span data-stu-id="690db-138">IDL</span></span>                       | <span data-ttu-id="690db-139">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="690db-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="690db-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="690db-140">Library</span></span>                   | <span data-ttu-id="690db-141">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="690db-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="690db-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="690db-142">DLL</span></span>                       | <span data-ttu-id="690db-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="690db-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="690db-144">IID</span><span class="sxs-lookup"><span data-stu-id="690db-144">IID</span></span>                       | <span data-ttu-id="690db-145">IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="690db-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="690db-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="690db-146">See also</span></span>

[<span data-ttu-id="690db-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="690db-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
