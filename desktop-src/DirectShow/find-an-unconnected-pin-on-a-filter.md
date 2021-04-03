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
# <a name="find-an-unconnected-pin-on-a-filter"></a>Buscar un PIN no conectado en un filtro

En este tema se describe cómo buscar un PIN no conectado en un filtro. La búsqueda de un PIN no conectado resulta útil cuando se conectan filtros.

En un escenario típico de creación de gráficos de DirectShow, se necesita un PIN no conectado que coincida con una dirección de PIN determinada (entrada o salida). Por ejemplo, cuando se conectan dos filtros, se conecta un PIN de salida de un filtro a un punto de entrada del otro filtro. Ambos PIN deben estar sin conexión antes de conectarlos.

En primer lugar, se necesita una función que prueba si un PIN está conectado a otro PIN. Esta función llama al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para probar si el PIN está conectado a otro PIN.


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
> En este ejemplo se usa la función [SafeRelease](/windows/desktop/medfound/saferelease) para liberar punteros de interfaz.

 

A continuación, se necesita una función que prueba si un PIN coincide con una dirección de PIN especificada. Esta función llama al método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obtener la dirección del PIN.


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



La función siguiente coincide con un PIN según los criterios (dirección del PIN y estado de la conexión).


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



Por último, la función siguiente usa la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer los PIN del filtro. El autor de la llamada especifica la dirección de PIN deseada. Para cada pin, la función llama `MatchPin` a para comprobar si el PIN es una coincidencia. Si la dirección coincide y el PIN está desconectado, la función devuelve un puntero al pin correspondiente en el parámetro *ppPin* .


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



Para obtener un ejemplo de cómo se puede usar esta función, consulte [Connect Two filters](connect-two-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar PIN](enumerating-pins.md)
</dt> <dt>

[Técnicas generales de Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
