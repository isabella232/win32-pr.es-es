---
title: Low-Delay audio
description: Low-Delay audio
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio con retraso bajo
- SDK de Windows Media Format, compatibilidad de audio
- códecs, audio con retraso bajo
- códecs, compatibilidad de audio
- audio con retraso bajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695464"
---
# <a name="low-delay-audio"></a><span data-ttu-id="5477b-108">Low-Delay audio</span><span class="sxs-lookup"><span data-stu-id="5477b-108">Low-Delay Audio</span></span>

<span data-ttu-id="5477b-109">El audio de retraso bajo es un modo de codificación que genera audio comprimido con una configuración de ventana de búfer más pequeña que otros modos.</span><span class="sxs-lookup"><span data-stu-id="5477b-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="5477b-110">Esto resulta útil para las secuencias que se deben cambiar rápidamente durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5477b-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="5477b-111">El escenario típico de esta característica es una presentación en streaming que incluye la capacidad de cambiar el contenido de forma arbitraria, como cambiar el canal de un televisor.</span><span class="sxs-lookup"><span data-stu-id="5477b-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="5477b-112">Cuando se usa un formato de audio de retraso bajo, la latencia para cambiar el contenido se reduce drásticamente en comparación con otros formatos de audio.</span><span class="sxs-lookup"><span data-stu-id="5477b-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="5477b-113">También se reduce la latencia para las difusiones en vivo cuando se usan formatos de retraso bajo.</span><span class="sxs-lookup"><span data-stu-id="5477b-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="5477b-114">Esta característica es compatible con los códecs Windows Media Audio 9,1 y Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="5477b-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="5477b-115">Los formatos de retraso bajo solo están disponibles para la codificación de velocidad de bits constante (tanto un paso como dos pasos).</span><span class="sxs-lookup"><span data-stu-id="5477b-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5477b-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5477b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5477b-117">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="5477b-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




