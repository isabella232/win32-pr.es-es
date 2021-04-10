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
# <a name="connect-two-filters"></a><span data-ttu-id="a73ff-103">Conectar dos filtros</span><span class="sxs-lookup"><span data-stu-id="a73ff-103">Connect Two Filters</span></span>

<span data-ttu-id="a73ff-104">En este tema se muestran algunas funciones auxiliares para conectar filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a73ff-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="a73ff-105">Para conectar dos filtros, debe buscar un PIN de salida no conectado en el filtro de nivel superior y un PIN de entrada sin conexión en el filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a73ff-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="a73ff-106">Si ya tiene punteros a ambos PIN, llame al método [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectarlos.</span><span class="sxs-lookup"><span data-stu-id="a73ff-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="a73ff-107">Si los PIN no se pueden conectar directamente entre sí, el método **IGraphBuilder:: Connect** podría insertar filtros adicionales para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="a73ff-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="a73ff-108">Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="a73ff-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="a73ff-109">Si tiene un puntero a los filtros pero no a los pin, debe usar el método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para buscar los pin.</span><span class="sxs-lookup"><span data-stu-id="a73ff-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="a73ff-110">(Consulte [enumeración de PIN](enumerating-pins.md)). En las funciones auxiliares de este tema se muestra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="a73ff-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="a73ff-111">PIN de salida para filtrar</span><span class="sxs-lookup"><span data-stu-id="a73ff-111">Output Pin to Filter</span></span>

<span data-ttu-id="a73ff-112">La siguiente función toma dos parámetros: un puntero a un terminal de salida y un puntero a un filtro.</span><span class="sxs-lookup"><span data-stu-id="a73ff-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="a73ff-113">La función conecta el PIN de salida al primer PIN de entrada disponible en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a73ff-113">The function connects the output pin to the first available input pin on the filter.</span></span>


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



<span data-ttu-id="a73ff-114">Esta función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a73ff-114">This function does the following:</span></span>

1.  <span data-ttu-id="a73ff-115">Llama `FindUnconnectedPin` a la función para obtener un PIN de entrada no conectado.</span><span class="sxs-lookup"><span data-stu-id="a73ff-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="a73ff-116">Esta función se muestra en el tema [búsqueda de un PIN no conectado en un filtro](find-an-unconnected-pin-on-a-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a73ff-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="a73ff-117">Llama a [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) para conectar los dos pines.</span><span class="sxs-lookup"><span data-stu-id="a73ff-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="a73ff-118">Filtrar a pin de entrada</span><span class="sxs-lookup"><span data-stu-id="a73ff-118">Filter to Input Pin</span></span>

<span data-ttu-id="a73ff-119">La siguiente función toma un puntero a un filtro y un puntero a un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a73ff-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="a73ff-120">Conecta el PIN de entrada al primer PIN de salida disponible en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a73ff-120">It connects the input pin to the first available output pin on the filter.</span></span>


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



### <a name="filter-to-filter"></a><span data-ttu-id="a73ff-121">Filtrar para filtrar</span><span class="sxs-lookup"><span data-stu-id="a73ff-121">Filter to Filter</span></span>

<span data-ttu-id="a73ff-122">La tercera función toma un puntero a un filtro de nivel superior y un puntero a un filtro de nivel inferior e intenta conectar ambos filtros.</span><span class="sxs-lookup"><span data-stu-id="a73ff-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a73ff-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a73ff-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73ff-124">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="a73ff-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="a73ff-125">**ICaptureGraphBuilder2:: RenderStream**</span><span class="sxs-lookup"><span data-stu-id="a73ff-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



