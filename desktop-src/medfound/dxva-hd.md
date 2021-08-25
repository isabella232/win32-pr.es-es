---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40e23d6e91f576f062c52a0f58d0bfe1f769ad3879581b01386333266cb0553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958655"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware. DXVA-HD usa la GPU para realizar funciones como el desenlazado, la composición y la conversión de espacio de color.

DXVA-HD es similar al procesamiento de vídeo [DXVA](dxva-video-processing.md) (DXVA-VP), pero ofrece características mejoradas y un modelo de procesamiento más sencillo. Al proporcionar un modelo de composición más flexible, DXVA-HD está diseñado para admitir la próxima generación de formatos ópticos de HD y estándares de difusión.

La API DXVA-HD requiere un controlador de pantalla WDDM que admita la interfaz de controlador de dispositivo DXVA-HD (DDI) o un procesador de software de complemento.

-   [Mejoras en DXVA-VP](#improvements-over-dxva-vp)
-   [Temas relacionados](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Mejoras en DXVA-VP

DXVA-HD expande el conjunto de características proporcionadas por DXVA-VP. Entre las mejoras se incluyen:

-   Mezcla RGB y YUV. Cualquier secuencia puede ser RGB o YUV. Ya no hay ninguna distinción entre la secuencia principal y las substreams.
-   Desenlazado de varias secuencias. Cualquier secuencia puede ser progresiva o entrelazada. Además, la cadencia y la velocidad de fotogramas pueden variar de un flujo de entrada a otro.
-   Colores de fondo RGB. Anteriormente, solo se admiteban los colores de fondo YUV.
-   Clave de Luma. Cuando se habilita la clave de luma, los valores luma que se encuentran dentro de un intervalo designado se vuelven transparentes.
-   Cambio dinámico entre modos de desinterés.

DXVA-HD también define algunas características avanzadas que los controladores pueden admitir. Sin embargo, las aplicaciones no deben suponer que todos los controladores admitirán estas características. Las características avanzadas incluyen:

-   Televisa inversa (por ejemplo, de 60i a 24p).
-   Conversión de velocidad de fotogramas (por ejemplo, de 24p a 120p).
-   Modos de relleno alfa.
-   Reducción de ruido y filtrado de mejora del borde.
-   Escalado anamórfico no lineal.
-   YCbCr extendido (sipYCC).

Esta sección contiene los temas siguientes.

-   [Creación de un procesador de vídeo DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Comprobación de los formatos DXVA-HD admitidos](checking-supported-dxva-hd-formats.md)
-   [Creación de superficies de vídeo DXVA-HD](creating-dxva-hd-video-surfaces.md)
-   [Configuración de estados DXVA-HD](setting-dxva-hd-states.md)
-   [Realización de dxva-HD Blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Ejemplo de DXVA-HD](dxva-hd-sample.md)
</dt> </dl>

 

 



