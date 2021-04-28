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
# <a name="creating-dxva-hd-video-surfaces"></a>Creación de superficies de vídeo DXVA-HD

La aplicación debe crear una o varias superficies de Direct3D para usarlas para los fotogramas de entrada. Deben asignarse en el grupo de memoria especificado por el **miembro InputPool** de la [**estructura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Se pueden usar los siguientes tipos de superficie:

-   Superficie de vídeo creada mediante una llamada a [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) y especificando el tipo de superficie PRIVADA **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT** o **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE.** Este tipo de superficie es equivalente a una superficie sin formato fuera de la pantalla.
-   Superficie de destino de representación de descodificador, creada mediante una llamada a [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) y especificando el tipo de superficie **DXVA2 \_ VideoDecoderRenderTarget.** Este tipo de superficie se usa para la decodificación de DXVA.
-   Superficie sin formato fuera de la pantalla.

El código siguiente muestra cómo asignar una superficie de vídeo mediante [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



