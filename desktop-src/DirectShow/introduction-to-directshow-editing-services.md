---
description: Introducción a los servicios de edición de DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introducción a los servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494963"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="4e38b-103">Introducción a los servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4e38b-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="4e38b-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4e38b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4e38b-105">El núcleo de DirectShow es una arquitectura eficaz para administrar los medios de streaming.</span><span class="sxs-lookup"><span data-stu-id="4e38b-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="4e38b-106">Una aplicación puede utilizarla para reproducir contenido multimedia creado en una amplia variedad de formatos, sin que el desarrollador tenga que preocuparse por la compresión de archivos y otros detalles tediosos.</span><span class="sxs-lookup"><span data-stu-id="4e38b-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="4e38b-107">Sin embargo, antes de los [servicios de edición de DirectShow](directshow-editing-services.md) (des), DirectShow carecía de la flexibilidad necesaria para la edición no lineal.</span><span class="sxs-lookup"><span data-stu-id="4e38b-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="4e38b-108">Por ejemplo, supongamos que desea crear una secuencia de vídeo compuesta por 4 segundos desde el origen A, seguido de 10 segundos del origen B y de que termina con 5 segundos a partir del código fuente C. Podría hacerlo con bastante facilidad con solo la API de DirectShow básica.</span><span class="sxs-lookup"><span data-stu-id="4e38b-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="4e38b-109">Pero, ¿qué ocurre si decidió que el origen C debe aparecer antes que el origen B, no después de; que la secuencia debe usar 8 segundos del origen A, no 4; y que todo el entorno de producción necesitaba una pista de audio independiente jugando en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4e38b-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="4e38b-110">Incluso los cambios menores como estos podrían ser difíciles de implementar.</span><span class="sxs-lookup"><span data-stu-id="4e38b-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="4e38b-111">Pero el escenario que se acaba de describir es un proyecto de edición trivial en DES: puede hacerlo con una serie de llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="4e38b-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="4e38b-112">Estas son algunas de las características que DES aporta a DirectShow:</span><span class="sxs-lookup"><span data-stu-id="4e38b-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="4e38b-113">Modelo de escala de tiempo que organiza las pistas de audio y vídeo en capas anidadas, lo que facilita la manipulación de la producción final.</span><span class="sxs-lookup"><span data-stu-id="4e38b-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="4e38b-114">La capacidad de obtener una vista previa de un proyecto de vídeo sobre la marcha</span><span class="sxs-lookup"><span data-stu-id="4e38b-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="4e38b-115">Persistencia del proyecto a través de un formato basado en XML</span><span class="sxs-lookup"><span data-stu-id="4e38b-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="4e38b-116">Compatibilidad con efectos de audio y vídeo, así como transiciones entre pistas de vídeo (como transiciones y barridos)</span><span class="sxs-lookup"><span data-stu-id="4e38b-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="4e38b-117">Más de 100 barridos estándar, tal y como se define en la sociedad de los ingenieros de películas y TV (SMPTE)</span><span class="sxs-lookup"><span data-stu-id="4e38b-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="4e38b-118">Incrustación basada en matiz, luminancia, valor RGB o valor alfa</span><span class="sxs-lookup"><span data-stu-id="4e38b-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="4e38b-119">Conversión automática de velocidades de fotogramas y tasas de muestreo de audio, lo que permite a una producción usar orígenes heterogéneos</span><span class="sxs-lookup"><span data-stu-id="4e38b-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="4e38b-120">Cambiar el tamaño o recortar el vídeo</span><span class="sxs-lookup"><span data-stu-id="4e38b-120">Resizing or cropping of video</span></span>

<span data-ttu-id="4e38b-121">Limitaciones:</span><span class="sxs-lookup"><span data-stu-id="4e38b-121">Limitations:</span></span>

-   <span data-ttu-id="4e38b-122">DES no es compatible con orígenes de vídeo MPEG-2 o H. 264.</span><span class="sxs-lookup"><span data-stu-id="4e38b-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e38b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e38b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e38b-124">Servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4e38b-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



