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
# <a name="enumerating-pins"></a>Enumerar PIN

Los filtros admiten el método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , que enumera los pin disponibles en el filtro. Devuelve un puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . El método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera punteros de interfaz de [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

En el ejemplo siguiente se muestra una función que busca un pin con una dirección determinada (entrada o salida) en un filtro determinado. Usa la enumeración [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar la dirección del PIN y el método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para encontrar la dirección de cada pin enumerado. Si esta función encuentra un PIN coincidente, devuelve un puntero de la interfaz **IPin** con un recuento de referencias pendiente. El autor de la llamada es responsable de liberar la interfaz.


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



Esta función se puede modificar fácilmente para devolver el PIN n con la dirección especificada o el PIN *n* no conectado. (Para averiguar si un PIN está conectado a otro PIN, llame al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar objetos en un gráfico de filtros](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Buscar un PIN no conectado en un filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Técnicas generales de Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[Conjunto de propiedades de PIN](pin-property-set.md)
</dt> </dl>

 

 



