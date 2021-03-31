---
description: Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808090"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware. DXVA-HD usa la GPU para realizar funciones como desentrelazado, composición y conversión de espacio de color.

DXVA-HD es similar al [procesamiento de vídeo de DXVA](dxva-video-processing.md) (DXVA-VP), pero ofrece características mejoradas y un modelo de procesamiento más sencillo. Al proporcionar un modelo de composición más flexible, DXVA-HD está diseñado para admitir la próxima generación de formatos ópticos HD y estándares de difusión.

La API DXVA-HD requiere un controlador de pantalla WDDM que admita la interfaz de controlador de dispositivo (DDI) de DXVA, o bien un procesador de software de complemento.

-   [Mejoras en DXVA-VP](#improvements-over-dxva-vp)
-   [Temas relacionados](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Mejoras en DXVA-VP

DXVA-HD expande el conjunto de características que proporciona DXVA-VP. Entre las mejoras se incluyen:

-   Combinación de RGB y YUV. Cualquier flujo puede ser RGB o YUV. Ya no hay una distinción entre el flujo principal y los subflujos.
-   Desentrelazado de varias secuencias. Cualquier flujo puede ser progresiva o entrelazado. Además, la cadencia y la velocidad de fotogramas pueden variar de un flujo de entrada a otro.
-   Colores de fondo RGB. Anteriormente, solo se admitían los colores de fondo YUV.
-   Creación de claves de luminancia. Cuando está habilitada la creación de claves de luminancia, los valores de luminancia que se encuentran dentro de un intervalo designado se vuelven transparentes.
-   Cambio dinámico entre los modos de desentrelazado.

DXVA: HD también define algunas características avanzadas que los controladores pueden admitir. Sin embargo, las aplicaciones no deben suponer que todos los controladores serán compatibles con estas características. Las características avanzadas incluyen:

-   Telecine inversa (por ejemplo, 60i a 24p).
-   Conversión de velocidad de fotogramas (por ejemplo, 24p a 120P).
-   Modos de relleno alfa.
-   Filtro de reducción de ruido y mejora del borde.
-   Escala no lineal anamorphic.
-   YCbCr extendido (xvYCC).

Esta sección contiene los temas siguientes.

-   [Creación de un procesador de vídeo DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Comprobando formatos de DXVA compatibles: HD](checking-supported-dxva-hd-formats.md)
-   [Creación de superficies de vídeo de HD de DXVA](creating-dxva-hd-video-surfaces.md)
-   [Configuración de los Estados de la HD de DXVA](setting-dxva-hd-states.md)
-   [Realización de DXVA: HD blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA: ejemplo HD](dxva-hd-sample.md)
</dt> </dl>

 

 



