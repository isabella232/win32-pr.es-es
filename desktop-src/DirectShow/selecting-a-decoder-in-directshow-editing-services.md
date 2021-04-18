---
description: Seleccionar un descodificador en servicios de edición de DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Seleccionar un descodificador en servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494885"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="744a4-103">Seleccionar un descodificador en servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="744a4-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="744a4-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="744a4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="744a4-105">Cuando los [servicios de edición de DirectShow](directshow-editing-services.md) (des) representan un proyecto de edición de vídeo, el motor de representación selecciona automáticamente los descodificadores necesarios.</span><span class="sxs-lookup"><span data-stu-id="744a4-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="744a4-106">Esto puede ocurrir dentro del método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) , o bien de forma dinámica durante la representación.</span><span class="sxs-lookup"><span data-stu-id="744a4-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="744a4-107">Un usuario puede instalar varios descodificadores que pueden descodificar un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="744a4-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="744a4-108">Cuando hay varios descodificadores disponibles, DES usa el algoritmo de [conexión inteligente](intelligent-connect.md) para seleccionar el descodificador.</span><span class="sxs-lookup"><span data-stu-id="744a4-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="744a4-109">No hay ninguna manera de que la aplicación especifique directamente el descodificador que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="744a4-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="744a4-110">Sin embargo, puede elegir el descodificador indirectamente a través de la interfaz de devolución de llamada [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) .</span><span class="sxs-lookup"><span data-stu-id="744a4-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="744a4-111">Al implementar esta interfaz en la aplicación, puede recibir notificaciones durante el proceso de creación de gráficos y rechazar ciertos filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="744a4-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="744a4-112">Comience implementando una clase que exponga la interfaz [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :</span><span class="sxs-lookup"><span data-stu-id="744a4-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="744a4-113">A continuación, cree una instancia de Filter Graph Manager y registre la clase para recibir notificaciones de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="744a4-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="744a4-114">A continuación, cree el motor de representación y llame al método [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntero al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="744a4-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="744a4-115">Esto garantiza que el motor de representación no crea su propio administrador de gráficos de filtro, sino que utiliza la instancia que ha configurado para las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="744a4-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="744a4-116">Cuando se representa el proyecto, se llama al método [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) de la aplicación inmediatamente antes de que el administrador de gráficos de filtros cree un nuevo filtro.</span><span class="sxs-lookup"><span data-stu-id="744a4-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="744a4-117">El método **SelectedFilter** recibe un puntero a una interfaz **IMoniker** que representa un moniker para el filtro.</span><span class="sxs-lookup"><span data-stu-id="744a4-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="744a4-118">Examine el moniker y, si decide rechazar el filtro, devuelva un código de error del método **SelectedFilter** .</span><span class="sxs-lookup"><span data-stu-id="744a4-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="744a4-119">La parte difícil es identificar qué monikers representan descodificadores y, en concreto, qué monikers representan descodificadores que desea rechazar.</span><span class="sxs-lookup"><span data-stu-id="744a4-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="744a4-120">Una solución es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="744a4-120">One solution is the following:</span></span>

-   <span data-ttu-id="744a4-121">Antes de representar el proyecto, use el método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) para crear una lista de filtros que se registran para aceptar el tipo de entrada deseado.</span><span class="sxs-lookup"><span data-stu-id="744a4-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="744a4-122">En el caso de los tipos de compresión de audio o vídeo, esta lista debe asignarse a un conjunto de descodificadores.</span><span class="sxs-lookup"><span data-stu-id="744a4-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="744a4-123">El método **EnumMatchingFilters** devuelve una colección de monikers.</span><span class="sxs-lookup"><span data-stu-id="744a4-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="744a4-124">Para cada moniker de la colección, obtenga la propiedad **displayName** , como se describe en [usar el asignador de filtros](using-the-filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="744a4-125">Almacene una lista de los nombres para mostrar, pero omita el nombre para mostrar que coincida con el filtro que desea utilizar para la descodificación.</span><span class="sxs-lookup"><span data-stu-id="744a4-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="744a4-126">Los nombres para mostrar de los filtros de software tienen el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="744a4-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="744a4-127">where</span><span class="sxs-lookup"><span data-stu-id="744a4-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="744a4-128">es el GUID de la categoría de filtro y</span><span class="sxs-lookup"><span data-stu-id="744a4-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="744a4-129">es el CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="744a4-129">is the filter's CLSID.</span></span> <span data-ttu-id="744a4-130">En el caso de DMOs, el formato es el mismo, pero cambie `sw` a `dmo` .</span><span class="sxs-lookup"><span data-stu-id="744a4-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="744a4-131">La lista contiene ahora los nombres para mostrar de todos los filtros que generan el tipo de medio deseado, pero no el filtro preferido.</span><span class="sxs-lookup"><span data-stu-id="744a4-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="744a4-132">En el método **SelectedFilter** , obtenga la propiedad **displayName** en el moniker propuesto y compruébelo en la lista almacenada.</span><span class="sxs-lookup"><span data-stu-id="744a4-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="744a4-133">Si el nombre para mostrar coincide con una entrada de la lista, rechace ese filtro.</span><span class="sxs-lookup"><span data-stu-id="744a4-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="744a4-134">De lo contrario, se debe aceptar si se devuelven los elementos \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="744a4-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="744a4-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="744a4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="744a4-136">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="744a4-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



