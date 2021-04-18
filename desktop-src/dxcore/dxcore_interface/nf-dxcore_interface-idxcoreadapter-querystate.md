---
title: IDXCoreAdapter::QueryState
description: Recupera el estado actual del elemento especificado en el adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720159"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="84e85-103">IDXCoreAdapter:: QueryState (método)</span><span class="sxs-lookup"><span data-stu-id="84e85-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="84e85-104">Recupera el estado actual del elemento especificado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="84e85-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="84e85-105">Antes de llamar a **QueryState** para un tipo de propiedad, llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="84e85-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="84e85-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84e85-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="84e85-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84e85-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="84e85-108">state</span><span class="sxs-lookup"><span data-stu-id="84e85-108">state</span></span>

<span data-ttu-id="84e85-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="84e85-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="84e85-110">El tipo de elemento de estado en el adaptador cuyo estado desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="84e85-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="84e85-111">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.</span><span class="sxs-lookup"><span data-stu-id="84e85-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="84e85-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="84e85-112">inputStateDetailsSize</span></span>

<span data-ttu-id="84e85-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="84e85-113">Type: **size_t**</span></span>

<span data-ttu-id="84e85-114">El tamaño, en bytes, del búfer de detalles de estado de entrada que se asigna y proporciona de forma opcional en *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="84e85-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="84e85-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="84e85-115">inputStateDetails [in]</span></span>

<span data-ttu-id="84e85-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="84e85-116">Type: **void const\***</span></span>

<span data-ttu-id="84e85-117">Un puntero opcional a un búfer de detalles de estado de entrada constante que se asigna en la aplicación, que contiene información sobre la solicitud que se requiere para la clase de estado que se especifica en el *Estado*.</span><span class="sxs-lookup"><span data-stu-id="84e85-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="84e85-118">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cualquier requisito de búfer de entrada para un tipo de estado determinado.</span><span class="sxs-lookup"><span data-stu-id="84e85-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="84e85-119">outputBufferSize</span><span class="sxs-lookup"><span data-stu-id="84e85-119">outputBufferSize</span></span>

<span data-ttu-id="84e85-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="84e85-120">Type: **size_t**</span></span>

<span data-ttu-id="84e85-121">El tamaño, en bytes, del búfer de salida que asigna y proporciona en *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="84e85-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="84e85-122">outputBuffer [out]</span><span class="sxs-lookup"><span data-stu-id="84e85-122">outputBuffer [out]</span></span>

<span data-ttu-id="84e85-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="84e85-123">Type: **void\***</span></span>

<span data-ttu-id="84e85-124">Un puntero a un búfer de salida que se asigna en la aplicación y que la función rellena.</span><span class="sxs-lookup"><span data-stu-id="84e85-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="84e85-125">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre el requisito de búfer de salida para un tipo de estado determinado.</span><span class="sxs-lookup"><span data-stu-id="84e85-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="84e85-126">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="84e85-126">Returns</span></span>

<span data-ttu-id="84e85-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="84e85-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="84e85-128">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="84e85-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="84e85-129">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="84e85-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="84e85-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84e85-130">Return value</span></span>|<span data-ttu-id="84e85-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="84e85-131">Description</span></span>|
|-|-|
|<span data-ttu-id="84e85-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="84e85-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="84e85-133">El adaptador ya no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="84e85-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="84e85-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="84e85-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="84e85-135">Este sistema operativo (SO) no reconoce la clase de estado especificada en *Estado* .</span><span class="sxs-lookup"><span data-stu-id="84e85-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="84e85-136">Llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="84e85-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="84e85-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="84e85-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="84e85-138">El adaptador no admite la clase de estado especificada en el *Estado* .</span><span class="sxs-lookup"><span data-stu-id="84e85-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="84e85-139">Llame a [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que la consulta de la clase de estado está disponible para este adaptador y sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="84e85-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="84e85-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="84e85-140">E_INVALIDARG</span></span>|<span data-ttu-id="84e85-141">Se proporciona un tamaño de búfer insuficiente para *outputBuffer* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).</span><span class="sxs-lookup"><span data-stu-id="84e85-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="84e85-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="84e85-142">E_POINTER</span></span>|<span data-ttu-id="84e85-143">`nullptr` se proporcionó para *outputBuffer* (o para *inputStateDetails* cuando se necesita un búfer de detalles de estado de entrada).</span><span class="sxs-lookup"><span data-stu-id="84e85-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="84e85-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84e85-144">Remarks</span></span>

<span data-ttu-id="84e85-145">Consulte [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador y qué entradas y salidas se usan.</span><span class="sxs-lookup"><span data-stu-id="84e85-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="84e85-146">Esta función pone en cero el búfer de *outputBuffer* antes de rellenarlo.</span><span class="sxs-lookup"><span data-stu-id="84e85-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="84e85-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="84e85-147">See also</span></span>

<span data-ttu-id="84e85-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="84e85-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>