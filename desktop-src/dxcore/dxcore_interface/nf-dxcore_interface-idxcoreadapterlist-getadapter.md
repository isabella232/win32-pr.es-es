---
title: IDXCoreAdapterList::GetAdapter
description: Recupera un adaptador específico por índice de un objeto de lista de adaptadores de DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078179"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="acf2a-103">IDXCoreAdapterList:: GetAdapter (método)</span><span class="sxs-lookup"><span data-stu-id="acf2a-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="acf2a-104">Recupera un adaptador específico por índice de un objeto de lista de adaptadores de DXCore.</span><span class="sxs-lookup"><span data-stu-id="acf2a-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="acf2a-105">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="acf2a-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="acf2a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acf2a-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="acf2a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acf2a-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="acf2a-108">índice</span><span class="sxs-lookup"><span data-stu-id="acf2a-108">index</span></span>

<span data-ttu-id="acf2a-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="acf2a-109">Type: **uint32_t**</span></span>

<span data-ttu-id="acf2a-110">Índice de base cero que identifica una instancia de adaptador dentro de la lista de adaptadores de DXCore.</span><span class="sxs-lookup"><span data-stu-id="acf2a-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="acf2a-111">riid</span><span class="sxs-lookup"><span data-stu-id="acf2a-111">riid</span></span>

<span data-ttu-id="acf2a-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="acf2a-112">Type: **REFIID**</span></span>

<span data-ttu-id="acf2a-113">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="acf2a-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="acf2a-114">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="acf2a-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="acf2a-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="acf2a-115">ppvAdapter [out]</span></span>

<span data-ttu-id="acf2a-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="acf2a-116">Type: **void\*\***</span></span>

<span data-ttu-id="acf2a-117">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="acf2a-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="acf2a-118">Si la devolución es correcta, *\* ppvAdapter* (la dirección desreferenciada) contiene un puntero al adaptador DXCore creado.</span><span class="sxs-lookup"><span data-stu-id="acf2a-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="acf2a-119">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="acf2a-119">Returns</span></span>

<span data-ttu-id="acf2a-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="acf2a-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="acf2a-121">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="acf2a-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="acf2a-122">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="acf2a-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="acf2a-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acf2a-123">Return value</span></span>|<span data-ttu-id="acf2a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="acf2a-124">Description</span></span>|
|-|-|
|<span data-ttu-id="acf2a-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="acf2a-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="acf2a-126">El *Índice* es válido, pero el adaptador ya no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="acf2a-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="acf2a-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="acf2a-127">E_INVALIDARG</span></span>|<span data-ttu-id="acf2a-128">El *Índice* proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="acf2a-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="acf2a-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="acf2a-129">E_NOINTERFACE</span></span>|<span data-ttu-id="acf2a-130">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="acf2a-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="acf2a-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="acf2a-131">E_POINTER</span></span>|<span data-ttu-id="acf2a-132">`nullptr` se proporcionó para *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="acf2a-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="acf2a-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acf2a-133">Remarks</span></span>

<span data-ttu-id="acf2a-134">Varias llamadas que pasan un índice que representa al mismo adaptador devuelven punteros de interfaz idénticos, incluso en distintas listas de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="acf2a-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="acf2a-135">Como resultado, es seguro comparar los punteros de interfaz para determinar si varios punteros hacen referencia al mismo objeto de adaptador.</span><span class="sxs-lookup"><span data-stu-id="acf2a-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="acf2a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="acf2a-136">See also</span></span>

<span data-ttu-id="acf2a-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="acf2a-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>