---
description: Atributos de tipo de medio
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Atributos de tipo de medio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd3bc77197a3a897cd5280338451c33f1ea2637
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361911"
---
# <a name="media-type-attributes"></a>Atributos de tipo de medio

Los siguientes atributos se aplican a los tipos de medios. Algunos de estos atributos están pensados únicamente para convertir formatos de tipo de medios heredados en Media Foundation tipos de medios.

## <a name="general-format-attributes"></a>Atributos de formato general

Estos atributos se pueden aplicar a todos los tipos de medios.



| Atributo                                                                            | Descripción                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ All \_ Samples \_ independiente**](mf-mt-all-samples-independent-attribute.md) | Especifica si cada ejemplo es independiente de los demás ejemplos de la secuencia.       |
| [**\_tipo de formato MF MT \_ AM \_ \_**](mf-mt-am-format-type-attribute.md)                   | GUID de formato.                                                                           |
| [**MF \_ MT \_ comprimido**](mf-mt-compressed-attribute.md)                             | Especifica si los datos multimedia están comprimidos                                         |
| [**\_ejemplos de \_ \_ tamaño fijo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           | Especifica si los ejemplos tienen un tamaño fijo.                                       |
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                            | GUID de tipo principal.                                                                       |
| [**tamaño de muestra de MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                          | Tamaño de cada ejemplo, en bytes.                                                         |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                   | GUID del subtipo.                                                                          |
| [**datos de usuario de MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                              | Contiene los datos de usuario para un tipo de medio que se ha convertido a partir de una estructura de formato heredada. |
| [**\_ \_ tipo ajustado MF \_ MT**](mf-mt-wrapped-type-attribute.md)                        | Contiene un tipo de medio que se ha ajustado en otro tipo de medio.                     |



 

## <a name="audio-format-attributes"></a>Atributos de formato de audio

Estos atributos se pueden aplicar a los tipos de medios cuyo tipo principal es igual a MFMediaType \_ audio.



| Atributo                                                                                            | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [\_indicación de \_ \_ nivel de \_ Perfil de audio \_ \_ MF MT AAC](mf-mt-aac-audio-profile-level-indication.md)       | Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).             |
| [\_tipo de \_ carga del AAC \_ \_ de MF MT](mf-mt-aac-payload-type.md)                                             | Especifica el tipo de carga para una secuencia de codificación de audio avanzada (AAC).                       |
| [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Número promedio de bytes por segundo.                                                         |
| [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)                    | Número de bits por muestra de audio.                                                            |
| [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)                     | Alineación de bloque, en bytes.                                                                  |
| [**\_máscara de \_ canal de audio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)                           | Especifica la asignación de canales de audio a las posiciones del hablante.                            |
| [**\_muestras de audio Float de MF MT \_ \_ \_ \_ por \_ segundo**](mf-mt-audio-float-samples-per-second-attribute.md) | Número de muestras de audio por segundo (valor de punto flotante).                                  |
| [**\_matriz MF MT \_ audio \_ FOLDDOWN \_**](mf-mt-audio-folddown-matrix-attribute.md)                     | Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo.        |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                           | Número de canales de audio.                                                                   |
| [**MF \_ MT \_ audio \_ preferida \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Especifica la estructura de formato heredada preferida que se va a usar al convertir un tipo de medio de audio. |
| [**\_ejemplos de audio MF MT \_ \_ \_ por \_ bloque**](mf-mt-audio-samples-per-block-attribute.md)                | Número de muestras de audio contenidas en un bloque comprimido de datos de audio.                    |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)              | Número de muestras de audio por segundo (valor entero).                                         |
| [**\_ \_ bits válidos de audio MF MT \_ \_ \_ por \_ muestra**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Número de bits válidos de datos de audio en cada ejemplo de audio.                                    |
| [**MF \_ MT \_ audio \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Nivel de volumen promedio de referencia de un archivo de Windows Media Audio.                               |
| [**MF \_ MT \_ audio \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Nivel de volumen medio de destino de un archivo de Windows Media Audio.                                  |
| [**MF \_ MT \_ audio \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Nivel de volumen máximo de referencia de un archivo de Windows Media Audio.                                  |
| [**MF \_ MT \_ audio \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Nivel de volumen máximo de destino de un archivo de Windows Media Audio.                                     |
| [\_etiqueta de \_ \_ formato de onda original MF MT \_ \_](mf-mt-original-wave-format-tag.md)                            | Contiene la etiqueta de formato de onda original para una secuencia de audio.                                  |



 

## <a name="video-format-attributes"></a>Atributos de formato de vídeo

Estos atributos se pueden aplicar a los tipos de medios cuyo tipo principal es igual a MFMediaType \_ video.



| Atributo                                                                              | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tasa de \_ \_ errores de bit medio MF MT \_ \_**](mf-mt-avg-bit-error-rate-attribute.md)            | Tasa de errores de datos.                                                                                                                        |
| [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)                            | Velocidad de datos aproximada de la secuencia de vídeo.                                                                                              |
| [**\_ \_ \_ primarios de vídeo \_ personalizados MF MT**](mf-mt-custom-video-primaries-attribute.md)     | Primarios de color personalizado.                                                                                                                 |
| [**\_ \_ intervalo predeterminado de MF MT \_**](mf-mt-default-stride-attribute.md)                      | STRIDE de la superficie predeterminada.                                                                                                                 |
| [**\_ \_ marcas DRM de MF MT \_**](mf-mt-drm-flags-attribute.md)                                | Especifica si el vídeo requiere la aplicación de protección contra copia.                                                                         |
| [**\_velocidad de \_ fotogramas MF MT \_**](mf-mt-frame-rate-attribute.md)                              | Velocidad de fotogramas.                                                                                                                             |
| [\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md)                      | La velocidad de fotogramas máxima compatible con un dispositivo de captura de vídeo.                                                                             |
| [\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ mín.](mf-mt-frame-rate-range-min.md)                      | La velocidad de fotogramas mínima admitida por un dispositivo de captura de vídeo.                                                                             |
| [**\_tamaño de \_ marco MF MT \_**](mf-mt-frame-size-attribute.md)                              | Ancho y alto del fotograma de vídeo.                                                                                                    |
| [**\_ \_ apertura geométrica de MF MT \_**](mf-mt-geometric-aperture-attribute.md)              | Abertura geométrica.                                                                                                                     |
| [**\_ \_ modo entrelazado MF MT \_**](mf-mt-interlace-mode-attribute.md)                      | Describe cómo se entrelazan los fotogramas.                                                                                                |
| [**\_ \_ \_ espaciado de fotogramas clave de MF MT máx. \_**](mf-mt-max-keyframe-spacing-attribute.md)         | Número máximo de fotogramas de un fotograma clave a la siguiente.                                                                                |
| [**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md) | Abertura de pantalla mínima.                                                                                                               |
| [**\_encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)         | Encabezado de secuencia MPEG-1 o MPEG-2.                                                                                                       |
| [**\_código de \_ \_ hora de inicio de MPEG MT \_ MF \_**](mf-mt-mpeg-start-time-code-attribute.md)        | Código de hora de inicio de grupo de imágenes (GOP).                                                                                                |
| [**Marcas de MF \_ MT \_ MPEG2 \_**](mf-mt-mpeg2-flags-attribute.md)                            | Marcas misceláneas para vídeo MPEG-2.                                                                                                   |
| [**\_Nivel MF MT \_ MPEG2 \_**](mf-mt-mpeg2-level-attribute.md)                            | Nivel MPEG-2 o H. 264.                                                                                                                  |
| [**\_Perfil MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md)                        | Perfil MPEG-2 o H. 264.                                                                                                                |
| [\_ \_ 4cc original MF \_ MT](mf-mt-original-4cc.md)                                        | Contiene el objeto FOURCC del códec original para una secuencia de vídeo.                                                                                  |
| [**\_marcas de control MF MT \_ Pad \_ \_**](mf-mt-pad-control-flags-attribute.md)               | Relación de aspecto del rectángulo de salida.                                                                                                   |
| [**\_paleta MF MT \_**](mf-mt-palette-attribute.md)                                     | Entradas de la paleta.                                                                                                                        |
| [**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)               | Define la región de vídeo de 4 × 3 que se debe mostrar en el modo Pan/Scan.                                                              |
| [**examen de pan de MF \_ MT \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md)                 | Especifica si está habilitado el modo de panorámica o de recorrido.                                                                                             |
| [**\_relación de \_ aspecto de píxeles MF MT \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)             | Relación de aspecto de píxeles.                                                                                                                     |
| [**\_sugerencia de \_ contenido de origen MF MT \_ \_**](mf-mt-source-content-hint-attribute.md)           | Relación de aspecto deseada.                                                                                                                  |
| [**MF \_ MT \_ Transfer ( \_ función)**](mf-mt-transfer-function-attribute.md)                | Función de conversión de RGB a R'G'B '.                                                                                                 |
| [Vídeo de MF \_ MT en \_ \_ 3D](mf-mt-video-3d.md)                                                | Especifica si una secuencia de vídeo contiene contenido 3D.                                                                                   |
| [**vídeo croma de MF MT en el \_ \_ \_ \_ emplazamiento**](mf-mt-video-chroma-siting-attribute.md)           | Describe cómo se muestrea el croma para el vídeo de Y'Cb'Cr.                                                                                    |
| [**\_iluminación de \_ vídeo MF MT \_**](mf-mt-video-lighting-attribute.md)                      | Condiciones de iluminación óptimas para la visualización.                                                                                                |
| [**\_ \_ \_ rango nominal de vídeo \_ de MF MT**](mf-mt-video-nominal-range-attribute.md)           | Rango nominal de la información de color                                                                                                  |
| [**\_ \_ primarios de vídeo MF MT \_**](mf-mt-video-primaries-attribute.md)                    | Primarios de color.                                                                                                                        |
| [\_rotación de \_ vídeo MF MT \_](mf-mt-video-rotation.md)                                    | Especifica el giro de un fotograma de vídeo en el sentido contrario a las agujas del reloj.                                                             |
| [**MF \_ MT \_ YUV \_ Matrix**](mf-mt-yuv-matrix-attribute.md)                              | Matriz de conversión del espacio de colores de Y'Cb'Cr al espacio de colores de R'G'B.                                                              |
| [el autor de la llamada de MF \_ XVP \_ \_ asigna \_ resultados](mf-xvp-caller-allocates-output.md)               | Especifica si el autor de la llamada asignará las texturas utilizadas para la salida del [**MFT del procesador de vídeo**](video-processor-mft.md). |
| [MF \_ XVP \_ deshabilitar \_ FRC](mf-xvp-disable-frc.md)                                        | Deshabilita la conversión de velocidad de fotogramas en la [**MFT del procesador de vídeo**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Otros atributos de formato

Los siguientes atributos se aplican al vídeo DV intercalado.



| Atributo                                                                      | Descripción                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ AAUX \_ Ctrl \_ Pack \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Paquete de control de código fuente auxiliar de audio (AAUX) para el primer bloque de audio. |
| [**MF \_ MT \_ DV \_ AAUX \_ Ctrl \_ Pack \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Módulo de control de código fuente de AAUX para el segundo bloque de audio.                  |
| [**MF \_ MT \_ DV \_ AAUX \_ src \_ Pack \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | Paquete de origen de AAUX para el primer bloque de audio.                           |
| [**MF \_ MT \_ DV \_ AAUX \_ src \_ Pack \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | Paquete de origen de AAUX para el segundo bloque de audio.                          |
| [**MF \_ MT \_ DV \_ Vaux \_ Ctrl \_ Pack**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Módulo de control de código fuente de vídeo auxiliar (VAUX).                           |
| [**\_módulo de origen MF MT \_ DV \_ Vaux \_ \_**](mf-mt-dv-vaux-src-pack-attribute.md)        | Paquete de origen de VAUX.                                                     |



 

Los siguientes atributos se aplican a los archivos de formato avanzado de transmisión por secuencias (ASF).



| Atributo                                                      | Descripción                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [\_ \_ formato arbitrario MF \_ MT](mf-mt-arbitrary-format.md)        | Datos de formato adicionales para una secuencia binaria en un archivo ASF.       |
| [\_ \_ encabezado arbitrario MF \_ MT](mf-mt-arbitrary-header.md)        | Datos específicos del tipo para una secuencia binaria en un archivo ASF.           |
| [MF \_ MT \_ Image \_ loss \_ tolerante](mf-mt-image-loss-tolerant.md) | Especifica si una secuencia de imágenes ASF es un tipo JPEG degradado. |



 

Los siguientes atributos se aplican a los archivos MPEG-4.



| Atributo                                                                     | Descripción                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [\_Entrada de \_ \_ ejemplo actual \_ MPEG4 \_ de MF MT](mf-mt-mpeg4-current-sample-entry.md) | Índice de la entrada actual en el cuadro de Descripción del ejemplo. |
| [\_Descripción del \_ ejemplo de MPEG4 MT \_ de MF \_](mf-mt-mpeg4-sample-description.md)      | El cuadro Descripción del ejemplo.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



