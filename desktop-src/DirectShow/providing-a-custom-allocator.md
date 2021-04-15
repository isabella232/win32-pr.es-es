---
description: Proporcionar un asignador personalizado
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Proporcionar un asignador personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422848"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="a7c14-103">Proporcionar un asignador personalizado</span><span class="sxs-lookup"><span data-stu-id="a7c14-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="a7c14-104">En esta sección se describe cómo proporcionar un asignador personalizado para un filtro.</span><span class="sxs-lookup"><span data-stu-id="a7c14-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="a7c14-105">Solo se describen las conexiones [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , pero los pasos para una conexión [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) son similares.</span><span class="sxs-lookup"><span data-stu-id="a7c14-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="a7c14-106">En primer lugar, defina una clase de C++ para el asignador.</span><span class="sxs-lookup"><span data-stu-id="a7c14-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="a7c14-107">Su asignador puede derivar de una de las clases de asignador estándar, [**CBaseAllocator**](cbaseallocator.md) o [**CMemAllocator**](cmemallocator.md), o puede crear una clase de asignador completamente nueva.</span><span class="sxs-lookup"><span data-stu-id="a7c14-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="a7c14-108">Si crea una nueva clase, debe exponer la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="a7c14-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="a7c14-109">Los pasos restantes dependen de si el asignador pertenece a un terminal de entrada o a un terminal de salida en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a7c14-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="a7c14-110">Los pin de entrada juegan un rol diferente que los pin de salida durante la fase de negociación del asignador, porque el PIN de salida selecciona en última instancia el asignador.</span><span class="sxs-lookup"><span data-stu-id="a7c14-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="a7c14-111">**Proporcionar un asignador personalizado para un PIN de entrada**</span><span class="sxs-lookup"><span data-stu-id="a7c14-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="a7c14-112">Para proporcionar un asignador para un PIN de entrada, invalide el método [**CBaseInputPin:: GetAllocator**](cbaseinputpin-getallocator.md) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7c14-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="a7c14-113">En este método, Compruebe la variable de miembro **m \_ pAllocator** .</span><span class="sxs-lookup"><span data-stu-id="a7c14-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="a7c14-114">Si esta variable no es **null**, significa que el asignador ya se ha seleccionado para esta conexión, por lo que el método **GetAllocator** debe devolver un puntero a ese asignador.</span><span class="sxs-lookup"><span data-stu-id="a7c14-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="a7c14-115">Si **m \_ PAllocator** es **null**, significa que no se ha seleccionado el asignador, por lo que el método **GetAllocator** debe devolver un puntero al asignador preferido del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7c14-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="a7c14-116">En ese caso, cree una instancia de su asignador personalizado y devuelva su puntero [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="a7c14-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="a7c14-117">En el código siguiente se muestra cómo implementar el método **GetAllocator** :</span><span class="sxs-lookup"><span data-stu-id="a7c14-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="a7c14-118">Cuando el filtro de nivel superior selecciona un asignador, llama al método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7c14-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="a7c14-119">Invalide el método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) para comprobar las propiedades de asignador.</span><span class="sxs-lookup"><span data-stu-id="a7c14-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="a7c14-120">En algunos casos, el PIN de entrada podría rechazar el asignador si no es el asignador personalizado, aunque esto puede hacer que se produzca un error en toda la conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="a7c14-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="a7c14-121">**Proporcionar un asignador personalizado para un PIN de salida**</span><span class="sxs-lookup"><span data-stu-id="a7c14-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="a7c14-122">Para proporcionar un asignador para un PIN de salida, invalide el método [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) para crear una instancia del asignador:</span><span class="sxs-lookup"><span data-stu-id="a7c14-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="a7c14-123">De forma predeterminada, la clase [**CBaseOutputPin**](cbaseoutputpin.md) solicita primero un asignador del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7c14-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="a7c14-124">Si ese asignador no es adecuado, el PIN de salida crea su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="a7c14-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="a7c14-125">Para forzar que la conexión use el asignador personalizado, invalide el método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c14-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="a7c14-126">Sin embargo, tenga en cuenta que esto puede impedir que la clavija de salida se conecte con determinados filtros, porque el otro filtro también puede requerir su propio asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7c14-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="a7c14-127">Una tercera opción es cambiar el orden: Pruebe el asignador personalizado primero y, a continuación, revierta al asignador del otro filtro.</span><span class="sxs-lookup"><span data-stu-id="a7c14-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7c14-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7c14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7c14-129">Negociar asignadores</span><span class="sxs-lookup"><span data-stu-id="a7c14-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 



