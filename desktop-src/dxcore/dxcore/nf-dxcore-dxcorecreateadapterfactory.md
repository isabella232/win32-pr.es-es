---
title: DXCoreCreateAdapterFactory
description: Crea un generador de adaptadores de DXCore, que puede usar para generar más objetos DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995508"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="dd471-103">DXCoreCreateAdapterFactory función)</span><span class="sxs-lookup"><span data-stu-id="dd471-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="dd471-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd471-104">Description</span></span>

<span data-ttu-id="dd471-105">Crea un generador de adaptadores de DXCore, que puede usar para generar más objetos DXCore.</span><span class="sxs-lookup"><span data-stu-id="dd471-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="dd471-106">Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="dd471-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="dd471-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd471-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="dd471-108">riid</span><span class="sxs-lookup"><span data-stu-id="dd471-108">riid</span></span>

<span data-ttu-id="dd471-109">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="dd471-109">Type: **REFIID**</span></span>

<span data-ttu-id="dd471-110">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="dd471-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="dd471-111">Se espera que sea el identificador de interfaz (IID) de [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="dd471-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="dd471-112">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="dd471-112">ppvFactory [out]</span></span>

<span data-ttu-id="dd471-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="dd471-113">Type: **void\*\***</span></span>

<span data-ttu-id="dd471-114">Dirección de un puntero a una interfaz con el IID especificado en el parámetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="dd471-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="dd471-115">Cuando la devolución es correcta, *\* ppvFactory* (la dirección desreferenciada) contiene un puntero al generador de DXCore creado.</span><span class="sxs-lookup"><span data-stu-id="dd471-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="dd471-116">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="dd471-116">Returns</span></span>

<span data-ttu-id="dd471-117">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="dd471-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="dd471-118">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="dd471-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="dd471-119">De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dd471-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="dd471-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd471-120">Return value</span></span>|<span data-ttu-id="dd471-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd471-121">Description</span></span>|
|-|-|
|<span data-ttu-id="dd471-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="dd471-122">E_NOINTERFACE</span></span>|<span data-ttu-id="dd471-123">Se proporcionó un valor no válido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="dd471-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="dd471-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="dd471-124">E_POINTER</span></span>|<span data-ttu-id="dd471-125">`nullptr` se proporcionó para *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="dd471-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dd471-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd471-126">Remarks</span></span>

<span data-ttu-id="dd471-127">Durante el tiempo que existe una referencia en una interfaz [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , una interfaz [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o una interfaz [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , las llamadas adicionales a **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) devolverán punteros al mismo objeto, lo que aumentará el recuento de referencias de la interfaz **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="dd471-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd471-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd471-128">See also</span></span>

<span data-ttu-id="dd471-129">[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="dd471-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>