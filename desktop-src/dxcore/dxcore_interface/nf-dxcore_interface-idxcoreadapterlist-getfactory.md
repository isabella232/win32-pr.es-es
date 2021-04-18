---
title: IDXCoreAdapterList::GetFactory
description: Recupera un puntero de interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador de adaptadores DXCore. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105721407"
---
# <a name="idxcoreadapterlistgetfactory-method"></a><span data-ttu-id="57cfa-104">IDXCoreAdapterList:: GetFactory (método)</span><span class="sxs-lookup"><span data-stu-id="57cfa-104">IDXCoreAdapterList::GetFactory method</span></span>

<span data-ttu-id="57cfa-105">Recupera un puntero de interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador de adaptadores DXCore.</span><span class="sxs-lookup"><span data-stu-id="57cfa-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="57cfa-106">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="57cfa-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="57cfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57cfa-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="57cfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57cfa-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="57cfa-109">riid</span><span class="sxs-lookup"><span data-stu-id="57cfa-109">riid</span></span>

<span data-ttu-id="57cfa-110">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="57cfa-110">Type: **REFIID**</span></span>

<span data-ttu-id="57cfa-111">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="57cfa-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="57cfa-112">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="57cfa-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="57cfa-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="57cfa-113">ppvFactory [out]</span></span>

<span data-ttu-id="57cfa-114">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="57cfa-114">Type: **void\*\***</span></span>

<span data-ttu-id="57cfa-115">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="57cfa-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="57cfa-116">Si la devolución es correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al objeto de generador de adaptadores DXCore existente.</span><span class="sxs-lookup"><span data-stu-id="57cfa-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="57cfa-117">Antes de devolver, la función incrementa el recuento de referencias en la interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) del objeto de generador.</span><span class="sxs-lookup"><span data-stu-id="57cfa-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="57cfa-118">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="57cfa-118">Returns</span></span>

<span data-ttu-id="57cfa-119">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="57cfa-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="57cfa-120">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="57cfa-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="57cfa-121">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="57cfa-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="57cfa-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57cfa-122">Return value</span></span>|<span data-ttu-id="57cfa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="57cfa-123">Description</span></span>|
|-|-|
|<span data-ttu-id="57cfa-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="57cfa-124">E_NOINTERFACE</span></span>|<span data-ttu-id="57cfa-125">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="57cfa-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="57cfa-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="57cfa-126">E_POINTER</span></span>|<span data-ttu-id="57cfa-127">`nullptr` se proporcionó para *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="57cfa-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="57cfa-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57cfa-128">Remarks</span></span>

<span data-ttu-id="57cfa-129">Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , una interfaz [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o una interfaz [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , las llamadas adicionales a [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory]()o [IDXCoreAdapter:: GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) devolverán punteros al mismo objeto, lo que aumentará el recuento de referencias de la interfaz **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="57cfa-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](), or [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="57cfa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="57cfa-130">See also</span></span>

<span data-ttu-id="57cfa-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="57cfa-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
