---
description: Flujo de datos para desarrolladores de filtros
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flujo de datos para desarrolladores de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080062"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="1f82a-103">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="1f82a-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="1f82a-104">En esta sección se describe en detalle cómo se mueven los datos a través del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="1f82a-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="1f82a-105">Se centra en el transporte de memoria local mediante la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) o [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="1f82a-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="1f82a-106">Está dirigido a los desarrolladores que escriben sus propios filtros personalizados.</span><span class="sxs-lookup"><span data-stu-id="1f82a-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="1f82a-107">Para obtener una introducción general al modo en que Microsoft DirectShow controla el flujo de datos, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="1f82a-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="1f82a-108">Muchos datos se desplazan a través de un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="1f82a-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="1f82a-109">Se divide en dos categorías aproximadamente: datos multimedia y datos de control.</span><span class="sxs-lookup"><span data-stu-id="1f82a-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="1f82a-110">En general, los datos multimedia viajan hacia abajo y los datos de control están ascendentes.</span><span class="sxs-lookup"><span data-stu-id="1f82a-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="1f82a-111">Los datos multimedia incluyen fotogramas de vídeo, muestras de audio, paquetes MPEG, etc. que componen una secuencia, pero también incluyen comandos de vaciado, notificaciones de final de secuencia y otros datos que viajan con la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1f82a-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="1f82a-112">Los datos de control no forman parte de la secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="1f82a-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="1f82a-113">Ejemplos de datos de control son las solicitudes de control de calidad y los comandos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1f82a-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="1f82a-114">Esta sección contiene los siguientes artículos.</span><span class="sxs-lookup"><span data-stu-id="1f82a-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="1f82a-115">Entrega de ejemplos</span><span class="sxs-lookup"><span data-stu-id="1f82a-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="1f82a-116">Procesamiento de datos</span><span class="sxs-lookup"><span data-stu-id="1f82a-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="1f82a-117">Notificaciones de final de secuencia</span><span class="sxs-lookup"><span data-stu-id="1f82a-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="1f82a-118">Nuevos segmentos</span><span class="sxs-lookup"><span data-stu-id="1f82a-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="1f82a-119">Vaciar</span><span class="sxs-lookup"><span data-stu-id="1f82a-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="1f82a-120">Invoca</span><span class="sxs-lookup"><span data-stu-id="1f82a-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="1f82a-121">Cambios en el formato dinámico</span><span class="sxs-lookup"><span data-stu-id="1f82a-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="1f82a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f82a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f82a-123">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="1f82a-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="1f82a-124">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="1f82a-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="1f82a-125">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f82a-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



