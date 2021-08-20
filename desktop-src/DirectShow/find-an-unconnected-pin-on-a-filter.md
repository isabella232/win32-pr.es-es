---
description: En este tema se describe cómo buscar un pin no relacionado en un filtro. La búsqueda de un pin no conectado es útil al conectar filtros.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Buscar un pin no conectados en un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a76100622f0398c58eb10f2dda041ba074f4610efbd1c649d48199ea2c676eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401759"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Buscar un pin no conectados en un filtro

En este tema se describe cómo buscar un pin no relacionado en un filtro. La búsqueda de un pin no conectado es útil al conectar filtros.

En un escenario DirectShow creación de gráficos, necesita un pin no desconectado que coincida con una dirección de pin determinada (entrada o salida). Por ejemplo, cuando se conectan dos filtros, se conecta un pin de salida de un filtro a un pin de entrada del otro filtro. Ambos pines deben estar desconectados antes de conectarlos.

En primer lugar, necesitamos una función que comprueba si un pin está conectado a otro pin. Esta función llama al [**método IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) para probar si el pin está conectado a otro pin.


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
> En este ejemplo se usa [la función SafeRelease para](/windows/desktop/medfound/saferelease) liberar punteros de interfaz.

 

A continuación, necesitamos una función que comprueba si un pin coincide con una dirección de pin especificada. Esta función llama al [**método IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para obtener la dirección del pin.


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



La siguiente función coincide con un pin según ambos criterios (dirección de anclado y estado de conexión).


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



Por último, la función siguiente usa la [**interfaz IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer en bucle los pines del filtro. El autor de la llamada especifica la dirección de anclado deseada. Para cada pin, la función llama `MatchPin` a para probar si el pin es una coincidencia. Si la dirección coincide y el pin no está desconectado, la función devuelve un puntero al pin correspondiente en el *parámetro ppPin.*


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



Para obtener un ejemplo de cómo se puede usar esta función, [vea Conectar Two Filters](connect-two-filters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración de pins](enumerating-pins.md)
</dt> <dt>

[Técnicas Graph-Building generales](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
