---
title: IDXCoreAdapter::GetProperty
description: Recupera el valor de la propiedad del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359349"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="d7703-103">IDXCoreAdapter:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="d7703-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="d7703-104">Recupera el valor de la propiedad del adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="d7703-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="d7703-105">Antes de llamar a **GetProperty** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="d7703-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="d7703-106">Además, antes de llamar a **GetProperty**, llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño necesario del búfer en el que se va a recibir el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d7703-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7703-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7703-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="d7703-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7703-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="d7703-109">propiedad</span><span class="sxs-lookup"><span data-stu-id="d7703-109">property</span></span>

<span data-ttu-id="d7703-110">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="d7703-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="d7703-111">Tipo de la propiedad cuyo valor se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="d7703-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="d7703-112">Vea la tabla en [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obtener más información sobre cada propiedad del adaptador.</span><span class="sxs-lookup"><span data-stu-id="d7703-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="d7703-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="d7703-113">bufferSize</span></span>

<span data-ttu-id="d7703-114">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="d7703-114">Type: **size_t**</span></span>

<span data-ttu-id="d7703-115">El tamaño, en bytes, del búfer de salida que asigna y proporciona en *propertyData*.</span><span class="sxs-lookup"><span data-stu-id="d7703-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="d7703-116">propertyData [out]</span><span class="sxs-lookup"><span data-stu-id="d7703-116">propertyData [out]</span></span>

<span data-ttu-id="d7703-117">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="d7703-117">Type: **void\***</span></span>

<span data-ttu-id="d7703-118">Un puntero a un búfer de salida que se asigna en la aplicación y que la función rellena.</span><span class="sxs-lookup"><span data-stu-id="d7703-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="d7703-119">Llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.</span><span class="sxs-lookup"><span data-stu-id="d7703-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="d7703-120">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="d7703-120">Returns</span></span>

<span data-ttu-id="d7703-121">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="d7703-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="d7703-122">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="d7703-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d7703-123">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d7703-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="d7703-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7703-124">Return value</span></span>|<span data-ttu-id="d7703-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7703-125">Description</span></span>|
|-|-|
|<span data-ttu-id="d7703-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="d7703-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="d7703-127">Este sistema operativo (SO) no reconoce el tipo de propiedad especificado en la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="d7703-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="d7703-128">Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="d7703-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="d7703-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d7703-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="d7703-130">El adaptador no admite el tipo de propiedad especificado en la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="d7703-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="d7703-131">Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="d7703-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="d7703-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d7703-132">E_INVALIDARG</span></span>|<span data-ttu-id="d7703-133">En *propertyData*, se proporciona un tamaño de búfer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="d7703-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="d7703-134">Llame a [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar el tamaño que debe tener el búfer *propertyData* para una propiedad de adaptador determinada.</span><span class="sxs-lookup"><span data-stu-id="d7703-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="d7703-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="d7703-135">E_POINTER</span></span>|<span data-ttu-id="d7703-136">`nullptr` se proporcionó para *propertyData*.</span><span class="sxs-lookup"><span data-stu-id="d7703-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d7703-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7703-137">Remarks</span></span>

<span data-ttu-id="d7703-138">Puede llamar a **GetProperty** en un adaptador que ya no sea válido &mdash; . la función no producirá un error como resultado de eso.</span><span class="sxs-lookup"><span data-stu-id="d7703-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="d7703-139">Esta función pone en cero el búfer de *propertyData* antes de rellenarlo.</span><span class="sxs-lookup"><span data-stu-id="d7703-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7703-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7703-140">See also</span></span>

<span data-ttu-id="d7703-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="d7703-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>