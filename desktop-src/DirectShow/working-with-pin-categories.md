---
description: Trabajar con categorías de pin
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Trabajar con categorías de pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272556"
---
# <a name="working-with-pin-categories"></a>Trabajar con categorías de pin

Para buscar en un filtro para un pin con una categoría de pin determinada, puede usar el método [**ICaptureGraphBuilder2::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) En el ejemplo siguiente se busca un pin de vista previa de vídeo:


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



El primer parámetro es un puntero a la interfaz [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro. Los tres parámetros siguientes especifican la dirección, la categoría de anclado y el tipo de medio. El valor **FALSE** del quinto parámetro indica que el pin puede estar conectado o no conectado. (Para obtener las definiciones exactas de estos parámetros, consulte la documentación del método ). Si el método encuentra un pin correspondiente, devuelve un puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el *parámetro pPin.*

Aunque el [**método FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) es cómodo, también puede escribir sus propias funciones auxiliares si lo prefiere. Para determinar la categoría de un pin, llame al método [**IKsPropertySet::Get**](ikspropertyset-get.md) como se describe en el tema [Pin Property Set](pin-property-set.md).

El código siguiente muestra una función auxiliar que comprueba si un pin coincide con una categoría especificada:


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



El ejemplo siguiente es una función que busca un pin por categoría, similar al [**método FindPin:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)


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



El código siguiente usa la función anterior para buscar un pin de puerto de vídeo en un filtro:


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



Para obtener más información sobre los conjuntos de propiedades, consulte la [documentación Windows Driver Kit (WDK).](/windows-hardware/drivers/gettingstarted/)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Anclar conjunto de propiedades](pin-property-set.md)
</dt> <dt>

[DirectShow Filtros de captura de vídeo](directshow-video-capture-filters.md)
</dt> </dl>

 

 
