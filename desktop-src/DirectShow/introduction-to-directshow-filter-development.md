---
description: Introducción al desarrollo de filtros de DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introducción al desarrollo de filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686332"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="fb69e-103">Introducción al desarrollo de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb69e-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="fb69e-104">En esta sección se proporciona una breve descripción de las tareas relacionadas con el desarrollo de un filtro DirectShow personalizado.</span><span class="sxs-lookup"><span data-stu-id="fb69e-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="fb69e-105">También se proporcionan vínculos a temas que describen estas tareas con mayor detalle.</span><span class="sxs-lookup"><span data-stu-id="fb69e-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="fb69e-106">Antes de leer esta sección, lea los temas [sobre DirectShow](about-directshow.md), que describen la arquitectura de DirectShow general.</span><span class="sxs-lookup"><span data-stu-id="fb69e-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="fb69e-107">**Biblioteca de clases base de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="fb69e-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="fb69e-108">El SDK de DirectShow incluye un conjunto de clases de C++ para escribir filtros.</span><span class="sxs-lookup"><span data-stu-id="fb69e-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="fb69e-109">Aunque no son necesarios, estas clases son la manera recomendada de escribir un nuevo filtro.</span><span class="sxs-lookup"><span data-stu-id="fb69e-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="fb69e-110">Para usar las clases base, compílelo en una biblioteca estática y vincule el archivo. lib al proyecto, tal como se describe en [crear filtros de DirectShow](building-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="fb69e-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="fb69e-111">La biblioteca de clases base define una clase raíz para los filtros, la clase [**CBaseFilter**](cbasefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="fb69e-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="fb69e-112">Otras clases se derivan de **CBaseFilter** y se especializan en determinados tipos de filtros.</span><span class="sxs-lookup"><span data-stu-id="fb69e-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="fb69e-113">Por ejemplo, la clase [**CTransformFilter**](ctransformfilter.md) está diseñada para los filtros de transformación.</span><span class="sxs-lookup"><span data-stu-id="fb69e-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="fb69e-114">Para crear un nuevo filtro, implemente una clase que herede de una de las clases de filtro.</span><span class="sxs-lookup"><span data-stu-id="fb69e-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="fb69e-115">Por ejemplo, la declaración de clase podría ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb69e-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="fb69e-116">Para obtener más información acerca de las clases base de DirectShow, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb69e-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="fb69e-117">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb69e-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="fb69e-118">Compilar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb69e-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="fb69e-119">**Crear PIN**</span><span class="sxs-lookup"><span data-stu-id="fb69e-119">**Creating Pins**</span></span>

<span data-ttu-id="fb69e-120">Un filtro debe crear uno o varios PIN.</span><span class="sxs-lookup"><span data-stu-id="fb69e-120">A filter must create one or more pins.</span></span> <span data-ttu-id="fb69e-121">El número de clavijas se puede corregir en tiempo de diseño o el filtro puede crear nuevos PIN según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="fb69e-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="fb69e-122">Los pin generalmente derivan de la clase [**CBasePin**](cbasepin.md) o de una clase que hereda **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="fb69e-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="fb69e-123">Los PIN del filtro se deben declarar como variables de miembro en la clase de filtro.</span><span class="sxs-lookup"><span data-stu-id="fb69e-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="fb69e-124">Algunas de las clases de filtro ya definen los pin, pero si el filtro hereda directamente de **CBaseFilter**, debe declarar los pin en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="fb69e-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="fb69e-125">**Negociar conexiones de anclaje**</span><span class="sxs-lookup"><span data-stu-id="fb69e-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="fb69e-126">Cuando el administrador de gráficos de filtro intenta conectar dos filtros, los pin deben estar de acuerdo en varias cosas.</span><span class="sxs-lookup"><span data-stu-id="fb69e-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="fb69e-127">Si no es así, se produce un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="fb69e-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="fb69e-128">Por lo general, los pin negocian lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb69e-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="fb69e-129">Transport.</span><span class="sxs-lookup"><span data-stu-id="fb69e-129">Transport.</span></span> <span data-ttu-id="fb69e-130">El transporte es el mecanismo que los filtros usarán para trasladar los ejemplos de medios del PIN de salida al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb69e-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="fb69e-131">Por ejemplo, pueden utilizar la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo de inserción") o la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de extracción").</span><span class="sxs-lookup"><span data-stu-id="fb69e-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="fb69e-132">Tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fb69e-132">Media type.</span></span> <span data-ttu-id="fb69e-133">Casi todos los pin usan tipos de medios para describir el formato de los datos que van a proporcionar.</span><span class="sxs-lookup"><span data-stu-id="fb69e-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="fb69e-134">Asignador.</span><span class="sxs-lookup"><span data-stu-id="fb69e-134">Allocator.</span></span> <span data-ttu-id="fb69e-135">El asignador es el objeto que crea los búferes que contienen los datos.</span><span class="sxs-lookup"><span data-stu-id="fb69e-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="fb69e-136">Los pin deben aceptar qué PIN proporcionará el asignador.</span><span class="sxs-lookup"><span data-stu-id="fb69e-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="fb69e-137">También deben estar de acuerdo en el tamaño de los búferes, el número de búferes que se van a crear y otras propiedades de búfer.</span><span class="sxs-lookup"><span data-stu-id="fb69e-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="fb69e-138">Las clases base implementan un marco para estas negociaciones.</span><span class="sxs-lookup"><span data-stu-id="fb69e-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="fb69e-139">Debe completar los detalles invalidando varios métodos en la clase base.</span><span class="sxs-lookup"><span data-stu-id="fb69e-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="fb69e-140">El conjunto de métodos que debe reemplazar depende de la clase y de la funcionalidad del filtro.</span><span class="sxs-lookup"><span data-stu-id="fb69e-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="fb69e-141">Para obtener más información, consulte [cómo se conectan los filtros](how-filters-connect.md).</span><span class="sxs-lookup"><span data-stu-id="fb69e-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="fb69e-142">**Procesamiento y entrega de datos**</span><span class="sxs-lookup"><span data-stu-id="fb69e-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="fb69e-143">La función principal de la mayoría de los filtros es procesar y proporcionar datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="fb69e-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="fb69e-144">La forma en que se produce depende del tipo de filtro:</span><span class="sxs-lookup"><span data-stu-id="fb69e-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="fb69e-145">Un origen de la inserciones tiene un subproceso de trabajo que rellena continuamente los ejemplos con datos y los entrega de forma descendente.</span><span class="sxs-lookup"><span data-stu-id="fb69e-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="fb69e-146">Un origen de extracción espera a que su vecino de nivel inferior solicite un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb69e-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="fb69e-147">Responde escribiendo datos en un ejemplo y entregando el ejemplo al filtro de bajada.</span><span class="sxs-lookup"><span data-stu-id="fb69e-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="fb69e-148">El filtro de nivel inferior crea el subproceso que controla el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="fb69e-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="fb69e-149">Un filtro de transformación tiene ejemplos que se le entregan por su vecino ascendente.</span><span class="sxs-lookup"><span data-stu-id="fb69e-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="fb69e-150">Cuando recibe un ejemplo, procesa los datos y los entrega de bajada.</span><span class="sxs-lookup"><span data-stu-id="fb69e-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="fb69e-151">Un filtro de representador recibe ejemplos de nivel superior y los programa para su representación en función de las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb69e-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="fb69e-152">Otras tareas relacionadas con el streaming incluyen el vaciado de datos del gráfico, el control del final de la secuencia y la respuesta a las solicitudes de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fb69e-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="fb69e-153">Para obtener más información acerca de estos problemas, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb69e-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="fb69e-154">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="fb69e-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="fb69e-155">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="fb69e-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="fb69e-156">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="fb69e-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="fb69e-157">**COM compatible**</span><span class="sxs-lookup"><span data-stu-id="fb69e-157">**Supporting COM**</span></span>

<span data-ttu-id="fb69e-158">Los filtros de DirectShow son objetos COM, normalmente empaquetados en archivos dll.</span><span class="sxs-lookup"><span data-stu-id="fb69e-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="fb69e-159">La biblioteca de clases base implementa un marco de trabajo para la compatibilidad con COM.</span><span class="sxs-lookup"><span data-stu-id="fb69e-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="fb69e-160">Se describe en la sección [DirectShow y com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="fb69e-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb69e-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb69e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb69e-162">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb69e-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



