---
description: Atributos de tipo multimedia
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Atributos de tipo multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52e906baa7bbac14d33dbc263e3a1edfa43b65851d96d0573032784c0149425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827465"
---
# <a name="media-type-attributes"></a>Atributos de tipo multimedia

Los atributos siguientes se aplican a los tipos de medios. Algunos de estos atributos están diseñados solo para convertir formatos de tipo de medio heredados en tipos Media Foundation multimedia.

## <a name="general-format-attributes"></a>Atributos de formato general

Estos atributos se pueden aplicar a todos los tipos de medios.



| Atributo                                                                            | Descripción                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | Especifica si cada muestra es independiente de las demás muestras de la secuencia.       |
| [**TIPO \_ DE FORMATO MF MT \_ \_ \_ AM**](mf-mt-am-format-type-attribute.md)                   | GUID de formato.                                                                           |
| [**MF \_ MT \_ COMPRIMIDO**](mf-mt-compressed-attribute.md)                             | Especifica si los datos multimedia están comprimidos                                         |
| [**EJEMPLOS \_ DE TAMAÑO FIJO \_ DE \_ \_ MF MT**](mf-mt-fixed-size-samples-attribute.md)           | Especifica si las muestras tienen un tamaño fijo.                                       |
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md)                            | GUID de tipo principal.                                                                       |
| [**TAMAÑO DE \_ MUESTRA DE MF MT \_ \_**](mf-mt-sample-size-attribute.md)                          | Tamaño de cada muestra, en bytes.                                                         |
| [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)                                   | GUID de subtipo.                                                                          |
| [**DATOS \_ DE USUARIO DE MF MT \_ \_**](mf-mt-user-data-attribute.md)                              | Contiene datos de usuario para un tipo de medio que se ha convertido a partir de una estructura de formato heredada. |
| [**TIPO \_ ENCAPSULADO MF MT \_ \_**](mf-mt-wrapped-type-attribute.md)                        | Contiene un tipo de medio que se ha encapsulado en otro tipo de medio.                     |



 

## <a name="audio-format-attributes"></a>Atributos de formato de audio

Estos atributos se pueden aplicar a tipos de medios cuyo tipo principal es igual a MFMediaType \_ Audio.



