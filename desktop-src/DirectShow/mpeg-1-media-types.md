---
description: En esta sección se enumeran los tipos de medios usados para los datos MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de medios MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f6486b455fc2045ceb0256f6b6344f06a8923ef767c397068022acec052627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684935"
---
# <a name="mpeg-1-media-types"></a>Tipos de medios MPEG-1

En esta sección se enumeran los tipos de medios usados para los datos MPEG-1.

## <a name="mpeg-1-system-stream"></a>Secuencia de sistema MPEG-1



| Etiqueta | Valor |
|-----------------------|-------------------------------------------------|
| Tipo principal            | Secuencia \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Tipo de formato           | FORMAT \_ MPEGStreams                             |
| Estructura de formato      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Contenido de ejemplo multimedia | Secuencia de bytes; sin alineación                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Secuencia del sistema MPEG-1 desde CD de vídeo (VCD)



| Etiqueta | Value |
|-----------------------|----------------------------|
| Tipo principal            | Secuencia \_ MEDIATYPE          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Tipo de formato           | GUID \_ NULL                 |
| Estructura de formato      | Ninguno                       |
| Contenido de ejemplo multimedia | Secuencia de bytes; sin alineación. |



 

## <a name="mpeg-1-audio-packet"></a>Paquete de audio MPEG-1



| Etiqueta | Value |
|-----------------------|------------------------------------------------|
| Tipo principal            | MEDIATYPE \_ Audio                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | FORMAT \_ WaveFormatEx                           |
| Estructura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Contenido de ejemplo multimedia | Paquete MPEG-1 único, incluido el encabezado de paquete. |



 

## <a name="mpeg-1-audio-payload"></a>Carga de audio MPEG-1



| Etiqueta | Value |
|-----------------------|--------------------------------------------|
| Tipo principal            | MEDIATYPE \_ Audio                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Tipo de formato           | FORMAT \_ WaveFormatEx                       |
| Estructura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Contenido de ejemplo multimedia | Datos de audio MPEG-1 alineados con bytes.            |



 

## <a name="mpeg-1-video-packet"></a>Paquete de vídeo MPEG-1



| Etiqueta | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Vídeo \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | FORMAT \_ MPEGVideo                              |
| Estructura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Contenido de ejemplo multimedia | Paquete MPEG-1 único, incluido el encabezado de paquete. |



 

## <a name="mpeg-1-video-payload"></a>Carga de vídeo MPEG-1



| Etiqueta | Valor |
|-----------------------|------------------------------------------|
| Tipo principal            | Vídeo \_ MEDIATYPE                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Tipo de formato           | FORMAT \_ MPEGVideo                        |
| Estructura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Contenido de ejemplo multimedia | Datos de vídeo MPEG-1 alineados en bytes.          |



 

## <a name="mpeg-1-native-video-stream"></a>Secuencia de vídeo nativa MPEG-1



| Etiqueta | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Secuencia \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Tipo de formato           | GUID \_ NULL                                     |
| Estructura de formato      | Ninguno                                           |
| Contenido de ejemplo multimedia | Matriz de bytes de secuencia de vídeo (sin capa del sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Secuencia de audio nativa MPEG-1



| Etiqueta | Value |
|-----------------------|------------------------------------------------|
| Tipo principal            | Secuencia \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Tipo de formato           | GUID \_ NULL                                     |
| Estructura de formato      | Ninguno                                           |
| Contenido de ejemplo multimedia | Matriz de bytes de secuencia de audio (sin capa del sistema). |



 

## <a name="remarks"></a>Comentarios

Los DirectShow MPEG-1 admiten estos tipos como se muestra a continuación.



| Filter               | Dirección | Tipos de medios admitidos                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Divisor MPEG-1      | Entrada     | Flujo del sistema MPEG-1 StreamMPEG-1 del sistema desde CD de vídeo (VCD)<br/>                                                 |
| Divisor MPEG-1      | Salida    | Paquete de audio MPEG-1Mpeg-1 Carga de audio<br/> Paquete de vídeo MPEG-1<br/> Carga de vídeo MPEG-1<br/> |
| Códec de audio de software | Entrada     | Paquete de audio MPEG-1Mpeg-1 Carga de audio<br/>                                                                |
| Códec de vídeo de software | Entrada     | Carga de vídeo MPEG-1 Video packetMPEG-1<br/>                                                                |
| Códec de audio de software | Salida    | Audio de PCM                                                                                                         |
| Códec de vídeo de software | Salida    | Vídeo sin comprimir (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

Los tipos multimedia de carga y paquete de vídeo MPEG-1 contienen un encabezado de secuencia completo para que los datos se puedan reproducir desde el centro de un archivo sin necesidad de un encabezado de secuencia para inicializar la reproducción de vídeo.

El encabezado de secuencia de vídeo se anexa al tipo de datos de vídeo para el vídeo MPEG para que la reproducción pueda comenzar desde el centro de una secuencia. La longitud de este campo es de hasta 140 bytes; incluye el código de inicio del encabezado de secuencia (0x000001B3) al principio, junto con las matrices de cuantificación que se encuentran en el primer encabezado de secuencia encontrado.

 

 




