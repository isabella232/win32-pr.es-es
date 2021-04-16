---
description: Características de VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Características de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677199"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="ab32c-103">Características de VMR</span><span class="sxs-lookup"><span data-stu-id="ab32c-103">Features of the VMR</span></span>

<span data-ttu-id="ab32c-104">El representador de mezcla de vídeo 7 (VMR-7) admite las siguientes características nuevas:</span><span class="sxs-lookup"><span data-stu-id="ab32c-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="ab32c-105">Combinación real de varias secuencias de vídeo con las capacidades de combinación alfa de los dispositivos de hardware de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ab32c-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="ab32c-106">La capacidad de conectar su propio componente de composición para implementar efectos y transiciones entre varias secuencias de vídeo que entran en la VMR.</span><span class="sxs-lookup"><span data-stu-id="ab32c-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="ab32c-107">Representación sin ventana verdadera.</span><span class="sxs-lookup"><span data-stu-id="ab32c-107">True windowless rendering.</span></span> <span data-ttu-id="ab32c-108">Ya no es necesario que la ventana de reproducción de vídeo sea un elemento secundario de la ventana de la aplicación para que contenga reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ab32c-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="ab32c-109">El nuevo modo de representación sin ventanas de VMR permite a las aplicaciones hospedar fácilmente la reproducción de vídeo en cualquier ventana sin tener que reenviar los mensajes de ventana al representador para el procesamiento específico del representador.</span><span class="sxs-lookup"><span data-stu-id="ab32c-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="ab32c-110">Un nuevo modo de reproducción no representativo en el que las aplicaciones pueden proporcionar su propio componente de asignador para obtener acceso a la imagen de vídeo descodificada antes de que se muestre en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ab32c-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="ab32c-111">Compatibilidad mejorada para equipos equipados con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="ab32c-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="ab32c-112">Compatibilidad con la nueva arquitectura de aceleración de vídeo de DirectX de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ab32c-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="ab32c-113">Compatibilidad con la reproducción de vídeo de alta calidad simultáneamente en varias ventanas.</span><span class="sxs-lookup"><span data-stu-id="ab32c-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="ab32c-114">Compatibilidad con el modo exclusivo de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="ab32c-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="ab32c-115">100% de compatibilidad con versiones anteriores con aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="ab32c-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="ab32c-116">Compatibilidad con la ejecución de fotogramas y una manera confiable de capturar la imagen actual que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ab32c-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="ab32c-117">La capacidad de las aplicaciones de alphamente mezclar sus propios datos de imagen estáticos (por ejemplo, logotipos de canal o componentes de interfaz de usuario) con el vídeo sin complicaciones.</span><span class="sxs-lookup"><span data-stu-id="ab32c-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="ab32c-118">VMR-9 es compatible con todas las características enumeradas anteriormente, además de:</span><span class="sxs-lookup"><span data-stu-id="ab32c-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="ab32c-119">La capacidad de procesar datos de vídeo directamente con las API de Direct3D, como los sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab32c-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="ab32c-120">Compatibilidad mejorada para el contenido de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="ab32c-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="ab32c-121">Compatibilidad con cualquier plataforma compatible con DirectX.</span><span class="sxs-lookup"><span data-stu-id="ab32c-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab32c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab32c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab32c-123">Acerca de la presentación de la combinación de vídeo</span><span class="sxs-lookup"><span data-stu-id="ab32c-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



