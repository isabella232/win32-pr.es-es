---
description: Buscar un elemento filters del mismo nivel
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Buscar un elemento filters del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079882"
---
# <a name="find-a-filters-peer"></a>Buscar un elemento filters del mismo nivel

Dado un filtro, puede recorrer el gráfico buscando los filtros a los que está conectado. Empiece por enumerar los PIN del filtro. Para cada pin, compruebe si ese pin está conectado a otro PIN. Si es así, consulte el otro PIN para su filtro propietario. Puede recorrer el gráfico en la dirección ascendente mediante la enumeración de los pin de entrada del filtro o en la dirección de nivel inferior mediante la enumeración de los pin de salida.

La siguiente función realiza una búsqueda ascendente o descendente para un filtro conectado. Devuelve el primer filtro coincidente que encuentra:


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



La función llama a [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para enumerar los PIN del primer filtro. Para cada pin, llama a [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para comprobar si el PIN coincide con la dirección especificada (entrada o salida). Si es así, la función determina si ese pin está conectado a otro PIN, llamando al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) . Por último, llama a [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) en el PIN conectado. Este método devuelve una estructura que contiene, entre otras cosas, un puntero al filtro propietario de ese pin. Este puntero se devuelve al autor de la llamada en el parámetro *ppNext* . El llamador debe liberar el puntero.

En el código siguiente se muestra cómo llamar a esta función:


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Un filtro podría estar conectado a dos o más filtros en cualquier dirección. Por ejemplo, podría tratarse de un filtro divisor, con varios filtros de nivel inferior. O bien, podría ser un filtro MUX, con varios filtros ascendentes desde él. Por lo tanto, es posible que desee recopilar todos ellos en una lista.

En el código siguiente se muestra una posible manera de implementar este tipo de función. Usa la clase [**CGenericList**](cgenericlist.md) de DirectShow; podría escribir una función equivalente con otra estructura de datos.


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



Para complicar en cierto modo, un filtro puede tener varias conexiones de PIN al mismo filtro. Para evitar poner duplicados en la lista, consulte cada puntero **IBaseFilter** para **IUnknown** y compare los punteros **IUnknown** . Por las reglas de COM, dos punteros de interfaz hacen referencia al mismo objeto solo si devuelven punteros **IUnknown** idénticos. En el ejemplo anterior, la función AddFilterUnique controla este detalle.

En el ejemplo siguiente se muestra cómo usar la función GetPeerFilters:


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas generales de Graph-Building](general-graph-building-techniques.md)
</dt> </dl>

 

 



