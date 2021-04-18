---
title: IDXCoreAdapter::SetState
description: Establece el estado del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720158"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="2c4d1-103">IDXCoreAdapter:: SetState (método)</span><span class="sxs-lookup"><span data-stu-id="2c4d1-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="2c4d1-104">Establece el estado del elemento especificado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="2c4d1-105">Antes de llamar a **SetState** para un tipo de propiedad, llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="2c4d1-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4d1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c4d1-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="2c4d1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c4d1-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="2c4d1-108">state</span><span class="sxs-lookup"><span data-stu-id="2c4d1-108">state</span></span>

<span data-ttu-id="2c4d1-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="2c4d1-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="2c4d1-110">El tipo de elemento de estado en el adaptador cuyo estado desea establecer.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="2c4d1-111">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="2c4d1-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="2c4d1-112">inputStateDetailsSize</span></span>

<span data-ttu-id="2c4d1-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="2c4d1-113">Type: **size_t**</span></span>

<span data-ttu-id="2c4d1-114">El tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna y proporciona de forma opcional en *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="2c4d1-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="2c4d1-115">inputStateDetails [in]</span></span>

<span data-ttu-id="2c4d1-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="2c4d1-116">Type: **void const\***</span></span>

<span data-ttu-id="2c4d1-117">Un puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene información sobre la solicitud que se requiere para la clase de estado que se especifica en el *Estado*.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="2c4d1-118">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="2c4d1-119">inputDataSize</span><span class="sxs-lookup"><span data-stu-id="2c4d1-119">inputDataSize</span></span>

<span data-ttu-id="2c4d1-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="2c4d1-120">Type: **size_t**</span></span>

<span data-ttu-id="2c4d1-121">El tamaño, en bytes, del búfer de entrada que asigna y proporciona en *inputData*.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="2c4d1-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="2c4d1-122">inputData [in]</span></span>

<span data-ttu-id="2c4d1-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="2c4d1-123">Type: **void\***</span></span>

<span data-ttu-id="2c4d1-124">Un puntero a un búfer de entrada que se asigna en la aplicación, que contiene la información de estado que se va a establecer para el elemento de Estado cuyo tipo se especifica en el *Estado*.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="2c4d1-125">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre el requisito de búfer de entrada para un tipo de estado determinado.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="2c4d1-126">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="2c4d1-126">Returns</span></span>

<span data-ttu-id="2c4d1-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2c4d1-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2c4d1-128">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2c4d1-129">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2c4d1-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2c4d1-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c4d1-130">Return value</span></span>|<span data-ttu-id="2c4d1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c4d1-131">Description</span></span>|
|-|-|
|<span data-ttu-id="2c4d1-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="2c4d1-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="2c4d1-133">El adaptador ya no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="2c4d1-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="2c4d1-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="2c4d1-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="2c4d1-135">Este sistema operativo (SO) no reconoce la clase de estado especificada en *Estado* .</span><span class="sxs-lookup"><span data-stu-id="2c4d1-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="2c4d1-136">Llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="2c4d1-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="2c4d1-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="2c4d1-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="2c4d1-138">El adaptador no admite la clase de estado especificada en el *Estado* .</span><span class="sxs-lookup"><span data-stu-id="2c4d1-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="2c4d1-139">Llame a [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que el establecimiento de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="2c4d1-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="2c4d1-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2c4d1-140">E_INVALIDARG</span></span>|<span data-ttu-id="2c4d1-141">Se proporciona un tamaño de búfer insuficiente para *inputData* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).</span><span class="sxs-lookup"><span data-stu-id="2c4d1-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="2c4d1-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2c4d1-142">E_POINTER</span></span>|<span data-ttu-id="2c4d1-143">`nullptr` se proporcionó para *inputData* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).</span><span class="sxs-lookup"><span data-stu-id="2c4d1-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="2c4d1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c4d1-144">See also</span></span>

<span data-ttu-id="2c4d1-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2c4d1-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>