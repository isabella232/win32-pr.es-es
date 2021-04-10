---
description: Aceleración de vídeo de DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Aceleración de vídeo de DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275119"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="7ef33-103">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="7ef33-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="7ef33-104">DirectX video Acceleration (DXVA) es una API y una DDI correspondiente para usar la aceleración de hardware para acelerar el procesamiento de códecs de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7ef33-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="7ef33-105">Los códecs de software y los procesadores de vídeo de software pueden usar DXVA para descargar ciertas operaciones de uso intensivo de la CPU en la GPU.</span><span class="sxs-lookup"><span data-stu-id="7ef33-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="7ef33-106">Por ejemplo, un descodificador de software puede descargar la transformación de coseno discreto inverso (iDCT) en la GPU.</span><span class="sxs-lookup"><span data-stu-id="7ef33-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="7ef33-107">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7ef33-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7ef33-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7ef33-108">In this section</span></span>



| <span data-ttu-id="7ef33-109">Tema</span><span class="sxs-lookup"><span data-stu-id="7ef33-109">Topic</span></span>                                                                                             | <span data-ttu-id="7ef33-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ef33-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ef33-111">Acerca de DXVA 2,0</span><span class="sxs-lookup"><span data-stu-id="7ef33-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="7ef33-112">Información general de DXVA 2 y su relación con DXVA 1.</span><span class="sxs-lookup"><span data-stu-id="7ef33-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="7ef33-113">Administrador de dispositivos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7ef33-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="7ef33-114">El administrador de dispositivos de Microsoft Direct3D habilita dos o más objetos para compartir el mismo dispositivo de Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7ef33-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="7ef33-115">Compatibilidad con DXVA 2,0 en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7ef33-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="7ef33-116">En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en un filtro de descodificador de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7ef33-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="7ef33-117">Compatibilidad con DXVA 2,0 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ef33-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="7ef33-118">En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en una transformación de Media Foundation (MFT) con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7ef33-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="7ef33-119">Procesamiento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="7ef33-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="7ef33-120">El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="7ef33-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="7ef33-121">Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7ef33-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="7ef33-122">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="7ef33-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="7ef33-123">Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="7ef33-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="7ef33-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ef33-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef33-125">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ef33-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7ef33-126">Especificación de DXVA 1</span><span class="sxs-lookup"><span data-stu-id="7ef33-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
