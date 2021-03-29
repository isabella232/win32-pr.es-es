---
description: Buscar un elemento filters del mismo nivel
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Buscar un elemento filters del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079882"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="90597-103">Buscar un elemento filters del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="90597-103">Find a Filters Peer</span></span>

<span data-ttu-id="90597-104">Dado un filtro, puede recorrer el gráfico buscando los filtros a los que está conectado.</span><span class="sxs-lookup"><span data-stu-id="90597-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="90597-105">Empiece por enumerar los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="90597-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="90597-106">Para cada pin, compruebe si ese pin está conectado a otro PIN.</span><span class="sxs-lookup"><span data-stu-id="90597-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="90597-107">Si es así, consulte el otro PIN para su filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="90597-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="90597-108">Puede recorrer el gráfico en la dirección ascendente mediante la enumeración de los pin de entrada del filtro o en la dirección de nivel inferior mediante la enumeración de los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="90597-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="90597-109">La siguiente función realiza una búsqueda ascendente o descendente para un filtro conectado.</span><span class="sxs-lookup"><span data-stu-id="90597-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="90597-110">Devuelve el primer filtro coincidente que encuentra:</span><span class="sxs-lookup"><span data-stu-id="90597-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="90597-111">La función llama a [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para enumerar los PIN del primer filtro.</span><span class="sxs-lookup"><span data-stu-id="90597-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="90597-112">Para cada pin, llama a [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) para comprobar si el PIN coincide con la dirección especificada (entrada o salida).</span><span class="sxs-lookup"><span data-stu-id="90597-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="90597-113">Si es así, la función determina si ese pin está conectado a otro PIN, llamando al método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="90597-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="90597-114">Por último, llama a [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) en el PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="90597-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="90597-115">Este método devuelve una estructura que contiene, entre otras cosas, un puntero al filtro propietario de ese pin.</span><span class="sxs-lookup"><span data-stu-id="90597-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="90597-116">Este puntero se devuelve al autor de la llamada en el parámetro *ppNext* .</span><span class="sxs-lookup"><span data-stu-id="90597-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="90597-117">El llamador debe liberar el puntero.</span><span class="sxs-lookup"><span data-stu-id="90597-117">The caller must release the pointer.</span></span>

<span data-ttu-id="90597-118">En el código siguiente se muestra cómo llamar a esta función:</span><span class="sxs-lookup"><span data-stu-id="90597-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="90597-119">Un filtro podría estar conectado a dos o más filtros en cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="90597-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="90597-120">Por ejemplo, podría tratarse de un filtro divisor, con varios filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="90597-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="90597-121">O bien, podría ser un filtro MUX, con varios filtros ascendentes desde él.</span><span class="sxs-lookup"><span data-stu-id="90597-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="90597-122">Por lo tanto, es posible que desee recopilar todos ellos en una lista.</span><span class="sxs-lookup"><span data-stu-id="90597-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="90597-123">En el código siguiente se muestra una posible manera de implementar este tipo de función.</span><span class="sxs-lookup"><span data-stu-id="90597-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="90597-124">Usa la clase [**CGenericList**](cgenericlist.md) de DirectShow; podría escribir una función equivalente con otra estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="90597-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="90597-125">Para complicar en cierto modo, un filtro puede tener varias conexiones de PIN al mismo filtro.</span><span class="sxs-lookup"><span data-stu-id="90597-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="90597-126">Para evitar poner duplicados en la lista, consulte cada puntero **IBaseFilter** para **IUnknown** y compare los punteros **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="90597-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="90597-127">Por las reglas de COM, dos punteros de interfaz hacen referencia al mismo objeto solo si devuelven punteros **IUnknown** idénticos.</span><span class="sxs-lookup"><span data-stu-id="90597-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="90597-128">En el ejemplo anterior, la función AddFilterUnique controla este detalle.</span><span class="sxs-lookup"><span data-stu-id="90597-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="90597-129">En el ejemplo siguiente se muestra cómo usar la función GetPeerFilters:</span><span class="sxs-lookup"><span data-stu-id="90597-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="90597-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90597-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90597-131">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="90597-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



