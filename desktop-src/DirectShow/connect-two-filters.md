---
description: En este tema se muestran algunas funciones auxiliares para conectar filtros de DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Conectar dos filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152452"
---
# <a name="connect-two-filters"></a>Conectar dos filtros

En este tema se muestran algunas funciones auxiliares para conectar filtros de DirectShow.

Para conectar dos filtros, debe buscar un PIN de salida no conectado en el filtro de nivel superior y un PIN de entrada sin conexión en el filtro de nivel inferior.

Si ya tiene punteros a ambos PIN, llame al método [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectarlos. Si los PIN no se pueden conectar directamente entre sí, el método **IGraphBuilder:: Connect** podría insertar filtros adicionales para completar la conexión. Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md).

Si tiene un puntero a los filtros pero no a los pin, debe usar el método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para buscar los pin. (Consulte [enumeración de PIN](enumerating-pins.md)). En las funciones auxiliares de este tema se muestra esta técnica.

### <a name="output-pin-to-filter"></a>PIN de salida para filtrar

La siguiente función toma dos parámetros: un puntero a un terminal de salida y un puntero a un filtro. La función conecta el PIN de salida al primer PIN de entrada disponible en el filtro.


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

1.  Llama `FindUnconnectedPin` a la función para obtener un PIN de entrada no conectado. Esta función se muestra en el tema [búsqueda de un PIN no conectado en un filtro](find-an-unconnected-pin-on-a-filter.md).
2.  Llama a [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar los dos pines.

### <a name="filter-to-input-pin"></a>Filtrar a pin de entrada

La siguiente función toma un puntero a un filtro y un puntero a un PIN de entrada. Conecta el PIN de entrada al primer PIN de salida disponible en el filtro.


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



### <a name="filter-to-filter"></a>Filtrar para filtrar

La tercera función toma un puntero a un filtro de nivel superior y un puntero a un filtro de nivel inferior e intenta conectar ambos filtros.


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

[Técnicas generales de Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



