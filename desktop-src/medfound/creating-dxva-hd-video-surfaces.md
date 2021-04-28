---
description: Creación de superficies de vídeo DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Creación de superficies de vídeo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102553"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="4d18d-103">Creación de superficies de vídeo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4d18d-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="4d18d-104">La aplicación debe crear una o varias superficies de Direct3D para usarlas para los fotogramas de entrada.</span><span class="sxs-lookup"><span data-stu-id="4d18d-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="4d18d-105">Deben asignarse en el grupo de memoria especificado por el **miembro InputPool** de la [**estructura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="4d18d-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="4d18d-106">Se pueden usar los siguientes tipos de superficie:</span><span class="sxs-lookup"><span data-stu-id="4d18d-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="4d18d-107">Superficie de vídeo creada mediante una llamada a [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) y especificando el tipo de superficie PRIVADA **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT** o **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE.**</span><span class="sxs-lookup"><span data-stu-id="4d18d-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="4d18d-108">Este tipo de superficie es equivalente a una superficie sin formato fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4d18d-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="4d18d-109">Superficie de destino de representación de descodificador, creada mediante una llamada a [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) y especificando el tipo de superficie **DXVA2 \_ VideoDecoderRenderTarget.**</span><span class="sxs-lookup"><span data-stu-id="4d18d-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="4d18d-110">Este tipo de superficie se usa para la decodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="4d18d-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="4d18d-111">Superficie sin formato fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4d18d-111">An off-screen plain surface.</span></span>

<span data-ttu-id="4d18d-112">El código siguiente muestra cómo asignar una superficie de vídeo mediante [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="4d18d-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a><span data-ttu-id="4d18d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d18d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d18d-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4d18d-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



