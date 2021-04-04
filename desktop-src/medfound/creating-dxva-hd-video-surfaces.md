---
description: .
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Creación de superficies de vídeo de HD de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459504a312ec0d59cf3642f528f433ffce8ba094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907575"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="ef3fd-103">Creación de superficies de vídeo de HD de DXVA</span><span class="sxs-lookup"><span data-stu-id="ef3fd-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="ef3fd-104">La aplicación debe crear una o varias superficies de Direct3D que se usarán para los fotogramas de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="ef3fd-105">Estos deben asignarse en el bloque de memoria especificado por el miembro **InputPool** de la estructura [**\_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="ef3fd-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="ef3fd-106">Se pueden usar los siguientes tipos de superficie:</span><span class="sxs-lookup"><span data-stu-id="ef3fd-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="ef3fd-107">Una superficie de vídeo creada mediante una llamada a [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) y especificando el **tipo de superficie DXVAHD de \_ \_ \_ vídeo \_ entrada de vídeo** o tipo de superficie DXVAHD tipo de superficie **\_ \_ \_ \_ \_ privada** .</span><span class="sxs-lookup"><span data-stu-id="ef3fd-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="ef3fd-108">Este tipo de superficie es equivalente a una superficie sin formato de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="ef3fd-109">Una superficie de representación de descodificador, creada mediante una llamada a [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) y especificando el tipo de superficie **DXVA2 \_ VideoDecoderRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="ef3fd-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="ef3fd-110">Este tipo de superficie se usa para la descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="ef3fd-111">Superficie sin pantalla.</span><span class="sxs-lookup"><span data-stu-id="ef3fd-111">An off-screen plain surface.</span></span>

<span data-ttu-id="ef3fd-112">En el código siguiente se muestra cómo asignar una superficie de vídeo mediante [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="ef3fd-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ef3fd-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef3fd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef3fd-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ef3fd-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



