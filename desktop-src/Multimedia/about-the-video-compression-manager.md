---
title: Acerca del administrador de compresión de vídeo
description: Acerca del administrador de compresión de vídeo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows multimedia, administrador de compresión de vídeo (VCM)
- multimedia, administrador de compresión de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487635"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="684ed-105">Acerca del administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="684ed-105">About the Video Compression Manager</span></span>

<span data-ttu-id="684ed-106">Normalmente, los compresores instalables operan con datos de imagen de vídeo almacenados en archivos de audio y vídeo intercalado (AVI).</span><span class="sxs-lookup"><span data-stu-id="684ed-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="684ed-107">En esta información general se explican las técnicas de programación que se usan para tener acceso a los compresores instalables a través de VCM y se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="684ed-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="684ed-108">VCM y el vídeo para la arquitectura de Windows</span><span class="sxs-lookup"><span data-stu-id="684ed-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="684ed-109">Comprimir y descomprimir los datos de imagen de la aplicación</span><span class="sxs-lookup"><span data-stu-id="684ed-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="684ed-110">Usar representadores VCM para dibujar datos desde la aplicación</span><span class="sxs-lookup"><span data-stu-id="684ed-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="684ed-111">Funciones y estructuras de VCM</span><span class="sxs-lookup"><span data-stu-id="684ed-111">VCM functions and structures</span></span>

<span data-ttu-id="684ed-112">Antes de leer esta información general, debe estar familiarizado con los servicios gráficos de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="684ed-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="684ed-113">En concreto, el uso de los mapas de bits y las estructuras relacionadas con los mapas de bits, como [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) y [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), se usan en gran medida en VCM.</span><span class="sxs-lookup"><span data-stu-id="684ed-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="684ed-114">Para obtener información adicional sobre las estructuras **bitmapinfo (** y **BITMAPINFOHEADER** , vea [mapas de bits](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="684ed-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="684ed-115">El administrador de compresión de audio (ACM) proporciona compatibilidad de nivel de sistema para los controladores de compresión y descompresión de audio.</span><span class="sxs-lookup"><span data-stu-id="684ed-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="684ed-116">Para obtener una descripción de los servicios de compresión de audio, consulte [Administrador de compresión de audio](audio-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="684ed-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="684ed-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="684ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="684ed-118">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="684ed-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 