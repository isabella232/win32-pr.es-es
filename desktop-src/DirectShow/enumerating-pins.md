---
description: Enumerar PIN
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumerar PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906585"
---
# <a name="enumerating-pins"></a><span data-ttu-id="68b83-103">Enumerar PIN</span><span class="sxs-lookup"><span data-stu-id="68b83-103">Enumerating Pins</span></span>

<span data-ttu-id="68b83-104">Los filtros admiten el método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , que enumera los pin disponibles en el filtro.</span><span class="sxs-lookup"><span data-stu-id="68b83-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="68b83-105">Devuelve un puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="68b83-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="68b83-106">El método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera punteros de interfaz de [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="68b83-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="68b83-107">En el ejemplo siguiente se muestra una función que busca un pin con una dirección determinada (entrada o salida) en un filtro determinado.</span><span class="sxs-lookup"><span data-stu-id="68b83-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="68b83-108">Usa la enumeración [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar la dirección del PIN y el método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para encontrar la dirección de cada pin enumerado.</span><span class="sxs-lookup"><span data-stu-id="68b83-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="68b83-109">Si esta función encuentra un PIN coincidente, devuelve un puntero de la interfaz **IPin** con un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="68b83-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="68b83-110">El autor de la llamada es responsable de liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="68b83-110">The caller is responsible for releasing the interface.</span></span>


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



<span data-ttu-id="68b83-111">Esta función se puede modificar fácilmente para devolver el PIN n con la dirección especificada o el PIN *n* no conectado.</span><span class="sxs-lookup"><span data-stu-id="68b83-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="68b83-112">(Para averiguar si un PIN está conectado a otro PIN, llame al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) ).</span><span class="sxs-lookup"><span data-stu-id="68b83-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="68b83-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68b83-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b83-114">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="68b83-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="68b83-115">Buscar un PIN no conectado en un filtro</span><span class="sxs-lookup"><span data-stu-id="68b83-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="68b83-116">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="68b83-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="68b83-117">Conjunto de propiedades de PIN</span><span class="sxs-lookup"><span data-stu-id="68b83-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



