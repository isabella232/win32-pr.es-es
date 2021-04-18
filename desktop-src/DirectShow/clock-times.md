---
description: Horas de reloj
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de reloj
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422790"
---
# <a name="clock-times"></a><span data-ttu-id="d8087-103">Horas de reloj</span><span class="sxs-lookup"><span data-stu-id="d8087-103">Clock Times</span></span>

<span data-ttu-id="d8087-104">DirectShow define dos horas de reloj relacionadas: tiempo de referencia y tiempo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d8087-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="d8087-105">El *tiempo de referencia* es la hora absoluta devuelta por el reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="d8087-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="d8087-106">(Consulte [relojes de referencia](reference-clocks.md)).</span><span class="sxs-lookup"><span data-stu-id="d8087-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="d8087-107">La hora de la *secuencia* se define en relación con la última vez que se inició la ejecución del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d8087-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="d8087-108">Mientras se ejecuta el gráfico, el tiempo de secuencia es igual a la hora de referencia menos a la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="d8087-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="d8087-109">Mientras el gráfico está en pausa, el tiempo de flujo permanece en el momento de la secuencia cuando se pausó.</span><span class="sxs-lookup"><span data-stu-id="d8087-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="d8087-110">Después de una operación de búsqueda, el tiempo de secuencia se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="d8087-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="d8087-111">Mientras se detiene el gráfico, el tiempo de secuencia no está definido.</span><span class="sxs-lookup"><span data-stu-id="d8087-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="d8087-112">Cuando un ejemplo multimedia tiene una marca de tiempo *t*, significa que el ejemplo se debe representar en el momento del flujo *t*.</span><span class="sxs-lookup"><span data-stu-id="d8087-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="d8087-113">Por esta razón, el tiempo de flujo también se denomina *tiempo de presentación*.</span><span class="sxs-lookup"><span data-stu-id="d8087-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="d8087-114">Cuando una aplicación llama a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico de filtros, el administrador de gráficos de filtros llama a [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) en cada filtro.</span><span class="sxs-lookup"><span data-stu-id="d8087-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="d8087-115">Para compensar el ligero tiempo necesario para que los filtros empiecen a ejecutarse, el administrador de gráficos de filtro especifica una hora de inicio ligeramente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d8087-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8087-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8087-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8087-117">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d8087-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d8087-118">Marcas de tiempo</span><span class="sxs-lookup"><span data-stu-id="d8087-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



