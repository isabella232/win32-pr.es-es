---
description: Establecer el reloj del gráfico
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Establecer el reloj del gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686267"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="1b33f-103">Establecer el reloj del gráfico</span><span class="sxs-lookup"><span data-stu-id="1b33f-103">Setting the Graph Clock</span></span>

<span data-ttu-id="1b33f-104">Al compilar un gráfico de filtros, el administrador de gráficos de filtros elige automáticamente un reloj de referencia para el gráfico.</span><span class="sxs-lookup"><span data-stu-id="1b33f-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="1b33f-105">Todos los filtros del gráfico se sincronizan con el reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="1b33f-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="1b33f-106">En concreto, los filtros de representador usan el reloj de referencia para determinar el tiempo de presentación de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1b33f-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="1b33f-107">Por lo general, no hay ninguna razón para que una aplicación invalide el reloj de referencia del administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="1b33f-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="1b33f-108">Sin embargo, puede hacerlo llamando al método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="1b33f-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="1b33f-109">Este método toma un puntero a la interfaz **IReferenceClock** del reloj.</span><span class="sxs-lookup"><span data-stu-id="1b33f-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="1b33f-110">Llame al método mientras se detiene el gráfico.</span><span class="sxs-lookup"><span data-stu-id="1b33f-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="1b33f-111">Si un filtro proporciona un reloj, puede obtener el puntero **IReferenceClock** llamando a **QueryInterface** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="1b33f-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="1b33f-112">Como alternativa, puede implementar un reloj de referencia externo que no sea proporcionado por un filtro, siempre que el reloj externo implemente **IReferenceClock**.</span><span class="sxs-lookup"><span data-stu-id="1b33f-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="1b33f-113">En el ejemplo siguiente se muestra cómo especificar un reloj:</span><span class="sxs-lookup"><span data-stu-id="1b33f-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="1b33f-114">En este ejemplo se da por supuesto que CreateMyPrivateClock es una función definida por la aplicación que crea un reloj y devuelve un puntero **IReferenceClock** .</span><span class="sxs-lookup"><span data-stu-id="1b33f-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="1b33f-115">También puede establecer que el gráfico de filtro se ejecute sin ningún reloj, llamando a **SetSyncSource** con el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="1b33f-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="1b33f-116">Si no hay ningún reloj, el gráfico se ejecuta lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="1b33f-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="1b33f-117">Sin ningún reloj, los filtros de representador no esperan el tiempo de presentación de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1b33f-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="1b33f-118">En su lugar, representan cada ejemplo en cuanto llega.</span><span class="sxs-lookup"><span data-stu-id="1b33f-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="1b33f-119">Configurar el gráfico para que se ejecute sin un reloj es útil si desea procesar los datos rápidamente, en lugar de obtener una vista previa en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="1b33f-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b33f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b33f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b33f-121">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b33f-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="1b33f-122">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="1b33f-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="1b33f-123">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b33f-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



