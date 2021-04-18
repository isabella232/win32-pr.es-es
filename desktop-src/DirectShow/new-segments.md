---
description: Nuevos segmentos
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuevos segmentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686278"
---
# <a name="new-segments"></a><span data-ttu-id="c2c8c-103">Nuevos segmentos</span><span class="sxs-lookup"><span data-stu-id="c2c8c-103">New Segments</span></span>

<span data-ttu-id="c2c8c-104">Un *segmento* es un grupo de muestras multimedia que comparten una hora de inicio, una hora de detención y una velocidad de reproducción comunes.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="c2c8c-105">El método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) señala el inicio de un nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="c2c8c-106">Proporciona un método para que un filtro de origen informe de los filtros de nivel inferior que la información de hora y tasa ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="c2c8c-107">Por ejemplo, si el filtro de origen busca un punto nuevo en la secuencia, llama a **NewSegment** con la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="c2c8c-108">Algunos filtros de nivel inferior usan la información del segmento cuando procesan ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="c2c8c-109">Por ejemplo, en un formato que usa la compresión entre fotogramas, si la hora de detención cae en un fotograma Delta, es posible que el filtro de origen necesite enviar muestras adicionales después de la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="c2c8c-110">Esto permite al descodificador descodificar el fotograma delta final.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="c2c8c-111">Para determinar el fotograma final correcto, el descodificador hace referencia a la hora de detención del segmento.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="c2c8c-112">Otro ejemplo: los representadores de audio usan la velocidad de segmento junto con la velocidad de muestreo de audio para generar la salida de audio correcta.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="c2c8c-113">En el modelo de extracción, el filtro de origen inicia la llamada a **NewSegment** .</span><span class="sxs-lookup"><span data-stu-id="c2c8c-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="c2c8c-114">En el modelo de extracción, esto se realiza mediante el filtro del analizador.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="c2c8c-115">En cualquier caso, el filtro llama a **NewSegment** en el PIN de entrada de nivel inferior, que propaga la llamada al siguiente filtro, hasta que la llamada alcanza el representador.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="c2c8c-116">Los filtros deben serializar llamadas **NewSegment** con otras llamadas de streaming, como [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="c2c8c-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="c2c8c-117">El tiempo de secuencia se restablece en cero después de cada nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="c2c8c-118">Marcas de tiempo en las muestras entregadas después de que el segmento empiece desde cero.</span><span class="sxs-lookup"><span data-stu-id="c2c8c-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



