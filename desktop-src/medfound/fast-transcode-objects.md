---
description: En este tema se describe cómo usar la API de transcodificación para codificar un archivo multimedia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso de Transcode API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742483"
---
# <a name="using-the-transcode-api"></a>Uso de Transcode API

En este tema se describe cómo usar la API de transcodificación para codificar un archivo multimedia.

-   [Información general](#overview)
-   [Crear un origen multimedia](#creating-a-media-source)
-   [Crear un perfil de transcodificación](#creating-a-transcode-profile)
    -   [Atributos de audio](#audio-attributes)
    -   [Atributos de vídeo](#video-attributes)
    -   [Atributos de contenedor](#container-attributes)
-   [Creación de una topología de transcodificación](#creating-a-transcode-topology)
-   [Ejecución de la sesión de codificación](#running-the-encoding-session)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Introducción

Antes de usar la API de transcodificación, la aplicación debe tener los siguientes fragmentos de información:

-   Ruta de acceso o dirección URL a un archivo multimedia existente que se volverá a codificar.
-   Nombre del archivo de salida.
-   Tipo de contenedor para el archivo de salida, como MP4 o Advanced Streaming Format (ASF).
-   Formato de codificación. Esta información incluye los tipos de medios que describen las secuencias de audio y vídeo codificadas.

Para usar la API de transcodificación, una aplicación realiza los pasos siguientes.

1.  Cree un origen multimedia para leer el archivo de origen.
2.  Cree un perfil de transcodificación. Agregue atributos que describan la secuencia de audio, la secuencia de vídeo y el contenedor de archivos.
3.  Use el perfil de transcodificación para crear una topología de codificación. (Para obtener más información sobre las topologías, vea [Acerca de las topologías).](about-topologies.md)
4.  Establezca la topología en la [sesión multimedia](media-session.md).
5.  Inicie la sesión multimedia y espere el [evento MESessionEnded.](mesessionended.md)

En el resto de este tema se describen estos pasos con más detalle.

## <a name="creating-a-media-source"></a>Crear un origen multimedia

Un origen multimedia es un objeto que lee y analiza el archivo de origen. Para crear un origen multimedia, use el [solucionador de origen](source-resolver.md). Puede encontrar código de ejemplo en el tema [Using the Source Resolver](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Crear un perfil de transcodificación

Un *perfil de transcodificación* describe el formato y la configuración que se usan para codificar el archivo de salida. El perfil de transcodificación contiene tres conjuntos de atributos:

-   Atributos de audio: describa el formato de audio de destino y la configuración del codificador de audio.
-   Atributos de vídeo: describa el formato de vídeo de destino y la configuración del codificador de vídeo.
-   Atributos de contenedor: defina el tipo de contenedor de archivos, así como algunos valores de codificación global.

Para crear un perfil de transcodificación, llame a [**la función MFCreateTranscodeProfile.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) Esta función devuelve un puntero a la [**interfaz IMFTranscodeProfile.**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) El objeto de perfil inicial está vacío; no contiene atributos. El siguiente paso consiste en agregar los atributos que definen el perfil.

### <a name="audio-attributes"></a>Atributos de audio

Para agregar atributos para la secuencia de audio, llame [**a IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Estos atributos especifican cómo se codifica la secuencia de audio. Si el archivo de salida no contendrá una secuencia de audio, omita estos atributos.

Los atributos de audio se divide en dos categorías:

-   Atributos que especifican el formato de la secuencia codificada
-   Atributos que especifican otros parámetros de codificación.

Los atributos de formato son simplemente atributos de tipo multimedia, como se describe en la sección [Tipos de medios de audio](audio-media-types.md). El conjunto exacto de atributos de formato depende del codificador. (Vea [Formatos multimedia admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)). Esta es una lista de atributos de formato de audio típicos:



| Atributo format                                                                         | Descripción                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [SUBTIPO \_ MT DE MF \_](mf-mt-subtype-attribute.md)                                           | Subtipo. Consulte [GUID de subtipo de audio.](audio-subtype-guids.md) |
| [CANALES \_ NUM \_ DE AUDIO \_ MF MT \_](mf-mt-audio-num-channels-attribute.md)                   | Número de canales de audio.                                    |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md)      | Número de muestras de audio por segundo.                          |
| [ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT](mf-mt-audio-block-alignment-attribute.md)             | Alineación de bloques.                                             |
| [PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | El número medio de bytes por segundo (la velocidad de bits codificada).   |



 

Se definen los siguientes parámetros de codificación.



| Parámetro de codificación                                                             | Descripción                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [CODIFICADOR \_ MF TRANSCODE \_ DONOT \_ INSERT \_](mf-transcode-donot-insert-encoder.md) | Impide que la API de transcodificación inserte un codificador para la secuencia de audio. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Especifica la plantilla de conformidad del dispositivo. (Solo se aplica a los archivos ASF).    |
| [MF \_ TRANSCODE \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Especifica el equilibrio entre la calidad y la velocidad de codificación.                |



 

Debe establecer los atributos de formato. Los parámetros de codificación son opcionales.

Una manera de buscar un formato compatible con el codificador es llamar a la función [**MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) El codificador deseado se especifica mediante subtipo. La función devuelve una colección de tipos de medios para ese codificador. Puede seleccionar un tipo de la lista y copiar los atributos en el perfil. Para obtener código de ejemplo que usa este enfoque, [vea Tutorial: Codificación de un archivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Atributos de vídeo

Para agregar atributos para la secuencia de vídeo, llame [**a IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Estos atributos especifican cómo se codifica la secuencia de vídeo. Si el archivo de salida no contendrá una secuencia de vídeo, omita estos atributos.

Al igual que con los atributos de audio, los atributos de vídeo se divide en dos categorías:

-   Atributos que especifican el formato de la secuencia codificada
-   Atributos que especifican otros parámetros de codificación.

Los atributos de formato son atributos de tipo multimedia, como se describe en la sección [Tipos de medios de vídeo](video-media-types.md). Esta es una lista de atributos de formato de vídeo típicos:



| Atributo format                                                       | Descripción                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [SUBTIPO \_ MT DE MF \_](mf-mt-subtype-attribute.md)                         | Subtipo. Consulte [GUID de subtipo de vídeo.](video-subtype-guids.md) |
| [VELOCIDAD \_ DE \_ FOTOGRAMAS MT DE MF \_](mf-mt-frame-rate-attribute.md)                  | Velocidad de fotogramas.                                                  |
| [TAMAÑO DEL \_ MARCO DE \_ MT \_ DE MF](mf-mt-frame-size-attribute.md)                  | Tamaño del marco.                                                  |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)            | Velocidad de bits media.                                            |
| [RELACIÓN \_ DE ASPECTO DE \_ \_ PÍXELES MF MT \_](mf-mt-pixel-aspect-ratio-attribute.md) | Relación de aspecto de píxeles.                                          |



 

Se definen los siguientes parámetros de codificación.



| Parámetro de codificación                                                             | Descripción                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [CODIFICADOR \_ MF TRANSCODE \_ DONOT \_ INSERT \_](mf-transcode-donot-insert-encoder.md) | Impide que la API de transcodificación inserte un codificador para la secuencia de vídeo. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Especifica la plantilla de conformidad del dispositivo. (Solo se aplica a los archivos ASF).    |
| [MF \_ TRANSCODE \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Especifica el equilibrio entre la calidad y la velocidad de codificación.                |



 

Debe establecer los atributos de formato. Los parámetros de codificación son opcionales.

### <a name="container-attributes"></a>Atributos de contenedor

Los atributos de contenedor definen las características de nivel de archivo del archivo de salida. Para establecer atributos de contenedor, llame [**a IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Se definen los atributos siguientes.



| Atributo                                                                          | Descripción                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ TRANSCODE \_ ADJUST \_ PROFILE](mf-transcode-adjust-profile.md)                  | Define la configuración de secuencia que se usará para la topología de transcodificación. Puede establecer las marcas para usar la configuración de origen de entrada o usar atributos de flujo personalizados. |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | Especifica el formato de archivo del archivo de salida, como MP4 o ASF. En función de este valor, se agrega el receptor multimedia adecuado a la topología.            |
| [MF \_ TRANSCODE \_ SKIP \_ METADATA \_ TRANSFER](mf-transcode-skip-metadata-transfer.md) | Especifica si los metadatos del origen se copian en el archivo de salida.                                                                               |
| [MF \_ TRANSCODE \_ TOPOLOGYMODE](mf-transcode-topologymode.md)                       | Especifica si se pueden usar códecs basados en hardware durante la transcodificación.                                                                                |
| [Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)          | Desbloquea un códec que tiene restricciones de campo de uso. Para obtener más información, [vea Restricciones de campo de uso.](field-of-use-restrictions.md)              |



 

Se [requiere el atributo \_ \_ TRANSCODE CONTAINERTYPE de MF.](mf-transcode-containertype.md) Los demás atributos de contenedor son opcionales.

## <a name="creating-a-transcode-topology"></a>Creación de una topología de transcodificación

La topología de transcodificación es una topología parcial que contiene el origen multimedia, los códecs adecuados y el receptor multimedia. Para crear la topología de transcodificación, llame a la [**función MFCreateTranscodeTopology.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) Esta función toma los parámetros siguientes como entrada:

-   Puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.
-   Nombre del archivo de salida.
-   Puntero a la interfaz [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del perfil de transcodificación.

La función devuelve un puntero a la [**interfaz DETOPOLOGY.**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="running-the-encoding-session"></a>Ejecución de la sesión de codificación

Después de crear la topología, está listo para codificar el archivo. Puede descartar el perfil en este momento.

1.  Llame [**a MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.
2.  Llame [**a IMFMediaSession::SetTopology para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) establecer la topología en la sesión multimedia.
3.  Llame [**a IMFMediaSession::Start para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) iniciar la sesión de codificación.
4.  Espere al [evento MESessionEnded.](mesessionended.md)
5.  Llame [**a IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.
6.  Espere al [evento MESessionClosed.](mesessionclosed.md)
7.  Llame [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Llame [**a IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

La mayor parte del tiempo invertido en codificación se produce entre los pasos 3 y 4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[Acerca de la sesión multimedia](about-the-media-session.md)
</dt> </dl>

 

 



