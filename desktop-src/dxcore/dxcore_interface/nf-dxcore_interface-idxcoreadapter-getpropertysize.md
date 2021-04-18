---
title: IDXCoreAdapter::GetPropertySize
description: Para una propiedad de adaptador especificada, recupera el tamaño del búfer, en bytes, que es necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720148"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="f7086-103">IDXCoreAdapter:: GetPropertySize (método)</span><span class="sxs-lookup"><span data-stu-id="f7086-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="f7086-104">Para una propiedad de adaptador especificada, recupera el tamaño del búfer, en bytes, que es necesario para una llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f7086-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="f7086-105">Antes de llamar a **GetPropertySize** para un tipo de propiedad, llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="f7086-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7086-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7086-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="f7086-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7086-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="f7086-108">propiedad</span><span class="sxs-lookup"><span data-stu-id="f7086-108">property</span></span>

<span data-ttu-id="f7086-109">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="f7086-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="f7086-110">Tipo de la propiedad cuyo tamaño, en bytes, se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="f7086-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="f7086-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="f7086-111">bufferSize [out]</span></span>

<span data-ttu-id="f7086-112">Tipo: **size_t \***</span><span class="sxs-lookup"><span data-stu-id="f7086-112">Type: **size_t\***</span></span>

<span data-ttu-id="f7086-113">Puntero a un valor de **size_t** .</span><span class="sxs-lookup"><span data-stu-id="f7086-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="f7086-114">La función desreferencia el puntero y establece el valor en el tamaño, en bytes, del búfer de salida que se debe asignar y pasar como argumento *propertyData* en la llamada a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f7086-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="f7086-115">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="f7086-115">Returns</span></span>

<span data-ttu-id="f7086-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f7086-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f7086-117">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f7086-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f7086-118">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f7086-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f7086-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7086-119">Return value</span></span>|<span data-ttu-id="f7086-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7086-120">Description</span></span>|
|-|-|
|<span data-ttu-id="f7086-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="f7086-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="f7086-122">Este sistema operativo (SO) no reconoce el tipo de propiedad especificado en la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="f7086-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="f7086-123">Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="f7086-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f7086-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f7086-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="f7086-125">El adaptador no admite el tipo de propiedad especificado en la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="f7086-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="f7086-126">Llame a [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que el tipo de propiedad está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="f7086-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="f7086-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f7086-127">E_POINTER</span></span>|<span data-ttu-id="f7086-128">`nullptr` se proporcionó para *buffersize*.</span><span class="sxs-lookup"><span data-stu-id="f7086-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f7086-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7086-129">Remarks</span></span>

<span data-ttu-id="f7086-130">Puede llamar a **GetPropertySize** en un adaptador que ya no sea válido &mdash; . la función no producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f7086-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7086-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7086-131">See also</span></span>

<span data-ttu-id="f7086-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f7086-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>