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
# <a name="creating-dxva-hd-video-surfaces"></a>Creación de superficies de vídeo de HD de DXVA

La aplicación debe crear una o varias superficies de Direct3D que se usarán para los fotogramas de entrada. Estos deben asignarse en el bloque de memoria especificado por el miembro **InputPool** de la estructura [**\_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Se pueden usar los siguientes tipos de superficie:

-   Una superficie de vídeo creada mediante una llamada a [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) y especificando el **tipo de superficie DXVAHD de \_ \_ \_ vídeo \_ entrada de vídeo** o tipo de superficie DXVAHD tipo de superficie **\_ \_ \_ \_ \_ privada** . Este tipo de superficie es equivalente a una superficie sin formato de pantalla.
-   Una superficie de representación de descodificador, creada mediante una llamada a [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) y especificando el tipo de superficie **DXVA2 \_ VideoDecoderRenderTarget** . Este tipo de superficie se usa para la descodificación de DXVA.
-   Superficie sin pantalla.

En el código siguiente se muestra cómo asignar una superficie de vídeo mediante [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


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

 

 



