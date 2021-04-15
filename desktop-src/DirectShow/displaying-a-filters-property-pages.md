---
description: Mostrar las páginas de propiedades de un filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Mostrar las páginas de propiedades de un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422770"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="f67be-103">Mostrar las páginas de propiedades de un filtro</span><span class="sxs-lookup"><span data-stu-id="f67be-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="f67be-104">Una página de propiedades es una manera de que un filtro admita las propiedades que el usuario puede establecer.</span><span class="sxs-lookup"><span data-stu-id="f67be-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="f67be-105">En este artículo se describe cómo mostrar las páginas de propiedades de un filtro en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f67be-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="f67be-106">Para obtener más información acerca de las páginas de propiedades, consulte la documentación de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f67be-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="f67be-107">Aunque muchos de los filtros que se proporcionan con DirectShow admiten páginas de propiedades, están pensados para fines de depuración y no se recomiendan para el uso de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f67be-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="f67be-108">En la mayoría de los casos, la funcionalidad equivalente se proporciona a través de una interfaz personalizada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="f67be-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="f67be-109">Una aplicación debe controlar estos filtros mediante programación, en lugar de exponer sus páginas de propiedades a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f67be-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="f67be-110">Los filtros con páginas de propiedades exponen la interfaz **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="f67be-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="f67be-111">Para determinar si un filtro define una página de propiedades, consulte el filtro de esta interfaz mediante **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f67be-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="f67be-112">Si ha creado directamente una instancia de un filtro (llamando a **CoCreateInstance**), ya tiene un puntero al filtro.</span><span class="sxs-lookup"><span data-stu-id="f67be-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="f67be-113">Si no es así, puede enumerar los filtros del gráfico mediante el método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) .</span><span class="sxs-lookup"><span data-stu-id="f67be-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="f67be-114">Para obtener más información, consulte [enumeración de objetos en un gráfico de filtros](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f67be-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="f67be-115">Una vez que tenga el puntero de interfaz **ISpecifyPropertyPages** , recupere las páginas de propiedades del filtro llamando al método **ISpecifyPropertyPages:: GetPages** .</span><span class="sxs-lookup"><span data-stu-id="f67be-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="f67be-116">Este método rellena una matriz contada de identificadores únicos globales (GUID) con el identificador de clase (CLSID) de cada página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f67be-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="f67be-117">Una matriz contada se define mediante una estructura **CAUUID** , que debe asignar pero que no tiene que inicializar.</span><span class="sxs-lookup"><span data-stu-id="f67be-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="f67be-118">El método **GetPages** asigna la matriz, que se encuentra en el miembro **pElems** de la estructura **CAUUID** .</span><span class="sxs-lookup"><span data-stu-id="f67be-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="f67be-119">Cuando haya terminado, libere la matriz mediante una llamada a la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="f67be-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="f67be-120">La función **OleCreatePropertyFrame** proporciona una manera sencilla de mostrar las páginas de propiedades dentro de un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="f67be-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="f67be-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f67be-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f67be-122">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="f67be-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