| Atributo                                                                                            | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [INDICACIÓN \_ DE NIVEL DE PERFIL DE AUDIO MF MT \_ AAC \_ \_ \_ \_](mf-mt-aac-audio-profile-level-indication.md)       | Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).             |
| [TIPO \_ DE CARGA DE AAC MT \_ \_ MF \_](mf-mt-aac-payload-type.md)                                             | Especifica el tipo de carga para una secuencia de codificación de audio avanzada (AAC).                       |
| [**PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Número medio de bytes por segundo.                                                         |
| [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ EJEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)                    | Número de bits por muestra de audio.                                                            |
| [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md)                     | Alineación de bloques, en bytes.                                                                  |
| [**MÁSCARA \_ DE CANAL DE \_ AUDIO \_ \_ MF MT**](mf-mt-audio-channel-mask-attribute.md)                           | Especifica la asignación de canales de audio a las posiciones del hablante.                            |
| [**MUESTRAS DE AUDIO FLOAT DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-float-samples-per-second-attribute.md) | Número de muestras de audio por segundo (valor de punto flotante).                                  |
| [**MF \_ MT \_ AUDIO \_ FOLDDOWN \_ MATRIX**](mf-mt-audio-folddown-matrix-attribute.md)                     | Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo.        |
| [**CANALES \_ NUM \_ DE AUDIO \_ MF MT \_**](mf-mt-audio-num-channels-attribute.md)                           | Número de canales de audio.                                                                   |
| [**MF \_ MT \_ AUDIO \_ \_ PREFERIR FORMA DE ONDAATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Especifica la estructura de formato heredado preferida que se usará al convertir un tipo de medio de audio. |
| [**EJEMPLOS \_ DE AUDIO MF MT POR \_ \_ \_ \_ BLOQUE**](mf-mt-audio-samples-per-block-attribute.md)                | Número de muestras de audio contenidas en un bloque comprimido de datos de audio.                    |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)              | Número de muestras de audio por segundo (valor entero).                                         |
| [**\_BITS VÁLIDOS DE AUDIO MF MT \_ \_ POR \_ \_ \_ EJEMPLO**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Número de bits válidos de datos de audio en cada muestra de audio.                                    |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | Haga referencia al nivel de volumen medio de Windows archivo de audio multimedia.                               |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | Nivel de volumen promedio de destino de un Windows de audio multimedia.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | Haga referencia al nivel de volumen máximo de Windows archivo de audio multimedia.                                  |
| [**MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | Nivel de volumen máximo de destino de un Windows de audio multimedia.                                     |
| [MF \_ MT \_ ORIGINAL \_ WAVE \_ FORMAT \_ TAG](mf-mt-original-wave-format-tag.md)                            | Contiene la etiqueta de formato WAVE original para una secuencia de audio.                                  |



 

## <a name="video-format-attributes"></a>Atributos de formato de vídeo

Estos atributos se pueden aplicar a los tipos de medios cuyo tipo principal es igual a MFMediaType \_ Video.



| Atributo                                                                              | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**TASA \_ DE ERRORES DE \_ BITS PROMEDIO DE \_ \_ MT DE MF \_**](mf-mt-avg-bit-error-rate-attribute.md)            | Velocidad de errores de datos.                                                                                                                        |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                            | Velocidad de datos aproximada de la secuencia de vídeo.                                                                                              |
| [**PRINCIPALES \_ DE \_ VÍDEO PERSONALIZADO \_ \_ DE MF MT**](mf-mt-custom-video-primaries-attribute.md)     | Elementos principal de color personalizado.                                                                                                                 |
| [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)                      | Paso de superficie predeterminado.                                                                                                                 |
| [**MARCAS \_ DRM DE MF MT \_ \_**](mf-mt-drm-flags-attribute.md)                                | Especifica si el vídeo requiere aplicar la protección de copia.                                                                         |
| [**VELOCIDAD \_ DE \_ FOTOGRAMAS MT DE MF \_**](mf-mt-frame-rate-attribute.md)                              | Velocidad de fotogramas.                                                                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md)                      | Velocidad máxima de fotogramas admitida por un dispositivo de captura de vídeo.                                                                             |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)                      | Velocidad mínima de fotogramas admitida por un dispositivo de captura de vídeo.                                                                             |
| [**TAMAÑO DEL \_ MARCO DE \_ MT \_ DE MF**](mf-mt-frame-size-attribute.md)                              | Ancho y alto del marco de vídeo.                                                                                                    |
| [**APERTURA \_ GEOMÉTRICA DE MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)              | Apertura geométrica.                                                                                                                     |
| [**MODO \_ DE \_ INTERLACE MF \_ MT**](mf-mt-interlace-mode-attribute.md)                      | Describe cómo se entrelazan los fotogramas.                                                                                                |
| [**ESPACIADO \_ MÁXIMO DE \_ \_ FOTOGRAMAS CLAVE DE \_ MF MT**](mf-mt-max-keyframe-spacing-attribute.md)         | Número máximo de fotogramas de un fotograma clave al siguiente.                                                                                |
| [**APERTURA \_ DE PANTALLA MÍNIMA \_ DE \_ \_ MF MT**](mf-mt-minimum-display-aperture-attribute.md) | Apertura de pantalla mínima.                                                                                                               |
| [**ENCABEZADO \_ DE SECUENCIA MPEG DE MF MT \_ \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)         | Encabezado de secuencia MPEG-1 o MPEG-2.                                                                                                       |
| [**MF \_ MT \_ MPEG \_ START \_ TIME \_ CODE**](mf-mt-mpeg-start-time-code-attribute.md)        | Código de hora de inicio de grupo de imágenes (GOP).                                                                                                |
| [**MF \_ MT \_ MPEG2 \_ FLAGS**](mf-mt-mpeg2-flags-attribute.md)                            | Varias marcas para vídeo MPEG-2.                                                                                                   |
| [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                            | Nivel MPEG-2 o H.264.                                                                                                                  |
| [**MF \_ MT \_ MPEG2 \_ PROFILE**](mf-mt-mpeg2-profile-attribute.md)                        | Perfil MPEG-2 o H.264.                                                                                                                |
| [MF \_ MT \_ ORIGINAL \_ 4CC](mf-mt-original-4cc.md)                                        | Contiene el códec original FOURCC para una secuencia de vídeo.                                                                                  |
| [**MARCAS \_ DE CONTROL DEL PANEL DE MT \_ \_ \_ DE MF**](mf-mt-pad-control-flags-attribute.md)               | Relación de aspecto del rectángulo de salida.                                                                                                   |
| [**PALETA \_ DE MT DE \_ MF**](mf-mt-palette-attribute.md)                                     | Entradas de paleta.                                                                                                                        |
| [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)               | Define la región 4×3 del vídeo que debe mostrarse en modo de panorámica o examen.                                                              |
| [**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)                 | Especifica si el modo pan/scan está habilitado.                                                                                             |
| [**RELACIÓN DE \_ ASPECTO \_ DE PÍXELES DE MT \_ DE \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)             | Relación de aspecto de píxeles.                                                                                                                     |
| [**SUGERENCIA \_ DE CONTENIDO DE ORIGEN DE MF \_ \_ \_ MT**](mf-mt-source-content-hint-attribute.md)           | Relación de aspecto prevista.                                                                                                                  |
| [**MF \_ MT \_ TRANSFER \_ FUNCTION**](mf-mt-transfer-function-attribute.md)                | Función de conversión de RGB a R'G'B'.                                                                                                 |
| [MF \_ MT \_ VIDEO \_ 3D](mf-mt-video-3d.md)                                                | Especifica si una secuencia de vídeo contiene contenido 3D.                                                                                   |
| [**MF \_ MT \_ VIDEO \_ CHROMA \_ SITING**](mf-mt-video-chroma-siting-attribute.md)           | Describe cómo se muestreó la zona para el vídeo de Y'Cb'Cr'.                                                                                    |
| [**ILUMINACIÓN \_ DE VÍDEO MF MT \_ \_**](mf-mt-video-lighting-attribute.md)                      | Condiciones de iluminación óptimas para la visualización.                                                                                                |
| [**MF \_ MT \_ VIDEO \_ NOMINAL \_ RANGE**](mf-mt-video-nominal-range-attribute.md)           | Intervalo nominal de la información de color                                                                                                  |
| [**MF \_ MT \_ VIDEO \_ PRIMARIES**](mf-mt-video-primaries-attribute.md)                    | Color principal.                                                                                                                        |
| [ROTACIÓN \_ DE VÍDEO DE MT \_ \_ DE MF](mf-mt-video-rotation.md)                                    | Especifica la rotación de un fotograma de vídeo en la dirección en sentido contrario a las agujas del reloj.                                                             |
| [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                              | Matriz de conversión del espacio de colores Y'Cb'Cr' al espacio de colores R'G'B'.                                                              |
| [MF \_ XVP \_ CALLER ASIGNA LA \_ \_ SALIDA](mf-xvp-caller-allocates-output.md)               | Especifica si el autor de la llamada asignará las texturas usadas para la salida por [**el MFT del procesador de vídeo.**](video-processor-mft.md) |
| [MF \_ XVP \_ DISABLE \_ FRC](mf-xvp-disable-frc.md)                                        | Deshabilita la conversión de velocidad de fotogramas en [**el MFT del procesador de vídeo.**](video-processor-mft.md)                                               |



 

## <a name="other-format-attributes"></a>Otros atributos de formato

Los siguientes atributos se aplican al vídeo DV intercalado.



| Atributo                                                                      | Descripción                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT DV A CTRL PACK \_ \_ \_ \_ \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Paquete de control de código fuente auxiliar de audio (A ODBC) para el primer bloque de audio. |
| [**MF \_ MT DV A CTRL PACK \_ \_ \_ \_ \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Paquete de control de código fuente A ODBC para el segundo bloque de audio.                  |
| [**MF \_ MT DV A MF \_ \_ \_ SRC PACK \_ \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | Paquete de origen de A ODBC para el primer bloque de audio.                           |
| [**MF \_ MT DV A MF \_ \_ \_ SRC PACK \_ \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | Paquete de origen de A ODBC para el segundo bloque de audio.                          |
| [**MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Paquete de control de código fuente auxiliar de vídeo (PEL).                           |
| [**MF \_ MT \_ DV \_ IQUE \_ SRC \_ PACK**](mf-mt-dv-vaux-src-pack-attribute.md)        | Paquete de origen de SUD.                                                     |



 

Los atributos siguientes se aplican a los archivos de formato de streaming avanzado (ASF).



| Atributo                                                      | Descripción                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [FORMATO \_ ARBITRARIO DE MT DE \_ \_ MF](mf-mt-arbitrary-format.md)        | Datos de formato adicionales para una secuencia binaria en un archivo ASF.       |
| [ENCABEZADO \_ ARBITRARIO MF MT \_ \_](mf-mt-arbitrary-header.md)        | Datos específicos del tipo para una secuencia binaria en un archivo ASF.           |
| [MF \_ MT \_ IMAGE \_ LOSS \_ TOLERANT](mf-mt-image-loss-tolerant.md) | Especifica si un flujo de imagen de ASF es un tipo JPEG degradable. |



 

Los siguientes atributos se aplican a los archivos MPEG-4.



| Atributo                                                                     | Descripción                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ENTRADA \_ DE EJEMPLO ACTUAL DE MF MT \_ MPEG4 \_ \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Índice de la entrada actual en el cuadro de descripción de ejemplo. |
| [DESCRIPCIÓN \_ DEL \_ EJEMPLO MPEG4 \_ DE \_ MF MT](mf-mt-mpeg4-sample-description.md)      | Cuadro de descripción de ejemplo.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



