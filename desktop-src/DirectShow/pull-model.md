---
description: Modelo de extracción
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modelo de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537161"
---
# <a name="pull-model"></a><span data-ttu-id="9c4a0-103">Modelo de extracción</span><span class="sxs-lookup"><span data-stu-id="9c4a0-103">Pull Model</span></span>

<span data-ttu-id="9c4a0-104">En la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , el filtro de nivel superior determina qué datos se van a enviar e incorpora los datos al filtro de bajada.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="9c4a0-105">En algunos filtros, un modelo de *extracción* es más adecuado.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="9c4a0-106">Aquí, el filtro de nivel inferior solicita datos del filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="9c4a0-107">Los ejemplos siguen viajando hacia abajo, desde la clavija de salida a la clavija de entrada, pero el filtro de nivel inferior inicia el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="9c4a0-108">Este tipo de conexión utiliza la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="9c4a0-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="9c4a0-109">El uso típico del modelo de extracción es la reproducción de archivos.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="9c4a0-110">Por ejemplo, en un gráfico de reproducción de AVI, el filtro de [origen de archivo asincrónico](file-source--async--filter.md) realiza operaciones de lectura de archivos genéricas y entrega los datos como un flujo de bytes, sin información de formato.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="9c4a0-111">El filtro de [divisor de AVI](avi-splitter-filter.md) Lee los encabezados AVI y analiza el flujo en muestras de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="9c4a0-112">El divisor de AVI puede determinar qué datos necesita mejor que el filtro de origen de archivo asincrónico y, por lo tanto, usa **IAsyncReader** en lugar de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="9c4a0-113">Para solicitar datos del PIN de salida, el PIN de entrada llama a uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c4a0-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="9c4a0-114">**IAsyncReader:: Request**</span><span class="sxs-lookup"><span data-stu-id="9c4a0-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="9c4a0-115">**IAsyncReader::SyncRead**</span><span class="sxs-lookup"><span data-stu-id="9c4a0-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="9c4a0-116">[**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="9c4a0-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="9c4a0-117">El primer método es asincrónico, para admitir varias lecturas superpuestas.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="9c4a0-118">Los demás son sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-118">The others are synchronous.</span></span>

<span data-ttu-id="9c4a0-119">En teoría, cualquier filtro puede admitir **IAsyncReader**, pero en la práctica está diseñado para los filtros de origen que se conectan a los filtros del analizador.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="9c4a0-120">El analizador actúa de forma muy similar a un filtro de origen en el modelo de extracción.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="9c4a0-121">Cuando se pausa, se crea un subproceso de streaming que extrae datos de la conexión **IAsyncReader** y los envía a nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="9c4a0-122">Los pin de salida usan **IMemInputPin** y el resto del gráfico usa el modelo de la instalación estándar.</span><span class="sxs-lookup"><span data-stu-id="9c4a0-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c4a0-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c4a0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c4a0-124">Flujo de datos en el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="9c4a0-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



