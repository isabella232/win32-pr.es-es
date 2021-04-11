---
description: Buscar una interfaz en un filtro o un PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Buscar una interfaz en un filtro o un PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274623"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Buscar una interfaz en un filtro o un PIN

Para muchas operaciones en DirectShow, la aplicación llama a los métodos en el administrador de gráficos de filtro. En algunas situaciones, sin embargo, la aplicación debe llamar a un método directamente en un filtro o un PIN. Por ejemplo, muchos filtros exponen interfaces especializadas que se usan para configurar el filtro.

En el caso de una interfaz de filtro, es posible que ya tenga un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro. En ese caso, simplemente use **QueryInterface** para obtener la otra interfaz. Pero es posible que el administrador de gráficos de filtro agregue algunos filtros al gráfico. (Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md)). En ese caso, use la interfaz [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) para recorrer todos los filtros del gráfico y consultar cada uno de ellos a su vez. La siguiente función muestra esto:


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



Para buscar una interfaz en un PIN, use la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer los pin de un filtro. La siguiente función muestra cómo hacerlo:


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



La función siguiente busca una interfaz en un filtro o un PIN:


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



Tenga en cuenta que todas las funciones que se muestran aquí se detienen en el primer **QueryInterface** correcto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar filtros](enumerating-filters.md)
</dt> <dt>

[Enumerar PIN](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



