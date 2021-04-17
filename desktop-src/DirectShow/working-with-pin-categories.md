---
description: Trabajar con categorías de PIN
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Trabajar con categorías de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666761"
---
# <a name="working-with-pin-categories"></a><span data-ttu-id="12c38-103">Trabajar con categorías de PIN</span><span class="sxs-lookup"><span data-stu-id="12c38-103">Working with Pin Categories</span></span>

<span data-ttu-id="12c38-104">Para buscar en un filtro el para un pin con una categoría de PIN determinada, puede usar el método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) .</span><span class="sxs-lookup"><span data-stu-id="12c38-104">To search on a filter the the for a pin with a given pin category, you can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method.</span></span> <span data-ttu-id="12c38-105">En el siguiente ejemplo se busca un PIN de vista previa de vídeo:</span><span class="sxs-lookup"><span data-stu-id="12c38-105">The following example searches for a video preview pin:</span></span>


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="12c38-106">El primer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.</span><span class="sxs-lookup"><span data-stu-id="12c38-106">The first parameter is a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="12c38-107">Los tres parámetros siguientes especifican la dirección, la categoría del PIN y el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="12c38-107">The next three parameters specify the direction, pin category, and media type.</span></span> <span data-ttu-id="12c38-108">El valor **false** en el quinto parámetro indica que el pin puede estar conectado o no conectado.</span><span class="sxs-lookup"><span data-stu-id="12c38-108">The value **FALSE** in the fifth parameter indicates that the pin can be either connected or unconnected.</span></span> <span data-ttu-id="12c38-109">(Para conocer las definiciones exactas de estos parámetros, consulte la documentación del método). Si el método encuentra un PIN coincidente, devuelve un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el parámetro *pPin* .</span><span class="sxs-lookup"><span data-stu-id="12c38-109">(For the exact definitions of these parameters, refer to the documentation for the method.) If the method finds a matching pin, it returns a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface in the *pPin* parameter.</span></span>

<span data-ttu-id="12c38-110">Aunque el método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) es práctico, también puede escribir sus propias funciones auxiliares si lo prefiere.</span><span class="sxs-lookup"><span data-stu-id="12c38-110">Although the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method is convenient, you can also write your own helper functions if you prefer.</span></span> <span data-ttu-id="12c38-111">Para determinar la categoría de un PIN, llame al método [**IKsPropertySet:: get**](ikspropertyset-get.md) como se describe en el tema [conjunto de propiedades](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="12c38-111">To determine a pin's category, call the [**IKsPropertySet::Get**](ikspropertyset-get.md) method as described in the topic [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="12c38-112">En el código siguiente se muestra una función auxiliar que comprueba si un PIN coincide con una categoría especificada:</span><span class="sxs-lookup"><span data-stu-id="12c38-112">The following code shows a helper function that checks whether a pin matches a specified category:</span></span>


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



<span data-ttu-id="12c38-113">El ejemplo siguiente es una función que busca un PIN por categoría, de forma similar al método [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :</span><span class="sxs-lookup"><span data-stu-id="12c38-113">The next example is a function that searches for a pin by category, similar to the [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method:</span></span>


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



<span data-ttu-id="12c38-114">En el código siguiente se usa la función Previous para buscar un PIN de puerto de vídeo en un filtro:</span><span class="sxs-lookup"><span data-stu-id="12c38-114">The following code uses the previous function to search for a video port pin on a filter:</span></span>


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



<span data-ttu-id="12c38-115">Para obtener más información acerca de los conjuntos de propiedades, consulte la documentación del [Kit de controladores de Windows (WDK)](/windows-hardware/drivers/gettingstarted/) .</span><span class="sxs-lookup"><span data-stu-id="12c38-115">For more information about property sets, refer to the [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12c38-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12c38-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12c38-117">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="12c38-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="12c38-118">Conjunto de propiedades de PIN</span><span class="sxs-lookup"><span data-stu-id="12c38-118">Pin Property Set</span></span>](pin-property-set.md)
</dt> <dt>

[<span data-ttu-id="12c38-119">Filtros de captura de vídeo de DirectShow</span><span class="sxs-lookup"><span data-stu-id="12c38-119">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> </dl>

 

 
