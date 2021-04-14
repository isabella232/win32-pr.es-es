---
description: Captura de audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104360002"
---
# <a name="audio-capture"></a><span data-ttu-id="89d3b-103">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="89d3b-103">Audio Capture</span></span>

<span data-ttu-id="89d3b-104">Una aplicación puede usar DirectShow para capturar datos de audio de micrófonos, reproductores de cinta y otros dispositivos a través de las entradas de la tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="89d3b-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="89d3b-105">Entre los escenarios típicos se incluyen:</span><span class="sxs-lookup"><span data-stu-id="89d3b-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="89d3b-106">Grabar una narración de VoiceOver para grabaciones posteriores en una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="89d3b-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="89d3b-107">Conversión de contenido de audio analógico heredado a formato digital.</span><span class="sxs-lookup"><span data-stu-id="89d3b-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="89d3b-108">Capturar voz o música para su transmisión a través de una red.</span><span class="sxs-lookup"><span data-stu-id="89d3b-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="89d3b-109">Los usuarios finales tienen varias opciones para capturar audio de la tarjeta de sonido en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="89d3b-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="89d3b-110">La mayoría de las tarjetas proporcionan aplicaciones para mezclar y grabar desde sus entradas de audio.</span><span class="sxs-lookup"><span data-stu-id="89d3b-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="89d3b-111">Windows proporciona grabadora de sonidos, una sencilla aplicación de utilidad para grabar desde un micrófono.</span><span class="sxs-lookup"><span data-stu-id="89d3b-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="89d3b-112">El codificador de Windows Media se puede incorporar en una aplicación de DirectShow como un [objeto multimedia de DirectX](directx-media-objects.md) (DMO).</span><span class="sxs-lookup"><span data-stu-id="89d3b-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="89d3b-113">En esta sección se describe cómo integrar la funcionalidad de captura de audio dentro de su propia aplicación mediante DirectShow.</span><span class="sxs-lookup"><span data-stu-id="89d3b-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="89d3b-114">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="89d3b-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="89d3b-115">Acerca del filtro de captura de audio</span><span class="sxs-lookup"><span data-stu-id="89d3b-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="89d3b-116">Selección de un dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="89d3b-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="89d3b-117">Creación de un gráfico de captura de audio</span><span class="sxs-lookup"><span data-stu-id="89d3b-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="89d3b-118">Creación de un gráfico de captura de audio con vista previa</span><span class="sxs-lookup"><span data-stu-id="89d3b-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="89d3b-119">Establecer propiedades de captura de audio</span><span class="sxs-lookup"><span data-stu-id="89d3b-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="89d3b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89d3b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d3b-121">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="89d3b-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



