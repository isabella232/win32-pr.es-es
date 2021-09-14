---
description: Enumeración de pins
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumeración de pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273004"
---
# <a name="enumerating-pins"></a>Enumeración de pins

Los filtros [**admiten el método IBaseFilter::EnumPins,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) que enumera los pines disponibles en el filtro. Devuelve un puntero a la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) El [**método IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera punteros [**de interfaz IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

En el ejemplo siguiente se muestra una función que busca un pin con una dirección determinada (entrada o salida) en un filtro determinado. Usa la [**enumeración PIN \_ DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar la dirección del pin y el método [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para buscar la dirección de cada pin enumerado. Si esta función encuentra un pin correspondiente, devuelve un puntero de interfaz **IPin** con un recuento de referencias pendiente. El autor de la llamada es responsable de liberar la interfaz.


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



Esta función se puede modificar fácilmente para devolver el enésimo pin con la dirección especificada o el *n.º* pin no asociado. (Para averiguar si un pin está conectado a otro pin, llame al [**método IPin::ConnectedTo).**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar objetos en un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Buscar un pin no conectados en un filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Técnicas de Graph-Building generales](general-graph-building-techniques.md)
</dt> <dt>

[Anclar conjunto de propiedades](pin-property-set.md)
</dt> </dl>

 

 



