---
description: En este tema se describe cómo buscar un PIN no conectado en un filtro. La búsqueda de un PIN no conectado resulta útil cuando se conectan filtros.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Buscar un PIN no conectado en un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079881"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="52f30-104">Buscar un PIN no conectado en un filtro</span><span class="sxs-lookup"><span data-stu-id="52f30-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="52f30-105">En este tema se describe cómo buscar un PIN no conectado en un filtro.</span><span class="sxs-lookup"><span data-stu-id="52f30-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="52f30-106">La búsqueda de un PIN no conectado resulta útil cuando se conectan filtros.</span><span class="sxs-lookup"><span data-stu-id="52f30-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="52f30-107">En un escenario típico de creación de gráficos de DirectShow, se necesita un PIN no conectado que coincida con una dirección de PIN determinada (entrada o salida).</span><span class="sxs-lookup"><span data-stu-id="52f30-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="52f30-108">Por ejemplo, cuando se conectan dos filtros, se conecta un PIN de salida de un filtro a un punto de entrada del otro filtro.</span><span class="sxs-lookup"><span data-stu-id="52f30-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="52f30-109">Ambos PIN deben estar sin conexión antes de conectarlos.</span><span class="sxs-lookup"><span data-stu-id="52f30-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="52f30-110">En primer lugar, se necesita una función que prueba si un PIN está conectado a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="52f30-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="52f30-111">Esta función llama al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para probar si el PIN está conectado a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="52f30-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="52f30-112">En este ejemplo se usa la función [SafeRelease](/windows/desktop/medfound/saferelease) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="52f30-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="52f30-113">A continuación, se necesita una función que prueba si un PIN coincide con una dirección de PIN especificada.</span><span class="sxs-lookup"><span data-stu-id="52f30-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="52f30-114">Esta función llama al método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obtener la dirección del PIN.</span><span class="sxs-lookup"><span data-stu-id="52f30-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



<span data-ttu-id="52f30-115">La función siguiente coincide con un PIN según los criterios (dirección del PIN y estado de la conexión).</span><span class="sxs-lookup"><span data-stu-id="52f30-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



<span data-ttu-id="52f30-116">Por último, la función siguiente usa la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="52f30-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="52f30-117">El autor de la llamada especifica la dirección de PIN deseada.</span><span class="sxs-lookup"><span data-stu-id="52f30-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="52f30-118">Para cada pin, la función llama `MatchPin` a para comprobar si el PIN es una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="52f30-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="52f30-119">Si la dirección coincide y el PIN está desconectado, la función devuelve un puntero al pin correspondiente en el parámetro *ppPin* .</span><span class="sxs-lookup"><span data-stu-id="52f30-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



<span data-ttu-id="52f30-120">Para obtener un ejemplo de cómo se puede usar esta función, consulte [Connect Two filters](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="52f30-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f30-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52f30-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f30-122">Enumerar PIN</span><span class="sxs-lookup"><span data-stu-id="52f30-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="52f30-123">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="52f30-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="52f30-124">**ICaptureGraphBuilder2::FindPin**</span><span class="sxs-lookup"><span data-stu-id="52f30-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
