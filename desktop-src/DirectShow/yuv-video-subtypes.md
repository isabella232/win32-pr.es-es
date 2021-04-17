---
description: 'Los formatos YUV se clasifican según la información siguiente:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Subtipos de vídeo YUV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312a3d9d8e12953353ed0f61fff67a05bf87426b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691021"
---
# <a name="yuv-video-subtypes"></a>Subtipos de vídeo YUV

Los formatos YUV se clasifican según la información siguiente:

**Formatos empaquetados frente a formatos planos.** En un formato empaquetado, los componentes Y, U y V se almacenan en una sola matriz. Los píxeles se organizan en grupos de macropixels, cuyo diseño depende del formato. En un formato plano, los componentes Y, U y V se almacenan por separado, como tres planos.

**Muestreo de croma.** Una notación denominada la notación A:B: C se usa para describir la frecuencia con la que se muestrean y las V en relación con Y:

-   4:4:4 significa que no hay una disminución de la resolución de los canales de croma.
-   4:2:2 significa una disminución de la resolución horizontal de 2:1, sin disminución de la resolución vertical. Cada línea de exploración contiene cuatro ejemplos Y por cada uno de los dos ejemplos U o V.
-   4:2:0 significa disminución de la reducción horizontal de 2:1, con una disminución de resolución de 2:1.
-   4:1:1 significa una disminución de la resolución horizontal de 4:1, sin disminución de la resolución vertical. Cada línea de exploración contiene cuatro ejemplos Y para cada muestra de U o V. el muestreo 4:1:1 es menos común que otros formatos y no se describe en detalle en este artículo.

**Bits por canal.** Los tamaños de ejemplo más comunes son 8, 10 o 16 bits por muestra. Algunos formatos YUV se encuentran en la paleta.

**Diseño de memoria.** Dos tipos de formato YUV pueden ser idénticos, pero usan pedidos diferentes para los ejemplos de Y, V y U en la memoria.

**Formatos YUV recomendados**



| GUID               | Formato | muestreo | Empaquetado o plano | Bits por canal |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Equipado           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Equipado           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | Equipado           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Trayectoria           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Trayectoria           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | Trayectoria           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Trayectoria           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Trayectoria           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Trayectoria           | 8                |



 

Para obtener una descripción de los formatos YUV para la representación de vídeo en Windows, consulte [formatos YUV de 8 bits recomendados para la representación de vídeo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md) .

**Otros tipos de formato YUV**



| GUID               | Formato                                                | muestreo                                                | Empaquetado o plano                                  | Bits por canal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ i420 | I420                                                  | 4:2:0                                                   | Trayectoria                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | Ya no se admite.<br/> YVU9 de Indeo<br/> | Ya no se admite.<br/> Vea Notas.<br/> | Ya no se admite.<br/> Trayectoria<br/> | Ya no se admite.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Trayectoria                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Vea Notas.                                            | Equipado                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Equipado                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Equipado                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | Vea Notas.                                            | Trayectoria                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | Equipado                                            | 8                                            |



 

-   I420 consta de un plano Y, seguido de un plano U seguido de un plano V.
-   IYUV es idéntico a i420.
-   Y211 es un formato empaquetado, en el que y se muestrea cada 2 píxeles horizontalmente y se muestrea cada 4 píxeles horizontalmente. Cada macropixel es 4 bytes y contiene 4 píxeles. Usa el orden de bytes siguiente:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P es un formato empaquetado de 4:1:1. Usa el orden de bytes siguiente:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 es un formato plano, en el que se muestrea cada 4 píxeles horizontal y verticalmente (a veces denominado 16:1:1). El plano V aparece delante del plano U.
-   El formato Indeo YVU9 (MEDIASUBTYPE \_ IF09) es una variación de YVU9 con información adicional sobre el fotograma Delta después del plano U. El códec Indeo ya no se admite en Windows.
-   YVYU es similar a UYVY con un orden de bytes diferente: `Y0 V0 Y1 U0`

-   El códec Indeo ya no se admite en Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Formatos YUV de 8 bits recomendados para la representación de vídeo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
