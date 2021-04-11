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
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="9a365-103">Buscar una interfaz en un filtro o un PIN</span><span class="sxs-lookup"><span data-stu-id="9a365-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="9a365-104">Para muchas operaciones en DirectShow, la aplicación llama a los métodos en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="9a365-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="9a365-105">En algunas situaciones, sin embargo, la aplicación debe llamar a un método directamente en un filtro o un PIN.</span><span class="sxs-lookup"><span data-stu-id="9a365-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="9a365-106">Por ejemplo, muchos filtros exponen interfaces especializadas que se usan para configurar el filtro.</span><span class="sxs-lookup"><span data-stu-id="9a365-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="9a365-107">En el caso de una interfaz de filtro, es posible que ya tenga un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.</span><span class="sxs-lookup"><span data-stu-id="9a365-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="9a365-108">En ese caso, simplemente use **QueryInterface** para obtener la otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a365-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="9a365-109">Pero es posible que el administrador de gráficos de filtro agregue algunos filtros al gráfico.</span><span class="sxs-lookup"><span data-stu-id="9a365-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="9a365-110">(Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md)). En ese caso, use la interfaz [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) para recorrer todos los filtros del gráfico y consultar cada uno de ellos a su vez.</span><span class="sxs-lookup"><span data-stu-id="9a365-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="9a365-111">La siguiente función muestra esto:</span><span class="sxs-lookup"><span data-stu-id="9a365-111">The following function demonstrates this:</span></span>


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



<span data-ttu-id="9a365-112">Para buscar una interfaz en un PIN, use la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) para recorrer los pin de un filtro.</span><span class="sxs-lookup"><span data-stu-id="9a365-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="9a365-113">La siguiente función muestra cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="9a365-113">The following function shows how to do this:</span></span>


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



<span data-ttu-id="9a365-114">La función siguiente busca una interfaz en un filtro o un PIN:</span><span class="sxs-lookup"><span data-stu-id="9a365-114">The next function searches for an interface on a filter or a pin:</span></span>


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



<span data-ttu-id="9a365-115">Tenga en cuenta que todas las funciones que se muestran aquí se detienen en el primer **QueryInterface** correcto.</span><span class="sxs-lookup"><span data-stu-id="9a365-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a365-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a365-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a365-117">Enumerar filtros</span><span class="sxs-lookup"><span data-stu-id="9a365-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="9a365-118">Enumerar PIN</span><span class="sxs-lookup"><span data-stu-id="9a365-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="9a365-119">**ICaptureGraphBuilder2::FindInterface**</span><span class="sxs-lookup"><span data-stu-id="9a365-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



