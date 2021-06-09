---
description: Introducción a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introducción a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827229"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="4fdd2-103">Introducción a DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fdd2-103">Introduction to DirectShow</span></span>

<span data-ttu-id="4fdd2-104">Microsoft® DirectShow® es una arquitectura para los medios de streaming en la plataforma microsoft windows®.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="4fdd2-105">DirectShow proporciona captura y reproducción de alta calidad de secuencias multimedia.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="4fdd2-106">Admite una amplia variedad de formatos, incluidos advanced systems format (ASF), motion picture experts group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) y archivos de sonido WAV.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="4fdd2-107">Admite la captura desde dispositivos digitales y análogos basados en Modelo de controlador de Windows (WDM) o Video para Windows.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="4fdd2-108">Detecta y usa automáticamente hardware de aceleración de vídeo y audio cuando está disponible, pero también admite sistemas sin hardware de aceleración.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="4fdd2-109">DirectShow se basa en el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="4fdd2-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="4fdd2-110">Para escribir una aplicación o componente de DirectShow, debe comprender la programación del cliente COM.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="4fdd2-111">Para la mayoría de las aplicaciones, no es necesario implementar sus propios objetos COM.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="4fdd2-112">DirectShow proporciona los componentes que necesita.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="4fdd2-113">Sin embargo, si desea extender DirectShow escribiendo sus propios componentes, debe implementarlos como objetos COM.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="4fdd2-114">DirectShow está diseñado para C++.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="4fdd2-115">Microsoft no proporciona una API administrada para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="4fdd2-116">DirectShow simplifica la reproducción multimedia, la conversión de formato y las tareas de captura.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="4fdd2-117">Al mismo tiempo, proporciona acceso a la arquitectura de control de flujo subyacente para las aplicaciones que requieren soluciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="4fdd2-118">También puede crear sus propios componentes de DirectShow para admitir nuevos formatos o efectos personalizados.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="4fdd2-119">Entre los ejemplos de los tipos de aplicación que puede escribir con DirectShow se incluyen reproductores de archivos, reproductores de TV y DVD, aplicaciones de edición de vídeo, convertidores de formato de archivo, aplicaciones de captura de audio y vídeo, codificadores y descodificadores, procesadores de señales digitales, etc.</span><span class="sxs-lookup"><span data-stu-id="4fdd2-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="4fdd2-120">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="4fdd2-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="4fdd2-121">Novedades de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fdd2-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="4fdd2-122">Formatos admitidos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fdd2-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="4fdd2-123">Preguntas más frecuentes sobre DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fdd2-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="4fdd2-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fdd2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fdd2-125">Introducción</span><span class="sxs-lookup"><span data-stu-id="4fdd2-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="4fdd2-126">Uso de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4fdd2-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



