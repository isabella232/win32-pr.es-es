---
description: Modos de Run-Time MPEG-2 Demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time MPEG-2 Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152568"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="909fd-103">Modos de Run-Time MPEG-2 Demux</span><span class="sxs-lookup"><span data-stu-id="909fd-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="909fd-104">El [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux") puede funcionar en modo de inserción o en modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="909fd-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="909fd-105">En el modo de extracción, los datos proceden de un origen en directo, como una difusión de red.</span><span class="sxs-lookup"><span data-stu-id="909fd-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="909fd-106">En el modo de extracción, los datos proceden de un archivo local.</span><span class="sxs-lookup"><span data-stu-id="909fd-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="909fd-107">El modo de extracción está disponible en Windows XP y versiones posteriores, solo para secuencias de programas.</span><span class="sxs-lookup"><span data-stu-id="909fd-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="909fd-108">En plataformas de nivel inferior, use el filtro [de divisor de MPEG-2](mpeg-2-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="909fd-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="909fd-109">El modo de inserciones está disponible en todas las plataformas, tanto para flujos de programa como para flujos de transporte.</span><span class="sxs-lookup"><span data-stu-id="909fd-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="909fd-110">Por lo tanto, Demux admite tres modos posibles: secuencias de programas en modo de extracción, secuencias de programa en modo de inserción y secuencias de transporte en modo de inserción.</span><span class="sxs-lookup"><span data-stu-id="909fd-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="909fd-111">Demux determina qué modo se va a utilizar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="909fd-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="909fd-112">El modo se determina cuando se conecta el PIN de entrada o cuando se configura el primer PIN de salida, lo que suceda primero:</span><span class="sxs-lookup"><span data-stu-id="909fd-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="909fd-113">Cuando el PIN de entrada se conecta: en Windows XP y versiones posteriores, el Demux consulta el filtro de nivel superior para la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Si el filtro de nivel superior expone esa interfaz, el Demux se configura a sí mismo para los flujos de programa en el modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="909fd-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="909fd-114">De lo contrario, el Demux usa el modo de extracción y el tipo de medio determina el tipo de secuencia (flujo de programa o secuencia de transporte).</span><span class="sxs-lookup"><span data-stu-id="909fd-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="909fd-115">Consulte [**tipos de medios de desmultiplexado MPEG-2**](mpeg-2-demultiplexer-media-types.md) para obtener una lista de tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="909fd-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="909fd-116">Cuando se configura el primer PIN de salida: Si crea un PIN de salida y lo consulta para [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), el Demux se configura para flujos de transporte en el modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="909fd-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="909fd-117">Si consulta el PIN de [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), el Demux se configura a sí mismo para los flujos de programa, también en el modo de extracción.</span><span class="sxs-lookup"><span data-stu-id="909fd-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="909fd-118">Se producirá un error en las consultas posteriores de la otra interfaz, ya que Demux no puede funcionar en dos modos a la vez.</span><span class="sxs-lookup"><span data-stu-id="909fd-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="909fd-119">Una vez que Demux se ha configurado para un modo determinado, permanece en ese modo.</span><span class="sxs-lookup"><span data-stu-id="909fd-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="909fd-120">Para usar un modo diferente, debe crear una nueva instancia de Demux.</span><span class="sxs-lookup"><span data-stu-id="909fd-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="909fd-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="909fd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="909fd-122">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="909fd-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



