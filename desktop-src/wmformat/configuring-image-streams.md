---
title: Configuración de secuencias de imágenes
description: Configuración de secuencias de imágenes
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- flujos, configurar secuencias de imágenes
- códecs, configurar secuencias de imágenes
- flujos de imagen, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418629"
---
# <a name="configuring-image-streams"></a>Configuración de secuencias de imágenes

Los flujos de imagen contienen imágenes fijas en formato JPEG. Aunque las secuencias de imágenes son similares a las secuencias de vídeo en que toman imágenes sin comprimir como entradas, requieren una configuración ligeramente diferente. Para configurar un flujo de imagen, debe establecer los valores de los miembros de las estructuras de configuración de vídeo, tal como se muestra en la tabla siguiente.



| Configuración                                                           | Descripción                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipo de medio de WM \_ \_ . majortype**                                     | Establezca en \_ imagen WMMEDIATYPE.                                                                                                                                                       |
| **Tipo de medio de WM \_ \_ . SubType**                                       | Establézcalo en WMMEDIASUBTYPE \_ RGB24.                                                                                                                                                    |
| **Tipo de medio de WM \_ \_ . bFixedSizeSamples**                             | Establézcalo en **false**.                                                                                                                                                                |
| **Tipo de medio de WM \_ \_ . bTemporalCompression**                          | Establézcalo en **false**.                                                                                                                                                                |
| **Tipo de medio de WM \_ \_ . lSampleSize**                                   | Establecer en 0.                                                                                                                                                                        |
| **Tipo de medio de WM \_ \_ . FormatType**                                    | Establezca en WMFORMAT \_ videoinfo.                                                                                                                                                      |
| **Tipo de medio de WM \_ \_ . pUnk**                                          | Se establece en **null**.                                                                                                                                                                 |
| **Tipo de medio de WM \_ \_ . cbFormat**                                      | Establézcalo en `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **Tipo de medio de WM \_ \_ . pbFormat**                                      | Establezca en la dirección de una estructura **WMVIDEOINFOHEADER** configurada correctamente.                                                                                                     |
| **WMVIDEOINFOHEADER. rcSource** y **WMVIDEOINFOHEADER. rcTarget** | Establezca ambos rectángulos para que las esquinas superior izquierda sean coordenadas (0,0) y las esquinas inferiores derecha sean coordenadas (x, y) donde x es el ancho de la imagen e y es el alto de la imagen. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Se establece en la velocidad de bits de la secuencia.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Establecer en 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Establecer en 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biwidth**                                      | Se establece en el ancho de la imagen.                                                                                                                                                   |
| **BITMAPINFOHEADER. biheight**                                     | Se establece en el alto de la imagen.                                                                                                                                                  |
| **BITMAPINFOHEADER. biplanes**                                     | establézcalo en 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biBitCount**                                   | Establezca en 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER. bicompression**                                | Establézcalo en BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER. biSizeImage**                                  | Se establece en (((x \* y \* c)/8), donde x es el ancho de la imagen, y es el alto de la imagen y c es la profundidad de color de la imagen (en este caso, siempre es 24).                     |
| **BITMAPINFOHEADER. biXPelsPerMeter**                              | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biYPelsPerMeter**                              | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biClrUsed**                                    | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biClrImportant**                               | Establecer en 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Obtener buenos resultados con el códec de pantalla de Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Flujos de imagen**](image-streams.md)
</dt> </dl>

 

 




