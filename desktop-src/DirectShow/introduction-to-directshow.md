---
description: Introducción a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introducción a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152280"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="1852c-103">Introducción a DirectShow</span><span class="sxs-lookup"><span data-stu-id="1852c-103">Introduction to DirectShow</span></span>

<span data-ttu-id="1852c-104">Microsoft® DirectShow® es una arquitectura para el streaming de contenido multimedia en la plataforma de® de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1852c-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="1852c-105">DirectShow proporciona una captura y reproducción de alta calidad de flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="1852c-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="1852c-106">Admite una amplia variedad de formatos, entre los que se incluyen Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio capa 3 (MP3) y archivos de sonido WAV.</span><span class="sxs-lookup"><span data-stu-id="1852c-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="1852c-107">Admite la captura desde dispositivos digitales y analógicos basados en el Modelo de controlador de Windows (WDM) o vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="1852c-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="1852c-108">Detecta y usa automáticamente hardware de aceleración de vídeo y audio cuando está disponible, pero también admite sistemas sin hardware de aceleración.</span><span class="sxs-lookup"><span data-stu-id="1852c-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="1852c-109">DirectShow se basa en el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="1852c-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="1852c-110">Para escribir una aplicación o un componente de DirectShow, debe entender la programación del cliente COM.</span><span class="sxs-lookup"><span data-stu-id="1852c-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="1852c-111">Para la mayoría de las aplicaciones, no es necesario implementar sus propios objetos COM.</span><span class="sxs-lookup"><span data-stu-id="1852c-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="1852c-112">DirectShow proporciona los componentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="1852c-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="1852c-113">Sin embargo, si desea extender DirectShow escribiendo sus propios componentes, debe implementarlos como objetos COM.</span><span class="sxs-lookup"><span data-stu-id="1852c-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="1852c-114">DirectShow está diseñado para C++.</span><span class="sxs-lookup"><span data-stu-id="1852c-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="1852c-115">Microsoft no proporciona una API administrada para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1852c-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="1852c-116">DirectShow simplifica la reproducción multimedia, la conversión de formato y las tareas de captura.</span><span class="sxs-lookup"><span data-stu-id="1852c-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="1852c-117">Al mismo tiempo, proporciona acceso a la arquitectura de control de flujo subyacente para las aplicaciones que requieren soluciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1852c-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="1852c-118">También puede crear sus propios componentes de DirectShow para admitir nuevos formatos o efectos personalizados.</span><span class="sxs-lookup"><span data-stu-id="1852c-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="1852c-119">Algunos ejemplos de los tipos de aplicación que se pueden escribir con DirectShow son reproductores de archivos, reproductores de TV y DVD, aplicaciones de edición de vídeo, convertidores de formato de archivo, aplicaciones de captura de vídeo de audio, codificadores y descodificadores, procesadores de señal digital, etc.</span><span class="sxs-lookup"><span data-stu-id="1852c-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="1852c-120">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="1852c-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1852c-121">Novedades de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1852c-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="1852c-122">Formatos admitidos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="1852c-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="1852c-123">Preguntas más frecuentes sobre DirectShow</span><span class="sxs-lookup"><span data-stu-id="1852c-123">DirectShow FAQ</span></span>](directshow-faq.md)

## <a name="related-topics"></a><span data-ttu-id="1852c-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1852c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1852c-125">Introducción</span><span class="sxs-lookup"><span data-stu-id="1852c-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="1852c-126">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="1852c-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



