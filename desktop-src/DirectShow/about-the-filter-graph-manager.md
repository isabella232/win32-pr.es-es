---
description: Acerca del administrador de gráficos de filtros
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Acerca del administrador de gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537833"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="7dac5-103">Acerca del administrador de gráficos de filtros</span><span class="sxs-lookup"><span data-stu-id="7dac5-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="7dac5-104">[Filter Graph Manager](filter-graph-manager.md) es un objeto com que controla los filtros de un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7dac5-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="7dac5-105">Realiza muchas funciones, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="7dac5-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="7dac5-106">Coordinación de los cambios de estado entre los filtros.</span><span class="sxs-lookup"><span data-stu-id="7dac5-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="7dac5-107">Establecer un reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="7dac5-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="7dac5-108">Comunicar los eventos de nuevo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dac5-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="7dac5-109">Proporcionar métodos para que las aplicaciones generen el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7dac5-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="7dac5-110">Cada una de estas funciones se describe brevemente aquí.</span><span class="sxs-lookup"><span data-stu-id="7dac5-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="7dac5-111">Los detalles se pueden encontrar en cualquier parte de la documentación.</span><span class="sxs-lookup"><span data-stu-id="7dac5-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="7dac5-112">**Cambios de estado**.</span><span class="sxs-lookup"><span data-stu-id="7dac5-112">**State changes**.</span></span> <span data-ttu-id="7dac5-113">Los cambios de estado dentro de los filtros deben aparecer en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="7dac5-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="7dac5-114">Por lo tanto, la aplicación no emite comandos de cambio de estado directamente a los filtros.</span><span class="sxs-lookup"><span data-stu-id="7dac5-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="7dac5-115">En su lugar, proporciona un solo comando al administrador de gráficos de filtro, que distribuye el comando a cada uno de los filtros.</span><span class="sxs-lookup"><span data-stu-id="7dac5-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="7dac5-116">La búsqueda funciona de manera similar: la aplicación proporciona un comando de búsqueda al administrador de gráficos de filtro, que lo distribuye a los filtros.</span><span class="sxs-lookup"><span data-stu-id="7dac5-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="7dac5-117">**Reloj de referencia**.</span><span class="sxs-lookup"><span data-stu-id="7dac5-117">**Reference clock**.</span></span> <span data-ttu-id="7dac5-118">Todos los filtros del gráfico usan el mismo reloj, denominado *reloj de referencia*.</span><span class="sxs-lookup"><span data-stu-id="7dac5-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="7dac5-119">El reloj de referencia garantiza que todos los flujos están sincronizados.</span><span class="sxs-lookup"><span data-stu-id="7dac5-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="7dac5-120">La hora a la que se debe representar un fotograma de vídeo o un ejemplo de audio se denomina *tiempo de presentación*.</span><span class="sxs-lookup"><span data-stu-id="7dac5-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="7dac5-121">El tiempo de presentación se mide en relación con el reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="7dac5-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="7dac5-122">El administrador de gráficos de filtro elige un reloj de referencia, normalmente el reloj de la tarjeta de sonido o el reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="7dac5-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="7dac5-123">**Eventos de gráfico**.</span><span class="sxs-lookup"><span data-stu-id="7dac5-123">**Graph events**.</span></span> <span data-ttu-id="7dac5-124">Filter Graph Manager usa una cola de eventos para informar a la aplicación de los eventos que se producen en el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7dac5-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="7dac5-125">Este mecanismo es similar a un bucle de mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="7dac5-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="7dac5-126">**Métodos de creación de gráficos**.</span><span class="sxs-lookup"><span data-stu-id="7dac5-126">**Graph-building methods**.</span></span> <span data-ttu-id="7dac5-127">Filter Graph Manager proporciona métodos para que la aplicación agregue filtros al gráfico, conecte filtros a otros filtros y desconecte filtros.</span><span class="sxs-lookup"><span data-stu-id="7dac5-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="7dac5-128">Una función que el administrador de gráficos de filtro no controla es mover los datos de un filtro al siguiente.</span><span class="sxs-lookup"><span data-stu-id="7dac5-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="7dac5-129">Esto se realiza mediante los propios filtros, a través de sus conexiones de PIN.</span><span class="sxs-lookup"><span data-stu-id="7dac5-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="7dac5-130">El procesamiento se produce siempre en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="7dac5-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="7dac5-131">Los filtros siempre son de subproceso libre, residen en el mismo proceso que el administrador de gráficos de filtro y se cargan desde servidores en proceso.</span><span class="sxs-lookup"><span data-stu-id="7dac5-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="7dac5-132">Por lo tanto, no se calculan las referencias de las llamadas a métodos entre los filtros o entre los filtros y el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="7dac5-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7dac5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dac5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dac5-134">Flujo de datos en el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="7dac5-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="7dac5-135">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7dac5-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="7dac5-136">Establecer el reloj del gráfico</span><span class="sxs-lookup"><span data-stu-id="7dac5-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="7dac5-137">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7dac5-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



