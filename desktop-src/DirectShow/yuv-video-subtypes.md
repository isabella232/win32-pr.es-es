---
description: 'Los formatos YUV se clasifican según la siguiente información:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Subtipos de vídeo YUV (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31afa11c855b865c7e524d393d1f86ae836e00119a3171b35a3c0c2549d184b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632704"
---
# <a name="yuv-video-subtypes"></a>Subtipos de vídeo de YUV

Los formatos YUV se clasifican según la siguiente información:

**Formatos empaquetados frente a formatos planares.** En un formato empaquetado, los componentes Y, U y V se almacenan en una sola matriz. Los píxeles se organizan en grupos de macropixeles, cuyo diseño depende del formato. En un formato planar, los componentes Y, U y V se almacenan por separado, como tres planos.

**Muestreo de muestreo de muestreo.** Se usa una notación denominada notación A:B:C para describir la frecuencia con la que se muestrean usted y V en relación con Y:

-   4:4:4 significa que no hay ninguna disminución de los canales del canal.
-   4:2:2 significa una disminución horizontal de 2:1, sin un bajomuestreo vertical. Cada línea de examen contiene cuatro muestras Y por cada dos muestras de U o V.
-   4:2:0 significa una disminución horizontal de 2:1, con una disminución vertical de 2:1.
-   4:1:1 significa una disminución horizontal de 4:1, sin un bajomuestreo vertical. Cada línea de examen contiene cuatro muestras Y para cada muestra de U o V. El muestreo de 4:1:1 es menos común que otros formatos y no se describe en detalle en este artículo.

**Bits por canal.** Los tamaños de muestra más comunes son 8, 10 o 16 bits por muestra. Algunos formatos YUV están en desenlazados.

**Diseño de memoria.** Dos tipos de formato YUV pueden ser idénticos, pero usar ordenaciones diferentes para los ejemplos Y, V y U en la memoria.

**Formatos YUV recomendados**



| GUID               | Formato | muestreo | Empaquetado o plano | Bits por canal |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Embalado           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Embalado           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | Embalado           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Planar           | 8                |



 

Para obtener una descripción de estos formatos YUV para la representación de vídeo en Windows, vea [Recommended 8-Bit YUV Formats for Video Rendering](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md) .

**Otros tipos de formato YUV**



| GUID               | Formato                                                | muestreo                                                | Empaquetado o plano                                  | Bits por canal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | Ya no se admite.<br/> Indeo YVU9<br/> | Ya no se admite.<br/> Vea Notas.<br/> | Ya no se admite.<br/> Planar<br/> | Ya no se admite.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Vea Notas.                                            | Embalado                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Embalado                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Embalado                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | Vea Notas.                                            | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | Embalado                                            | 8                                            |



 

-   I420 consta de un plano Y, seguido de un plano U, seguido de un plano V.
-   IYUV es idéntico a I420.
-   Y211 es un formato empaquetado, en el que Y se muestrea cada 2 píxeles horizontalmente, y se muestrean usted y V cada 4 píxeles horizontalmente. Cada macropixel tiene 4 bytes y contiene 4 píxeles. Usa el siguiente orden de bytes:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P es un formato empaquetado de 4:1:1. Usa el siguiente orden de bytes:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 es un formato plano, en el que usted y V se muestrean cada 4 píxeles horizontal y verticalmente (a veces denominado 16:1:1). El plano V aparece delante del plano U.
-   El formato Indeo YVU9 (MEDIASUBTYPE IF09) es una variación de YVU9 con información adicional de fotograma delta después del \_ plano U. El códec Indeo ya no se admite en Windows.
-   YVYU es similar a UYVY con un orden de bytes diferente: `Y0 V0 Y1 U0`

-   El códec Indeo ya no se admite en Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Formatos YUV de 8 bits recomendados para la representación en vídeo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
