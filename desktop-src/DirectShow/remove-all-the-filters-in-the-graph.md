---
description: Quitar todos los filtros del gráfico
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Quitar todos los filtros del gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805876"
---
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="b4856-103">Quitar todos los filtros del gráfico</span><span class="sxs-lookup"><span data-stu-id="b4856-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="b4856-104">La forma más fácil de quitar todos los filtros de un gráfico de filtros es simplemente liberar el administrador de gráficos de filtro y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="b4856-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="b4856-105">Asegúrese de liberar todos los punteros que la aplicación tenga a cualquier interfaz de los administradores de gráficos de filtro, así como punteros a objetos del gráfico, incluidos filtros, PIN, el reloj de referencia, etc.</span><span class="sxs-lookup"><span data-stu-id="b4856-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="b4856-106">Como alternativa, puede quitar los filtros de uno en uno, mediante el método [**IFilterGraph:: removeFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :</span><span class="sxs-lookup"><span data-stu-id="b4856-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



<span data-ttu-id="b4856-107">En este ejemplo se usa el método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) para enumerar los filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="b4856-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="b4856-108">Al quitar un filtro, el objeto de enumerador deja de estar sincronizado con el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b4856-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="b4856-109">Use el método [**IEnumFilters:: RESET**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) para restablecer el enumerador.</span><span class="sxs-lookup"><span data-stu-id="b4856-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="b4856-110">De lo contrario, se producirá un error en cualquier llamada subsiguiente a [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) .</span><span class="sxs-lookup"><span data-stu-id="b4856-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



