---
title: Acerca de la discontinuidad
description: Acerca de la discontinuidad
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, discontinuidad de audio
- Complementos DSP, discontinuidad de audio
- Complementos de DSP de audio, discontinuidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418418"
---
# <a name="about-discontinuity"></a><span data-ttu-id="138cb-108">Acerca de la discontinuidad</span><span class="sxs-lookup"><span data-stu-id="138cb-108">About Discontinuity</span></span>

<span data-ttu-id="138cb-109">En cualquier momento, Windows Media Player puede señalar una interrupción en el flujo de entrada mediante una llamada al método **IMediaObject::D iscontinuity** .</span><span class="sxs-lookup"><span data-stu-id="138cb-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="138cb-110">Esto se produce habitualmente al principio y al final de una secuencia, y también antes de cada operación de búsqueda o cuando se interrumpe el contenido de streaming por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="138cb-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="138cb-111">El complemento DSP de ejemplo que genera el Asistente para complementos de Windows Media Player no necesita tratar con discontinuidad por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="138cb-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="138cb-112">Los ejemplos de PCM son atómicos, lo que significa que se pueden procesar sin tener en cuenta los demás ejemplos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="138cb-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="138cb-113">Algunos formatos de vídeo contienen datos que dependen de fotogramas clave y ejemplos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="138cb-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="138cb-114">El código de ejemplo se escribe para obligar siempre al cliente a procesar todos los resultados antes de que el complemento acepte más entradas.</span><span class="sxs-lookup"><span data-stu-id="138cb-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="138cb-115">La implementación predeterminada de **IMediaObject::D iscontinuity** simplemente devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="138cb-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="138cb-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="138cb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="138cb-117">**Implementar un complemento de DSP de audio**</span><span class="sxs-lookup"><span data-stu-id="138cb-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




