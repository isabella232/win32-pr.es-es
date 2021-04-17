---
description: Enumerar filtros
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Enumerar filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de0f979973d339b790b04a8a5d4d98fc52c95c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652315"
---
# <a name="enumerating-filters"></a><span data-ttu-id="439ae-103">Enumerar filtros</span><span class="sxs-lookup"><span data-stu-id="439ae-103">Enumerating Filters</span></span>

<span data-ttu-id="439ae-104">Filter Graph Manager admite el método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , que enumera todos los filtros del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="439ae-104">The Filter Graph Manager supports the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method, which enumerates all the filters in the filter graph.</span></span> <span data-ttu-id="439ae-105">Devuelve un puntero a la interfaz [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) .</span><span class="sxs-lookup"><span data-stu-id="439ae-105">It returns a pointer to the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface.</span></span> <span data-ttu-id="439ae-106">El método [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) recupera punteros de interfaz de [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="439ae-106">The [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) method retrieves [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointers.</span></span>

<span data-ttu-id="439ae-107">En el ejemplo siguiente se muestra una función que enumera los filtros de un gráfico y muestra un cuadro de mensaje con el nombre de cada filtro.</span><span class="sxs-lookup"><span data-stu-id="439ae-107">The following example shows a function that enumerates the filters in a graph and displays a message box with each filter's name.</span></span> <span data-ttu-id="439ae-108">Usa el método [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) para recuperar el nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="439ae-108">It uses the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method to retrieve the name of the filter.</span></span> <span data-ttu-id="439ae-109">Tenga en cuenta los lugares en los que la función llama a **Release** en una interfaz para reducir el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="439ae-109">Note the places where the function calls **Release** on an interface to decrement the reference count.</span></span>


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="439ae-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="439ae-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439ae-111">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="439ae-111">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



