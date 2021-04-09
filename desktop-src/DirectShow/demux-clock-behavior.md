---
description: Comportamiento del reloj de Demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamiento del reloj de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080007"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="ad584-103">Comportamiento del reloj de Demux</span><span class="sxs-lookup"><span data-stu-id="ad584-103">Demux Clock Behavior</span></span>

<span data-ttu-id="ad584-104">En el modo de extracción, el demultiplexador MPEG-2 (Demux) expone la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="ad584-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="ad584-105">Actúa como un origen en directo, por lo que se elegirá como el reloj de referencia del gráfico de forma predeterminada. vea [orígenes en directo](live-sources.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ad584-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="ad584-106">En el caso de las secuencias de transporte, el Demux sincroniza su reloj con el flujo de PCR que corresponde a la secuencia de audio o de vídeo asignada más recientemente por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ad584-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="ad584-107">Internamente, Demux realiza un seguimiento de las tablas PAT y PMT.</span><span class="sxs-lookup"><span data-stu-id="ad584-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="ad584-108">Cuando la aplicación asigna un PID de flujo elemental a un terminal de salida, Demux busca el flujo de PCR para ese PID y usa ese flujo de PCR.</span><span class="sxs-lookup"><span data-stu-id="ad584-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="ad584-109">(Actualmente, no hay forma de que la aplicación especifique el PID de PCR directamente).</span><span class="sxs-lookup"><span data-stu-id="ad584-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="ad584-110">En el caso de las secuencias de programa, Demux sincroniza su reloj con el flujo de SCR.</span><span class="sxs-lookup"><span data-stu-id="ad584-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="ad584-111">Sincronizar el reloj del filtro con el flujo PCR o SCR impide el desbordamiento o subdesbordamiento de los datos, lo que podría dar lugar a que el reloj del gráfico varíe desde el reloj de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ad584-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="ad584-112">El Demux también traduce los valores PTS de PES en horas de referencia de DirectShow y usa estos valores para la marca de tiempo de los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="ad584-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="ad584-113">Las marcas de tiempo se aplican al límite del marco siguiente; no hay ninguna garantía de que el límite del marco se alinee con el inicio del ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad584-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="ad584-114">Demux garantiza que las marcas de tiempo aumentan de una vez más.</span><span class="sxs-lookup"><span data-stu-id="ad584-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="ad584-115">Esto significa, por ejemplo, que si una secuencia de transporte incluye un segmento como un comercial que se creó con un reloj diferente que el programa principal, el Demux ajustará las marcas de tiempo de presentación para ocultar la discontinuidad de tiempo de los filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ad584-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad584-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad584-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad584-117">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ad584-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



