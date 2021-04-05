---
description: Componentes del filtro VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componentes del filtro VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546038"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="c2bb7-103">Componentes del filtro VMR</span><span class="sxs-lookup"><span data-stu-id="c2bb7-103">VMR Filter Components</span></span>

<span data-ttu-id="c2bb7-104">La VMR emplea un diseño modular que permite a las aplicaciones configurarlo para muchos escenarios de representación diferentes.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="c2bb7-105">En función de su configuración, la VMR contiene de dos a cinco subcomponentes (además de sus clavijas de entrada).</span><span class="sxs-lookup"><span data-stu-id="c2bb7-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR en modo de ventana con varias secuencias](images/vmr-multiple-streams.png)

<span data-ttu-id="c2bb7-107">**Mezclador:** El mezclador es un objeto COM responsable de la combinación de varias secuencias.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="c2bb7-108">El desentrelazado también se produce dentro del mezclador.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="c2bb7-109">VMR carga el mezclador cuando se detectan varios flujos de entrada o cuando el vídeo de entrada está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="c2bb7-110">El mezclador recopila información sobre cada flujo de entrada y ordena los flujos en el orden Z correcto.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="c2bb7-111">Es responsable de determinar cuándo cada pin de entrada recibe un ejemplo y para indicar al compositor de la imagen en el momento adecuado que realice la mezcla real.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="c2bb7-112">El mezclador también calcula la marca de tiempo que se va a aplicar a cada imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="c2bb7-113">Cuando la aplicación está proporcionando un mapa de bits que se va a mostrar en la parte superior de la imagen compuesta, el mezclador es responsable de garantizar que el mapa de bits se muestre en la parte superior aunque se modifique el orden Z de los flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="c2bb7-114">**Compositor de imágenes:** El compositor de imágenes es un objeto COM que realiza la combinación real de los flujos de entrada en una única superficie DirectDraw o Direct3D proporcionada por el asignador-presentador.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="c2bb7-115">VMR proporciona un compositor de imágenes predeterminado que permite a las aplicaciones realizar efectos de mezcla alfa 2D.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="c2bb7-116">Las aplicaciones pueden proporcionar un compositor de imágenes personalizado para habilitar otros efectos 2D y 3D, como la aplicación de texturas a partes de la imagen, la combinación alfa por píxel, la asignación de la imagen a objetos 3D fijos o móviles, etc.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="c2bb7-117">**Allocator-Presenter:** Allocator-Presenter es un objeto COM que asigna el objeto DirectDraw o Direct3D y controla la comunicación con la tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="c2bb7-118">El dibujo puede realizarse como volteo o como blit.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="c2bb7-119">Puede conectar su propio asignador-presentador para crear y controlar el objeto DirectDraw o Direct3D, y/o para obtener acceso a los bits de vídeo en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="c2bb7-120">**Administrador de ventanas:** El administrador de ventanas solo se usa en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="c2bb7-121">El administrador de ventanas admite las interfaces heredadas [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c2bb7-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2bb7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2bb7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2bb7-123">Acerca de la presentación de la combinación de vídeo</span><span class="sxs-lookup"><span data-stu-id="c2bb7-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



