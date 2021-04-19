---
description: Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido premium con una robustez mejorada, una calidad sin parangón y una interoperabilidad perfecta.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Acerca de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707525"
---
# <a name="about-media-foundation"></a><span data-ttu-id="926ac-103">Acerca de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="926ac-103">About Media Foundation</span></span>

<span data-ttu-id="926ac-104">Microsoft Media Foundation es la plataforma multimedia de próxima generación para Windows que permite a los desarrolladores, consumidores y proveedores de contenido adoptar la nueva ola de contenido premium con una robustez mejorada, una calidad sin parangón y una interoperabilidad perfecta.</span><span class="sxs-lookup"><span data-stu-id="926ac-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="926ac-105">Media Foundation requiere Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="926ac-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="926ac-106">Utiliza el modelo de objetos componentes (COM) y requiere C/C++.</span><span class="sxs-lookup"><span data-stu-id="926ac-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="926ac-107">Microsoft no proporciona una API administrada para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="926ac-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="926ac-108">Las API de Media Foundation forman parte de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="926ac-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="926ac-109">Para desarrollar una aplicación Media Foundation, instale la versión más reciente de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="926ac-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="926ac-110">Calidad de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="926ac-110">Audio and Video Quality</span></span>

<span data-ttu-id="926ac-111">Media Foundation se ha diseñado para satisfacer los desafíos planteados por el contenido de alta definición.</span><span class="sxs-lookup"><span data-stu-id="926ac-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="926ac-112">Las mejoras de calidad de audio y vídeo realizadas en toda la plataforma ahora permiten ofrecer una gran experiencia para el contenido de alta definición de próxima generación.</span><span class="sxs-lookup"><span data-stu-id="926ac-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="926ac-113">DirectX video Acceleration (DXVA) 2,0 ofrece una aceleración de vídeo más eficaz, en comparación con DXVA 1,0, con descodificación de vídeo más sólida y simplificada y uso extendido de hardware en el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="926ac-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="926ac-114">Con DXVA 2,0, Windows puede controlar algunos de los contenidos más exigentes de alta definición con alta calidad y resistencia ante problemas mejorados.</span><span class="sxs-lookup"><span data-stu-id="926ac-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="926ac-115">La información del espacio de colores se conserva a lo largo de la canalización de vídeo.</span><span class="sxs-lookup"><span data-stu-id="926ac-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="926ac-116">Los usuarios pueden disfrutar de contenido de vídeo con plena fidelidad.</span><span class="sxs-lookup"><span data-stu-id="926ac-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="926ac-117">La información de color y las imágenes entrelazadas se pasan ahora al hardware para las composiciones de un solo paso.</span><span class="sxs-lookup"><span data-stu-id="926ac-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="926ac-118">Conservar la información del espacio de colores también reduce las conversiones de espacio de color innecesarias, lo que libera más ciclos para procesar contenido HD exigente.</span><span class="sxs-lookup"><span data-stu-id="926ac-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="926ac-119">El representador de vídeo mejorado (EVR) ofrece una mejor compatibilidad con el control de tiempo, el procesamiento de vídeo mejorado y la resistencia de problemas mejorada.</span><span class="sxs-lookup"><span data-stu-id="926ac-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="926ac-120">Se ha mejorado la compatibilidad con la reproducción de pantalla completa y se ha minimizado el desgaste de vídeo en el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="926ac-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="926ac-121">Media Foundation usa el servicio Programador de clases multimedia (MMCSS), un nuevo servicio de sistema en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="926ac-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="926ac-122">MMCSS permite a las aplicaciones multimedia asegurarse de que su procesamiento dependiente del tiempo recibe el acceso prioritario a los recursos de la CPU.</span><span class="sxs-lookup"><span data-stu-id="926ac-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="926ac-123">Acceso al contenido</span><span class="sxs-lookup"><span data-stu-id="926ac-123">Content Access</span></span>

<span data-ttu-id="926ac-124">A medida que el entretenimiento digital se traslada a la era de alta definición y el contenido es más portátil y omnipresente, la protección de contenido se convierte en una parte integral de los productos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="926ac-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="926ac-125">La extensibilidad de Media Foundation garantiza que puede admitir estas tendencias.</span><span class="sxs-lookup"><span data-stu-id="926ac-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="926ac-126">Además, la extensibilidad de Media Foundation permite que distintos sistemas de protección de contenido funcionen juntos.</span><span class="sxs-lookup"><span data-stu-id="926ac-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="926ac-127">Acerca de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="926ac-127">About Media Foundation</span></span>

<span data-ttu-id="926ac-128">Esta sección contiene información general sobre las API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="926ac-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="926ac-129">Puede encontrar información de programación detallada en la [Guía de programación de Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="926ac-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="926ac-130">Sección</span><span class="sxs-lookup"><span data-stu-id="926ac-130">Section</span></span>                                                                              | <span data-ttu-id="926ac-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="926ac-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="926ac-132">Novedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="926ac-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="926ac-133">Describe las nuevas características de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="926ac-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="926ac-134">Media Foundation encabezados y bibliotecas</span><span class="sxs-lookup"><span data-stu-id="926ac-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="926ac-135">Enumera los archivos de encabezado y de biblioteca que definen las API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="926ac-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="926ac-136">Herramientas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="926ac-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="926ac-137">Describe las herramientas de desarrollo que están disponibles para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="926ac-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="926ac-138">Media Foundation no se incluye con las ediciones N y KN de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="926ac-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="926ac-139">Para obtener más información, consulte [Microsoft Windows Media Feature Pack para las versiones N y kN de todas las ediciones de Windows 8](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="926ac-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="926ac-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="926ac-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="926ac-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="926ac-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



