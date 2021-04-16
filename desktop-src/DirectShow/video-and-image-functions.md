---
description: Funciones de vídeo e imagen
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funciones de vídeo e imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55e439a17dd570b6e939d1cb84d836f9100eaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677546"
---
# <a name="video-and-image-functions"></a>Funciones de vídeo e imagen

Estas funciones y macros manipulan las estructuras de formato de vídeo de DirectShow.



| Función                                                             | Descripción                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**las \_ máscaras de bits \_ coinciden**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Compara las máscaras de color de dos estructuras de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                                       |
| [**MÁSCARAS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera las máscaras de color de una estructura de [**VIDEOinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Comprueba si hay errores en un tipo de medio que contiene una estructura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y que pueden producir desbordamientos de búfer o desbordamientos de enteros.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Comprueba si hay errores en un tipo de medio que contiene una estructura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) y que pueden producir desbordamientos de búfer o desbordamientos de enteros. |
| [**COLOREA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera las entradas de la paleta de una estructura de [**VIDEOinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina si una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contiene una paleta.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Convierte un tipo de medio que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en uno que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIB**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcula el número de bytes requerido por un mapa de bits independiente del dispositivo (DIB).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcula el tamaño necesario para una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que puede contener una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Devuelve la primera entrada de la paleta en una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcula el número de bytes requerido por un mapa de bits independiente del dispositivo (DIB).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Devuelve el **GUID** del subtipo de medios para el mapa de bits especificado.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera el nombre legible de un subtipo de vídeo.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Devuelve el **GUID** del subtipo de medio para un mapa de bits RGB sin comprimir de 16 bits.                                                                                          |
| [**ENCABEZADO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Devuelve la dirección de [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dentro de un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader).                                      |
| [**Información de la \_ secuencia MPEG1 \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Devuelve la dirección del encabezado de secuencia dentro de una estructura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .                                                          |
| [**De paleta**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Comprueba si un mapa de bits tiene una profundidad de color de 8 bits o menos.                                                                                                      |
| [**entradas de la paleta \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera el número máximo de colores de la paleta de un mapa de bits especificado.                                                                                      |
| [**RESTABLECER \_ máscaras**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Rellena los campos de máscara de color de una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con ceros.                                                                            |
| [**RESTABLECER \_ encabezado**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Rellena un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con ceros.                                                                                                   |
| [**RESTABLECER \_ paleta**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Rellena las entradas de la paleta en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con ceros.                                                                              |
| [**paleta de tamaño \_ EGA \_**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcula el tamaño necesario para las entradas de la paleta en un mapa de bits RGB de 4 bits.                                                                                         |
| [**máscaras de tamaño \_**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcula el tamaño de las máscaras de color en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                             |
| [**TAMAÑO \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcula el tamaño de una estructura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) , incluido el encabezado de secuencia.                                                      |
| [**paleta de tamaño \_**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | calcula el tamaño de las entradas de la paleta en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                         |
| [**TAMAÑO del \_ encabezado**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcula el desplazamiento de bytes del campo **bmiHeader** dentro de una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                              |
| [**TAMAÑO del \_ VIDEOencabezado**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcula el tamaño de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                                  |
| [**COLORES**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Devuelve la estructura [**TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) de una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Comprueba si hay errores en una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que puedan producir desbordamientos de búfer o desbordamientos de enteros.                                   |



 

## <a name="remarks"></a>Observaciones

La mayoría de las macros y funciones que se describen en la sección están diseñadas para manipular estructuras **VIDEOINFOHEADER** y **videoinfo** para mapas de bits RGB. Use estas macros con cuidado: la mayoría de ellas suponen que la estructura especificada se ha inicializado correctamente. Muchos de ellos también suponen que la estructura **BITMAPINFOHEADER** es el tamaño estándar; es decir, `biSize == sizeof(BITMAPINFOHEADER)` .

La biblioteca de clases base de DirectShow también proporciona las constantes globales siguientes, que definen las máscaras de color estándar para los mapas de bits de color verdadero.



| Datos globales | Descripción                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matriz de máscaras de color para un mapa de bits RGB de 16 bits en formato 5-5-5. |
| **bits565** | Matriz de máscaras de color para un mapa de bits RGB de 16 bits en formato 5-6-5. |
| **bits888** | Matriz de máscaras de color para un mapa de bits RGB de 24 bits.                 |



 

Cada una de estas constantes en una matriz de tres **DWORD** s, que contiene las máscaras rojo, verde y azul, en ese orden.

 

 
