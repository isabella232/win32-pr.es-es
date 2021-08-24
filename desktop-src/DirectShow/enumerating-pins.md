---
description: Enumeración de pins
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Enumeración de pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748715"
---
# <a name="enumerating-pins"></a>Enumeración de pins

Los filtros [**admiten el método IBaseFilter::EnumPins,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) que enumera los pines disponibles en el filtro. Devuelve un puntero a la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) El [**método IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) recupera punteros de interfaz [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

En el ejemplo siguiente se muestra una función que busca un pin con una dirección determinada (entrada o salida) en un filtro determinado. Usa la [**enumeración \_ PIN DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) para especificar la dirección del pin y el método [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para buscar la dirección de cada pin enumerado. Si esta función encuentra un pin de coincidencia, devuelve un puntero de **interfaz IPin** con un recuento de referencias pendiente. El autor de la llamada es responsable de liberar la interfaz.


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

[Buscar un pin no desconectado en un filtro](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Técnicas Graph-Building general](general-graph-building-techniques.md)
</dt> <dt>

[Anclar conjunto de propiedades](pin-property-set.md)
</dt> </dl>

 

 



