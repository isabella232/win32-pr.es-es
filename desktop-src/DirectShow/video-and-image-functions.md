---
description: Funciones de vídeo e imagen
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funciones de vídeo e imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432125"
---
# <a name="video-and-image-functions"></a>Funciones de vídeo e imagen

Estas funciones y macros manipulan las DirectShow de formato de vídeo.



| Función                                                             | Descripción                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COINCIDENCIA \_ DE MÁSCARAS \_ DE BITS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Compara las máscaras de color de dos [**estructuras VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                       |
| [**MÁSCARAS DE BITS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera las máscaras de color de una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Comprueba un tipo de medio que contiene una estructura de [**formato VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en busca de errores que puedan provocar saturaciones de búfer o desbordamientos de enteros.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Comprueba un tipo de medio que contiene una estructura de [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) en busca de errores que puedan provocar saturaciones del búfer o desbordamientos de enteros. |
| [**Colores**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera las entradas de la paleta de una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina si una estructura [**VIDEOINFOHEADER especificada**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contiene una paleta.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Convierte un tipo de medio que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en uno que [**usa VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcula el tamaño necesario para una estructura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que puede contener una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Devuelve la primera entrada de la paleta en una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Devuelve el GUID del subtipo **multimedia** para el mapa de bits especificado.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera el nombre legible de un subtipo de vídeo.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Devuelve el GUID del subtipo **multimedia para** un mapa de bits RGB sin comprimir de 16 bits.                                                                                          |
| [**Rúbrica**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Devuelve la dirección de [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dentro de [**un elemento VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                      |
| [**INFORMACIÓN DE \_ SECUENCIA MPEG1 \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Devuelve la dirección del encabezado de secuencia dentro de una [**estructura MPEG1VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)                                                          |
| [**ASÍNTO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Comprueba si un mapa de bits tiene una profundidad de color de 8 bits o menos.                                                                                                      |
| [**ENTRADAS \_ DE PALETA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera el número máximo de colores de la paleta de un mapa de bits especificado.                                                                                      |
| [**RESTABLECER \_ MÁSCARAS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Rellena los campos de máscara de color de una [**estructura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con ceros.                                                                            |
| [**RESTABLECER \_ ENCABEZADO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Rellena un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con ceros.                                                                                                   |
| [**RESTABLECER \_ PALETA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Rellena las entradas de la paleta en una [**estructura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con ceros.                                                                              |
| [**PALETA \_ DE EGA \_ DE TAMAÑO**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcula el tamaño necesario para las entradas de la paleta en un mapa de bits RGB de 4 bits.                                                                                         |
| [**MÁSCARAS \_ DE TAMAÑO**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcula el tamaño de las máscaras de color en una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                             |
| [**SIZE \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcula el tamaño de una estructura [**MPEG1VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) incluido el encabezado de secuencia.                                                      |
| [**PALETA DE \_ TAMAÑOS**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | calcula el tamaño de las entradas de la paleta en una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                         |
| [**SIZE \_ PREHEADER**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcula el desplazamiento de bytes del **campo bmiHeader** dentro de una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                              |
| [**SIZE \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcula el tamaño de la [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                                  |
| [**Truecolor**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Devuelve la [**estructura TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) de una [**estructura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Comprueba si hay errores en una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que puedan provocar saturaciones de búfer o desbordamientos de enteros.                                   |



 

## <a name="remarks"></a>Comentarios

La mayoría de las macros y funciones descritas en la sección están diseñadas para manipular estructuras **VIDEOINFOHEADER** y **VIDEOINFO** para mapas de bits RGB. Use estas macros con cuidado: la mayoría de ellas suponen que la estructura especificada se ha inicializado correctamente. Muchos de ellos también suponen que la **estructura BITMAPINFOHEADER** es el tamaño estándar; es decir, `biSize == sizeof(BITMAPINFOHEADER)` .

La DirectShow de clases base también proporciona las siguientes constantes globales, que definen las máscaras de color estándar para los mapas de bits de color verdadero.



| Datos globales | Descripción                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matriz de máscaras de color para un mapa de bits RGB de 16 bits en formato 5-5-5. |
| **bits565** | Matriz de máscaras de color para un mapa de bits RGB de 16 bits en formato 5-6-5. |
| **bits888** | Matriz de máscaras de color para un mapa de bits RGB de 24 bits.                 |



 

Cada una de estas constantes en una matriz de tres **DWORD,** que contiene las máscaras de color rojo, verde y azul, en ese orden.

 

 
