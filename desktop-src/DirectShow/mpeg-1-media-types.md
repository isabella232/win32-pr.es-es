---
description: En esta sección se enumeran los tipos de medios que se usan para los datos MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de medios MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689634"
---
# <a name="mpeg-1-media-types"></a>Tipos de medios MPEG-1

En esta sección se enumeran los tipos de medios que se usan para los datos MPEG-1.

## <a name="mpeg-1-system-stream"></a>Secuencia de sistema MPEG-1



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| Tipo principal            | \_Secuencia MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Tipo de formato           | FORMATO \_ MPEGStreams                             |
| Estructura de formato      | [**\_MPEGSYSTEMTYPE AM**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Contenido de ejemplo multimedia | Secuencia de bytes; sin alineación                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Secuencia del sistema MPEG-1 desde el CD de vídeo



|                       |                            |
|-----------------------|----------------------------|
| Tipo principal            | \_Secuencia MEDIATYPE          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Tipo de formato           | GUID \_ null                 |
| Estructura de formato      | None                       |
| Contenido de ejemplo multimedia | Secuencia de bytes; sin alineación. |



 

## <a name="mpeg-1-audio-packet"></a>Paquete de audio MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principal            | Audio de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | DAR formato a \_ WaveFormatEx                           |
| Estructura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Contenido de ejemplo multimedia | Paquete MPEG-1 único, incluido el encabezado de paquete. |



 

## <a name="mpeg-1-audio-payload"></a>Carga de audio MPEG-1



|                       |                                            |
|-----------------------|--------------------------------------------|
| Tipo principal            | Audio de MEDIATYPE \_                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Tipo de formato           | DAR formato a \_ WaveFormatEx                       |
| Estructura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Contenido de ejemplo multimedia | Datos de audio MPEG-1 alineados en bytes.            |



 

## <a name="mpeg-1-video-packet"></a>Paquete de vídeo MPEG-1



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principal            | Vídeo de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | FORMATO \_ MPEGVideo                              |
| Estructura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Contenido de ejemplo multimedia | Paquete MPEG-1 único, incluido el encabezado de paquete. |



 

## <a name="mpeg-1-video-payload"></a>Carga de vídeo MPEG-1



|                       |                                          |
|-----------------------|------------------------------------------|
| Tipo principal            | Vídeo de MEDIATYPE \_                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Tipo de formato           | FORMATO \_ MPEGVideo                        |
| Estructura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Contenido de ejemplo multimedia | Datos de vídeo MPEG-1 alineados en bytes.          |



 

## <a name="mpeg-1-native-video-stream"></a>Secuencia de vídeo de MPEG-1 nativo



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principal            | \_Secuencia MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Tipo de formato           | GUID \_ null                                     |
| Estructura de formato      | None                                           |
| Contenido de ejemplo multimedia | Matriz de bytes de secuencia de vídeo (sin capa del sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Secuencia de audio de MPEG-1 nativo



|                       |                                                |
|-----------------------|------------------------------------------------|
| Tipo principal            | \_Secuencia MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Tipo de formato           | GUID \_ null                                     |
| Estructura de formato      | None                                           |
| Contenido de ejemplo multimedia | Matriz de bytes de secuencia de audio (sin capa del sistema). |



 

## <a name="remarks"></a>Observaciones

Los filtros MPEG-1 de DirectShow admiten estos tipos de la manera siguiente.



| Filter               | Dirección | Tipos de medios admitidos                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Separador MPEG-1      | Entrada     | Flujo del sistema streamMPEG-1 del sistema MPEG-1 del CD de vídeo<br/>                                                 |
| Separador MPEG-1      | Output    | Carga de audio packetMPEG-1 de audio MPEG-1<br/> Paquete de vídeo MPEG-1<br/> Carga de vídeo MPEG-1<br/> |
| Códec de audio de software | Entrada     | Carga de audio packetMPEG-1 de audio MPEG-1<br/>                                                                |
| Códec de vídeo de software | Entrada     | Carga de vídeo MPEG-1 video packetMPEG-1<br/>                                                                |
| Códec de audio de software | Output    | Audio PCM                                                                                                         |
| Códec de vídeo de software | Output    | Vídeo sin comprimir (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

Los tipos de medios de paquete y carga de vídeo MPEG-1 contienen un encabezado de secuencia completo para que los datos se puedan reproducir desde el centro de un archivo sin necesidad de un encabezado de secuencia para inicializar la reproducción del vídeo.

El encabezado de la secuencia de vídeo se anexa al tipo de datos de vídeo del vídeo MPEG para que el juego pueda comenzar desde el medio de una secuencia. La longitud de este campo es de hasta 140 bytes. incluye el código de inicio del encabezado de secuencia (0x000001B3) al principio, junto con las matrices de cuantificación encontradas en el primer encabezado de secuencia encontrado.

 

 




