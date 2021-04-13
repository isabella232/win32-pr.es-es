---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera el objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para un LUID especificado, si está disponible.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421139"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="ad123-103">IDXCoreAdapterFactory:: GetAdapterByLuid (método)</span><span class="sxs-lookup"><span data-stu-id="ad123-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="ad123-104">Recupera el objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para un LUID especificado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="ad123-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="ad123-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="ad123-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad123-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad123-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="ad123-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad123-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="ad123-108">adapterLUID</span><span class="sxs-lookup"><span data-stu-id="ad123-108">adapterLUID</span></span>

<span data-ttu-id="ad123-109">Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="ad123-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="ad123-110">Valor único local que identifica la instancia del adaptador.</span><span class="sxs-lookup"><span data-stu-id="ad123-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="ad123-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="ad123-111">riid [in]</span></span>

<span data-ttu-id="ad123-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="ad123-112">Type: **REFIID**</span></span>

<span data-ttu-id="ad123-113">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="ad123-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="ad123-114">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="ad123-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="ad123-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="ad123-115">ppvAdapter [out]</span></span>

<span data-ttu-id="ad123-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="ad123-116">Type: **void\*\***</span></span>

<span data-ttu-id="ad123-117">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="ad123-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="ad123-118">Si la devolución es correcta, *\* ppvAdapter* (la dirección desreferenciada) contiene un puntero al adaptador DXCore creado.</span><span class="sxs-lookup"><span data-stu-id="ad123-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="ad123-119">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="ad123-119">Returns</span></span>

<span data-ttu-id="ad123-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="ad123-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="ad123-121">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ad123-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="ad123-122">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ad123-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="ad123-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad123-123">Return value</span></span>|<span data-ttu-id="ad123-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad123-124">Description</span></span>|
|-|-|
|<span data-ttu-id="ad123-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="ad123-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="ad123-126">Se reconoce el LUID de adaptador pasado en *adapterLUID* , pero el adaptador ya no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="ad123-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="ad123-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ad123-127">E_INVALIDARG</span></span>|<span data-ttu-id="ad123-128">No se dispone de este LUID de adaptador como el valor pasado en *adapterLUID* a través de DXCore.</span><span class="sxs-lookup"><span data-stu-id="ad123-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="ad123-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="ad123-129">E_NOINTERFACE</span></span>|<span data-ttu-id="ad123-130">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="ad123-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="ad123-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="ad123-131">E_POINTER</span></span>|<span data-ttu-id="ad123-132">`nullptr` se proporcionó para *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="ad123-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ad123-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad123-133">Remarks</span></span>

<span data-ttu-id="ad123-134">Varias llamadas que pasan el mismo [LUID](/windows/win32/api/winnt/ns-winnt-luid) devuelven punteros de interfaz idénticos.</span><span class="sxs-lookup"><span data-stu-id="ad123-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="ad123-135">Como resultado, es seguro comparar los punteros de interfaz para determinar si varios punteros hacen referencia al mismo objeto de adaptador.</span><span class="sxs-lookup"><span data-stu-id="ad123-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad123-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad123-136">See also</span></span>

<span data-ttu-id="ad123-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ad123-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>