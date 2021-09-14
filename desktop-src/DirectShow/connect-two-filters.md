---
description: En este tema se muestran algunas funciones auxiliares para conectar DirectShow filtros.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Conectar Dos filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161581"
---
# <a name="connect-two-filters"></a>Conectar Dos filtros

En este tema se muestran algunas funciones auxiliares para conectar DirectShow filtros.

Para conectar dos filtros, debe encontrar un pin de salida no conectado en el filtro ascendente y un pin de entrada no conectado en el filtro de bajada.

Si ya tiene punteros a ambos pines, llame al método [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectarlos. Si los pines no se pueden conectar directamente entre sí, el método **IGraphBuilder::Conectar** podría insertar filtros adicionales para completar la conexión. Para obtener más información, vea [Intelligent Conectar](intelligent-connect.md).

Si tiene un puntero a los filtros, pero no a los pines, debe usar el método [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para buscar los pines. (Consulte [Enumeración de patillas).](enumerating-pins.md) Las funciones auxiliares de este tema muestran esta técnica.

### <a name="output-pin-to-filter"></a>Pin de salida para filtrar

La función siguiente toma dos parámetros: un puntero a un pin de salida y un puntero a un filtro. La función conecta el pin de salida al primer pin de entrada disponible en el filtro.


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



Esta función hace lo siguiente:

1.  Llama a `FindUnconnectedPin` la función para obtener una patilla de entrada no conectada. Esta función se muestra en el tema Buscar un pin [no relacionado en un filtro](find-an-unconnected-pin-on-a-filter.md).
2.  Llama [**a IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar los dos pines.

### <a name="filter-to-input-pin"></a>Filtro a pin de entrada

La función siguiente toma un puntero a un filtro y un puntero a un pin de entrada. Conecta el pin de entrada al primer pin de salida disponible en el filtro.


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a>Filtrar a filtro

La tercera función toma un puntero a un filtro ascendente y un puntero a un filtro de nivel inferior e intenta conectar ambos filtros.


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de Graph-Building generales](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



