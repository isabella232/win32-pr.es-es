---
description: Buscar una interfaz en un filtro o un pin
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Buscar una interfaz en un filtro o un pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819567"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Buscar una interfaz en un filtro o un pin

Para muchas operaciones en DirectShow, la aplicación llama a métodos en filter Graph Manager. Sin embargo, en algunas situaciones, la aplicación debe llamar a un método directamente en un filtro o un pin. Por ejemplo, muchos filtros exponen interfaces especializadas que se usan para configurar el filtro.

En el caso de una interfaz de filtro, es posible que ya tenga un puntero a la interfaz [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro. En ese caso, simplemente use **QueryInterface** para obtener la otra interfaz. Sin embargo, el Administrador de filtros Graph podría agregar algunos filtros al gráfico. (Para más información, consulte [Intelligent Conectar).](intelligent-connect.md) En ese caso, use la [**interfaz IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) para recorrer en bucle todos los filtros del gráfico y consultar cada uno a su vez. La siguiente función muestra lo siguiente:


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



Para buscar una interfaz en un pin, use la [**interfaz IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer en bucle los pines de un filtro. La siguiente función muestra cómo hacerlo:


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



La función siguiente busca una interfaz en un filtro o un pin:


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



Tenga en cuenta que todas las funciones que se muestran aquí se detienen en el primer **objeto QueryInterface correcto.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración de filtros](enumerating-filters.md)
</dt> <dt>

[Enumeración de pins](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



