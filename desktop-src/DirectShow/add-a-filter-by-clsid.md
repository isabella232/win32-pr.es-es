---
description: Agregar un filtro por CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Agregar un filtro por CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8306613e5a73ad863b3c16b04529e3e0def12b76fb4e27685db9cb442b6c80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873435"
---
# <a name="add-a-filter-by-clsid"></a>Agregar un filtro por CLSID

La función siguiente crea un filtro con un identificador de clase especificado (CLSID) y lo agrega al gráfico de filtros:


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> En este ejemplo se usa [la función SafeRelease](/windows/desktop/medfound/saferelease) para liberar el [**puntero IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)

 

La función llama [**a CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el filtro y, a continuación, llama a [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico. En el ejemplo de código siguiente se usa esta función para agregar el [filtro AVI Mux](avi-mux-filter.md) al gráfico:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Tenga en cuenta que algunos filtros no se pueden crear [**con CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Este suele ser el caso de los filtros que administran otros componentes de software. Por ejemplo, el filtro [avi Deserción es](avi-compressor-filter.md) un contenedor para códecs de vídeo y el filtro captura de vídeo [wdm](wdm-video-capture-filter.md) es un contenedor para los controladores de captura wdm. Estos filtros deben crearse mediante el enumerador [de dispositivos del sistema](system-device-enumerator.md) o el [asignador de filtros.](filter-mapper.md) Para obtener más información, [vea Enumerar dispositivos y filtros.](enumerating-devices-and-filters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas Graph-Building general](general-graph-building-techniques.md)
</dt> </dl>

 

 
