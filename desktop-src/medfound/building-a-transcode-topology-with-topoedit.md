---
description: En este tema se describe cómo crear una topología de transcodificación en TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Creación de una topología de transcodificación con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539639"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Creación de una topología de transcodificación con TopoEdit

En este tema se describe cómo crear una topología de transcodificación en TopoEdit.

> [!Note]  
> Esta característica requiere Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Para compilar una topología de transcodificación

1.  En el menú **archivo** , haga clic en **representar transcodificación**.

2.  En el cuadro de diálogo **Seleccionar origen de medios** , seleccione el archivo de origen para la transcodificación.
3.  Haga clic en **Abrir**.
4.  En el cuadro de diálogo **Elegir perfil** de transcodificación, seleccione uno de los perfiles de codificación de la lista desplegable.
    > [!Note]  
    > Los perfiles se cargan desde el archivo TranscodeProfiles.xml.

     

5.  En el cuadro de diálogo **elegir archivo de destino** , seleccione el nombre del archivo de salida.
6.  TopoEdit crea la topología de transcodificación y muestra los nodos de topología en la ventana principal de la aplicación.
7.  Haga clic en el botón **reproducir** de la barra de herramientas para ejecutar la sesión multimedia. Espere a que se complete la codificación.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit carga los perfiles de codificación del archivo TranscodeProfiles.xml. Este archivo se encuentra en el directorio bin del Windows SDK.

El archivo comienza con un elemento **TedTranscodeProfiles** . Cada perfil comienza con un elemento **TedTranscodeProfile** . Cada perfil está formado por un conjunto de valores con el formato `<VALUE_NAME Value="VALUE"/>` . Se definen los valores siguientes:



| Value                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Promedio de bytes por segundo de la secuencia de audio. Equivalente al atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | El número de bits por muestra para la secuencia de audio. Equivalente al atributo [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md) .<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | La alineación de bloque para la secuencia de audio. Equivalente al atributo [**de \_ \_ alineación del \_ bloque \_ de audio MF MT**](mf-mt-audio-block-alignment-attribute.md) .<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Valor específico del códec que define el perfil de audio. Equivalente al atributo [ \_ \_ ENCODINGPROFILE de Transcode MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | El subtipo de audio codificado. Equivalente al atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Número de canales de la secuencia de audio. Equivalente al atributo [**MF \_ MT \_ audio \_ NUM \_ Channels**](mf-mt-audio-num-channels-attribute.md) .<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | La velocidad de muestra de la secuencia de audio, en muestras por segundo. Equivalente al atributo [**MF \_ MT \_ audio \_ Samples \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) .<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Tipo de contenedor de archivos. Equivalente al atributo [ \_ \_ CONTAINERTYPE de Transcode MF](mf-transcode-containertype.md) . <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | Nombre para mostrar del perfil.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Especifique 1 si no se deben transferir los metadatos al archivo de salida o 0 si se deben transferir los metadatos. Equivalente al atributo [MF \_ Transcode \_ omitir \_ \_ transferencia de metadatos](mf-transcode-skip-metadata-transfer.md) .<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**Velocidad de bits**<br/>                                                                                 | Velocidad de bits de vídeo media. Equivalente al atributo [**MF \_ MT \_ AVG de \_ velocidad de bits**](mf-mt-avg-bitrate-attribute.md) . <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Valor específico del códec que define la calidad de la codificación. Equivalente al atributo [ \_ \_ QUALITYVSSPEED de Transcode MF](mf-transcode-qualityvsspeed.md) . <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Valor específico del códec que define el perfil de vídeo. Equivalente al atributo [ \_ \_ ENCODINGPROFILE de Transcode MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**Videoformat**<br/>                                                                                     | El subtipo de vídeo codificado. Equivalente al atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Alto del vídeo de salida. Equivalente al atributo [**de \_ \_ \_ tamaño de marco MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | El denominador de la velocidad de fotogramas del vídeo de salida. Equivalente al atributo [**MF \_ MT \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md) .<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Numerador de la velocidad de fotogramas del vídeo de salida. Equivalente al atributo [**MF \_ MT \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md) .<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Ancho del vídeo de salida. Equivalente al atributo [**de \_ \_ \_ tamaño de marco MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | El denominador de la relación de aspecto de píxeles (PAR) del vídeo de salida. Equivalente al atributo [**de \_ \_ relación de \_ aspecto \_ MF MT en píxeles**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | El numerador del PAR de vídeo de salida. Equivalente al atributo [**de \_ \_ relación de \_ aspecto \_ MF MT en píxeles**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




