---
title: Configuración de imágenes Secuencias
description: Configuración de imágenes Secuencias
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- streams,configuring image streams
- codecs,configuring image streams
- secuencias de imágenes, configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ce58fe3da709772b08d0956f3f5540713f7960742338f73c9d9807ad1a1e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848970"
---
# <a name="configuring-image-streams"></a>Configuración de imágenes Secuencias

Los flujos de imágenes contienen imágenes fijas en formato JPEG. Aunque las secuencias de imágenes son como secuencias de vídeo en las que toman imágenes sin comprimir como entradas, requieren una configuración ligeramente diferente. Para configurar un flujo de imágenes, debe establecer los valores de los miembros de las estructuras de configuración de vídeo, como se muestra en la tabla siguiente.



| Configuración                                                           | Descripción                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                                     | Se establece en Imagen \_ WMMEDIATYPE.                                                                                                                                                       |
| **WM \_ MEDIA \_ TYPE.subtype**                                       | Establezca en WMMEDIASUBTYPE \_ RGB24.                                                                                                                                                    |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**                             | Se establece en **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.bMentalCompression**                          | Se establece en **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                                   | Establecer en 0.                                                                                                                                                                        |
| **WM \_ MEDIA \_ TYPE.formattype**                                    | Establezca en WMFORMAT \_ VideoInfo.                                                                                                                                                      |
| **WM \_ MEDIA \_ TYPE.pUnk**                                          | Se establece en **NULL.**                                                                                                                                                                 |
| **WM \_ MEDIA \_ TYPE.cbFormat**                                      | Establézcalo en `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **WM \_ MEDIA \_ TYPE.pbFormat**                                      | Establezca en la dirección de una estructura **WMVIDEOINFOHEADER** configurada correctamente.                                                                                                     |
| **WMVIDEOINFOHEADER.rcSource** y **WMVIDEOINFOHEADER.rcTarget** | Establezca ambos rectángulos para que las esquinas superiores izquierdas sean coordenadas (0, 0) y las esquinas inferiores derechas sean coordenadas (x, y), donde x es el ancho de la imagen e y es el alto de la imagen. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Establezca en la velocidad de bits de la secuencia.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Establecer en 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Establecer en 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biWidth**                                      | Establezca en el ancho de la imagen.                                                                                                                                                   |
| **BITMAPINFOHEADER.biHeight**                                     | Establezca en el alto de la imagen.                                                                                                                                                  |
| **BITMAPINFOHEADER.biPlanes**                                     | establézcalo en 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | Establezca en 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER.biCompression**                                | Establezca en BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Establezca en ((x y c) / 8), donde x es el ancho de la imagen, y es el alto de la imagen y c es la profundidad de color de la imagen (en este caso siempre \* \* 24).                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Establecer en 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | Establecer en 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todos los Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Obtención de buenos resultados con el códec de pantalla Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Imagen Secuencias**](image-streams.md)
</dt> </dl>

 

 




