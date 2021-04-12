---
description: Televisión analógica
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisión analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152246"
---
# <a name="analog-television"></a><span data-ttu-id="81e8e-103">Televisión analógica</span><span class="sxs-lookup"><span data-stu-id="81e8e-103">Analog Television</span></span>

<span data-ttu-id="81e8e-104">La televisión analógica es diferente de otros escenarios de captura de vídeo de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="81e8e-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="81e8e-105">La tarjeta de sintonizador se ajusta a una señal analógica, que luego se digitaliza.</span><span class="sxs-lookup"><span data-stu-id="81e8e-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="81e8e-106">El audio se lleva a cabo en la señal analógica.</span><span class="sxs-lookup"><span data-stu-id="81e8e-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="81e8e-107">La forma en que el audio alcanza la tarjeta de sonido varía en función del hardware.</span><span class="sxs-lookup"><span data-stu-id="81e8e-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="81e8e-108">La señal puede contener datos adicionales en el intervalo de espacio en blanco (VBI) vertical, como subtítulos (CC), teletexto estándar universal (elemento WST) y Extended Data Services (XDS).</span><span class="sxs-lookup"><span data-stu-id="81e8e-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="81e8e-109">En el diagrama siguiente se muestra un gráfico de filtro típico para la vista previa de televisión.</span><span class="sxs-lookup"><span data-stu-id="81e8e-109">The following diagram shows a typical filter graph for television preview.</span></span>

![gráfico de televisión analógica](images/vidcap06.png)

-   <span data-ttu-id="81e8e-111">El filtro de [sintonizador de TV](tv-tuner-filter.md) controla la optimización.</span><span class="sxs-lookup"><span data-stu-id="81e8e-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="81e8e-112">El filtro de [audio de TV](tv-audio-filter.md) controla la descodificación de audio.</span><span class="sxs-lookup"><span data-stu-id="81e8e-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="81e8e-113">Si la tarjeta de sintonizador tiene más de una entrada física, el filtro de [Cruz de vídeo analógico](analog-video-crossbar-filter.md) permite a la aplicación seleccionar qué entrada se descodifica y se representa.</span><span class="sxs-lookup"><span data-stu-id="81e8e-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="81e8e-114">El filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) entrega el flujo de vídeo digitalizado.</span><span class="sxs-lookup"><span data-stu-id="81e8e-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="81e8e-115">El generador de gráficos de captura inserta automáticamente los filtros que se requieren al ascendente desde el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="81e8e-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="81e8e-116">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="81e8e-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="81e8e-117">Optimización de televisión analógica</span><span class="sxs-lookup"><span data-stu-id="81e8e-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="81e8e-118">Audio analógico de televisión</span><span class="sxs-lookup"><span data-stu-id="81e8e-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="81e8e-119">Subtítulos y teletexto</span><span class="sxs-lookup"><span data-stu-id="81e8e-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="81e8e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81e8e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81e8e-121">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="81e8e-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



