---
description: Interfaces para controlar un gráfico de filtros
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces para controlar un gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806481"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="df141-103">Interfaces para controlar un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="df141-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="df141-104">Estas interfaces proporcionan métodos para controlar un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="df141-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="df141-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="df141-105">Interface</span></span>                                  | <span data-ttu-id="df141-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="df141-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df141-107">**IAMClockAdjust**</span><span class="sxs-lookup"><span data-stu-id="df141-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="df141-108">Ajuste el reloj del gráfico.</span><span class="sxs-lookup"><span data-stu-id="df141-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="df141-109">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="df141-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="df141-110">Sincronizar secuencias en directo en un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="df141-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="df141-111">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="df141-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="df141-112">Controlan las cadenas de filtros.</span><span class="sxs-lookup"><span data-stu-id="df141-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="df141-113">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="df141-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="df141-114">Ejecutar, pausar y detener el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="df141-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="df141-115">(También proporciona métodos compatibles con automatización para crear gráficos).</span><span class="sxs-lookup"><span data-stu-id="df141-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="df141-116">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="df141-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="df141-117">Responder a eventos en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="df141-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="df141-118">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="df141-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="df141-119">Buscar dentro de un archivo.</span><span class="sxs-lookup"><span data-stu-id="df141-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="df141-120">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="df141-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="df141-121">Comandos de cola que se ejecutarán más adelante.</span><span class="sxs-lookup"><span data-stu-id="df141-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="df141-122">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="df141-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="df141-123">Marco: recorra paso a paso un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="df141-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



