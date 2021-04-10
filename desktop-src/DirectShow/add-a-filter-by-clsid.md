---
description: Agregar un filtro por CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Agregar un filtro por CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152604"
---
# <a name="add-a-filter-by-clsid"></a><span data-ttu-id="ede5f-103">Agregar un filtro por CLSID</span><span class="sxs-lookup"><span data-stu-id="ede5f-103">Add a Filter by CLSID</span></span>

<span data-ttu-id="ede5f-104">La función siguiente crea un filtro con un identificador de clase (CLSID) especificado y lo agrega al gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="ede5f-104">The following function creates a filter with a specified class identifier (CLSID) and adds it to the filter graph:</span></span>


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
> <span data-ttu-id="ede5f-105">En este ejemplo se usa la función [SafeRelease](/windows/desktop/medfound/saferelease) para liberar el puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="ede5f-105">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>

 

<span data-ttu-id="ede5f-106">La función llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el filtro y, a continuación, llama a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico.</span><span class="sxs-lookup"><span data-stu-id="ede5f-106">The function calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the filter, and then calls [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span> <span data-ttu-id="ede5f-107">En el ejemplo de código siguiente se usa esta función para agregar el filtro de [AVI](avi-mux-filter.md) en el gráfico:</span><span class="sxs-lookup"><span data-stu-id="ede5f-107">The following code example uses this function to add the [AVI Mux](avi-mux-filter.md) filter to the graph:</span></span>


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



<span data-ttu-id="ede5f-108">Tenga en cuenta que algunos filtros no se pueden crear con [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="ede5f-108">Note that some filters cannot be created with [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="ede5f-109">Este suele ser el caso de los filtros que administran otros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="ede5f-109">This is often the case with filters that manage other software components.</span></span> <span data-ttu-id="ede5f-110">Por ejemplo, el filtro del [compresor AVI](avi-compressor-filter.md) es un contenedor de códecs de vídeo y el filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) es un contenedor para los controladores de captura WDM.</span><span class="sxs-lookup"><span data-stu-id="ede5f-110">For example, the [AVI Compressor](avi-compressor-filter.md) filter is a wrapper for video codecs, and the [WDM Video Capture](wdm-video-capture-filter.md) filter is a wrapper for WDM capture drivers.</span></span> <span data-ttu-id="ede5f-111">Estos filtros deben crearse mediante el [enumerador de dispositivos del sistema](system-device-enumerator.md) o el [asignador de filtros](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="ede5f-111">These filters must be created using either the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="ede5f-112">Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ede5f-112">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ede5f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ede5f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede5f-114">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="ede5f-114">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
