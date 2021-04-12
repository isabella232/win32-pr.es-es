---
title: IDXCoreAdapter::GetFactory
description: Recupera un puntero de interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador de adaptadores DXCore. | IDXCoreAdapter::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280078"
---
# <a name="idxcoreadaptergetfactory-method"></a><span data-ttu-id="be557-104">IDXCoreAdapter:: GetFactory (método)</span><span class="sxs-lookup"><span data-stu-id="be557-104">IDXCoreAdapter::GetFactory method</span></span>

<span data-ttu-id="be557-105">Recupera un puntero de interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) al objeto de generador de adaptadores DXCore.</span><span class="sxs-lookup"><span data-stu-id="be557-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="be557-106">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="be557-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be557-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be557-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="be557-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be557-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="be557-109">riid</span><span class="sxs-lookup"><span data-stu-id="be557-109">riid</span></span>

<span data-ttu-id="be557-110">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="be557-110">Type: **REFIID**</span></span>

<span data-ttu-id="be557-111">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="be557-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="be557-112">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="be557-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="be557-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="be557-113">ppvFactory [out]</span></span>

<span data-ttu-id="be557-114">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="be557-114">Type: **void\*\***</span></span>

<span data-ttu-id="be557-115">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="be557-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="be557-116">Si la devolución es correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al objeto de generador de adaptadores DXCore existente.</span><span class="sxs-lookup"><span data-stu-id="be557-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="be557-117">Antes de devolver, la función incrementa el recuento de referencias en la interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) del objeto de generador.</span><span class="sxs-lookup"><span data-stu-id="be557-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="be557-118">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="be557-118">Returns</span></span>

<span data-ttu-id="be557-119">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="be557-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="be557-120">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="be557-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="be557-121">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="be557-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="be557-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be557-122">Return value</span></span>|<span data-ttu-id="be557-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="be557-123">Description</span></span>|
|-|-|
|<span data-ttu-id="be557-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="be557-124">E_NOINTERFACE</span></span>|<span data-ttu-id="be557-125">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="be557-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="be557-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="be557-126">E_POINTER</span></span>|<span data-ttu-id="be557-127">`nullptr` se proporcionó para *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="be557-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="be557-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be557-128">Remarks</span></span>

<span data-ttu-id="be557-129">Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , una interfaz [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o una interfaz [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , las llamadas adicionales a [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory]() devolverán punteros al mismo objeto, lo que aumentará el recuento de referencias de la interfaz **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="be557-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory]() will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="be557-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="be557-130">See also</span></span>

<span data-ttu-id="be557-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="be557-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
