---
description: En este tema se describe cómo crear una topología de transcodificación en TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Creación de una topología de transcodificación con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5386af09b04f155295b807523cdb1c5519c946b45228df51d767e9d2a3aabe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959465"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Creación de una topología de transcodificación con TopoEdit

En este tema se describe cómo crear una topología de transcodificación en TopoEdit.

> [!Note]  
> Esta característica requiere Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Para crear una topología de transcodificación

1.  En el menú **Archivo** , haga clic **en Representar transcodificación.**

2.  En el **cuadro de diálogo Seleccionar origen** multimedia, seleccione el archivo de origen para la transcodificación.
3.  Haga clic en **Abrir**.
4.  En el **cuadro de diálogo Elegir perfil de** transcodificación, seleccione uno de los perfiles de codificación en la lista desplegable.
    > [!Note]  
    > Los perfiles se cargan desde el archivo TranscodeProfiles.xml.

     

5.  En el **cuadro de diálogo Elegir archivo de** destino, seleccione el nombre del archivo de salida.
6.  TopoEdit crea la topología de transcodificación y muestra los nodos de topología en la ventana principal de la aplicación.
7.  Haga clic en **el botón** Reproducir de la barra de herramientas para ejecutar la sesión multimedia. Espere a que se complete la codificación.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit carga los perfiles de codificación desde el archivo TranscodeProfiles.xml. Este archivo se encuentra en el directorio Bin del SDK Windows.

El archivo comienza con un **elemento TedTranscodeProfiles.** Cada perfil comienza con un **elemento TedTranscodeProfile.** Cada perfil consta de un conjunto de valores con el formato `<VALUE_NAME Value="VALUE"/>` . Se definen los siguientes valores:



| Value                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Promedio de bytes por segundo para la secuencia de audio. Equivalente al atributo [**MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND.**](mf-mt-audio-avg-bytes-per-second-attribute.md)<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Número de bits por muestra para la secuencia de audio. Equivalente al atributo [**MF MT AUDIO BITS PER \_ \_ \_ \_ \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | Alineación de bloques para la secuencia de audio. Equivalente al atributo [**MF MT AUDIO BLOCK \_ \_ \_ \_ ALIGNMENT.**](mf-mt-audio-block-alignment-attribute.md)<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Valor específico del códec que define el perfil de audio. Equivalente al atributo [ \_ TRANSCODE \_ ENCODINGPROFILE de MF.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | Subtipo de audio codificado. Equivalente al atributo [**MF \_ MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Número de canales de la secuencia de audio. Equivalente al atributo [**MF MT AUDIO NUM \_ \_ \_ \_ CHANNELS.**](mf-mt-audio-num-channels-attribute.md)<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | Velocidad de muestreo de la secuencia de audio, en muestras por segundo. Equivalente al atributo [**MF MT AUDIO SAMPLES PER \_ \_ \_ \_ \_ SECOND.**](mf-mt-audio-samples-per-second-attribute.md)<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Tipo de contenedor de archivos. Equivalente al atributo [ \_ TRANSCODE \_ CONTAINERTYPE de MF.](mf-transcode-containertype.md) <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | Nombre para mostrar del perfil.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Especifique 1 si los metadatos no se deben transferir al archivo de salida, o 0 si se deben transferir metadatos. Equivalente al atributo SKIP METADATA TRANSFER de [MF \_ \_ \_ \_ TRANSCODE.](mf-transcode-skip-metadata-transfer.md)<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | Velocidad de bits de vídeo media. Equivalente al atributo [**AVG \_ \_ \_ BITRATE de MF MT.**](mf-mt-avg-bitrate-attribute.md) <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Valor específico del códec que define la calidad de la codificación. Equivalente al atributo [MF \_ TRANSCODE \_ QUALITYVSSPEED.](mf-transcode-qualityvsspeed.md) <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Valor específico del códec que define el perfil de vídeo. Equivalente al atributo [ \_ TRANSCODE \_ ENCODINGPROFILE de MF.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | Subtipo de vídeo codificado. Equivalente al atributo [**MF \_ MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Alto del vídeo de salida. Equivalente al atributo [**MF \_ MT FRAME \_ \_ SIZE.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | Denominador de la velocidad de fotogramas del vídeo de salida. Equivalente al atributo [**MF \_ MT FRAME \_ \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Numerador de la velocidad de fotogramas del vídeo de salida. Equivalente al atributo [**MF \_ MT FRAME \_ \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Ancho del vídeo de salida. Equivalente al atributo [**MF \_ MT FRAME \_ \_ SIZE.**](mf-mt-frame-size-attribute.md)<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | Denominador de la relación de aspecto de píxeles (PAR) del vídeo de salida. Equivalente al atributo [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | Numerador del PAR del vídeo de salida. Equivalente al atributo [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




