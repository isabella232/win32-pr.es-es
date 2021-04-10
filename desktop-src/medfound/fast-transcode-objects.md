---
description: En este tema se describe cómo usar la API de Transcode para codificar un archivo multimedia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Uso de la API de Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153631"
---
# <a name="using-the-transcode-api"></a>Uso de la API de Transcode

En este tema se describe cómo usar la API de Transcode para codificar un archivo multimedia.

-   [Información general](#overview)
-   [Crear un origen de medios](#creating-a-media-source)
-   [Creación de un perfil de transcodificación](#creating-a-transcode-profile)
    -   [Atributos de audio](#audio-attributes)
    -   [Atributos de vídeo](#video-attributes)
    -   [Atributos de contenedor](#container-attributes)
-   [Creación de una topología de transcodificación](#creating-a-transcode-topology)
-   [Ejecutar la sesión de codificación](#running-the-encoding-session)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Antes de usar la API de Transcode, la aplicación debe tener los siguientes datos:

-   La ruta de acceso o la dirección URL de un archivo multimedia existente que se volverá a codificar.
-   Nombre del archivo de salida.
-   El tipo de contenedor para el archivo de salida, como MP4 o el formato de streaming avanzado (ASF).
-   Formato de codificación. Esta información incluye los tipos de medios que describen las secuencias de audio y vídeo codificadas.

Para usar la API de Transcode, una aplicación realiza los pasos siguientes.

1.  Cree un origen de medios para leer el archivo de origen.
2.  Cree un perfil de transcodificación. Agregue atributos que describan la secuencia de audio, el flujo de vídeo y el contenedor de archivos.
3.  Use el perfil de transcodificación para crear una topología de codificación. (Para obtener más información acerca de las topologías, consulte [acerca de las topologías](about-topologies.md)).
4.  Establezca la topología en la [sesión de medios](media-session.md).
5.  Inicie la sesión de medios y espere hasta el evento [MESessionEnded](mesessionended.md) .

En el resto de este tema se describen estos pasos con más detalle.

## <a name="creating-a-media-source"></a>Crear un origen de medios

Un origen multimedia es un objeto que lee y analiza el archivo de código fuente. Para crear un origen multimedia, use la [resolución de origen](source-resolver.md). Puede encontrar código de ejemplo en el tema [uso de la resolución de origen](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Creación de un perfil de transcodificación

Un *Perfil de transcodificación* describe el formato y la configuración que se usan para codificar el archivo de salida. El perfil de transcodificación contiene tres conjuntos de atributos:

-   Atributos de audio: describa el formato de audio de destino y la configuración del codificador de audio.
-   Atributos de vídeo: describe el formato de vídeo de destino y la configuración del codificador de vídeo.
-   Atributos de contenedor: defina el tipo de contenedor de archivos, así como algunos valores de codificación globales.

Para crear un perfil de transcodificación, llame a la función [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) . Esta función devuelve un puntero a la interfaz [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) . El objeto de perfil inicial está vacío; no contiene ningún atributo. El siguiente paso consiste en agregar los atributos que definen el perfil.

### <a name="audio-attributes"></a>Atributos de audio

Para agregar atributos para la secuencia de audio, llame a [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Estos atributos especifican cómo se codifica la secuencia de audio. Si el archivo de salida no va a contener una secuencia de audio, omita estos atributos.

Los atributos de audio se dividen en dos categorías:

-   Atributos que especifican el formato de la secuencia codificada
-   Atributos que especifican otros parámetros de codificación.

Los atributos de formato son simplemente atributos de tipo de medio, como se describe en la sección [tipos de medios de audio](audio-media-types.md). El conjunto exacto de atributos de formato depende del codificador. (Consulte [formatos de medios compatibles en Media Foundation](supported-media-formats-in-media-foundation.md)). Esta es una lista de los atributos de formato de audio típicos:



| Atributo de formato                                                                         | Descripción                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | Subtipo. Vea [GUID de subtipo de audio](audio-subtype-guids.md). |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | Número de canales de audio.                                    |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md)      | Número de muestras de audio por segundo.                          |
| [\_alineación del \_ bloque de audio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | La alineación del bloque.                                             |
| [\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | Número promedio de bytes por segundo (velocidad de bits codificada).   |



 

Se definen los siguientes parámetros de codificación.



| Parámetro Encoding                                                             | Descripción                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ Transcode \_ donot \_ Insertar \_ codificador](mf-transcode-donot-insert-encoder.md) | Impide que la API de Transcode Inserte un codificador para la secuencia de audio. |
| [\_ENCODINGPROFILE de TRANSCODIFICACIÓN MF \_](mf-transcode-encodingprofile.md)             | Especifica la plantilla de conformidad del dispositivo. (Sólo se aplica a archivos ASF).    |
| [\_QUALITYVSSPEED de TRANSCODIFICACIÓN MF \_](mf-transcode-qualityvsspeed.md)               | Especifica el equilibrio entre la calidad y la velocidad de codificación.                |



 

Debe establecer los atributos de formato. Los parámetros de codificación son opcionales.

Una manera de buscar un formato que sea compatible con el codificador es llamar a la función [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . El codificador deseado se especifica mediante el subtipo. La función devuelve una colección de tipos de medios para ese codificador. Puede seleccionar un tipo de la lista y copiar los atributos en el perfil. Para ver un ejemplo de código que usa este enfoque, vea [Tutorial: codificar un archivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Atributos de vídeo

Para agregar atributos para la secuencia de vídeo, llame a [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Estos atributos especifican cómo se codifica el flujo de vídeo. Si el archivo de salida no va a contener una secuencia de vídeo, omita estos atributos.

Al igual que con los atributos de audio, los atributos de vídeo se dividen en dos categorías:

-   Atributos que especifican el formato de la secuencia codificada
-   Atributos que especifican otros parámetros de codificación.

Los atributos de formato son atributos de tipo de medio, como se describe en la sección [tipos de medios de vídeo](video-media-types.md). Esta es una lista de los atributos de formato de vídeo típicos:



| Atributo de formato                                                       | Descripción                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                         | Subtipo. Vea [GUID de subtipo de vídeo](video-subtype-guids.md). |
| [\_velocidad de \_ fotogramas MF MT \_](mf-mt-frame-rate-attribute.md)                  | Velocidad de fotogramas.                                                  |
| [\_tamaño de \_ marco MF MT \_](mf-mt-frame-size-attribute.md)                  | Tamaño del marco.                                                  |
| [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)            | Velocidad de bits media.                                            |
| [\_relación de \_ aspecto de píxeles MF MT \_ \_](mf-mt-pixel-aspect-ratio-attribute.md) | La relación de aspecto de píxeles.                                          |



 

Se definen los siguientes parámetros de codificación.



| Parámetro Encoding                                                             | Descripción                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ Transcode \_ donot \_ Insertar \_ codificador](mf-transcode-donot-insert-encoder.md) | Impide que la API de Transcode Inserte un codificador para la secuencia de vídeo. |
| [\_ENCODINGPROFILE de TRANSCODIFICACIÓN MF \_](mf-transcode-encodingprofile.md)             | Especifica la plantilla de conformidad del dispositivo. (Sólo se aplica a archivos ASF).    |
| [\_QUALITYVSSPEED de TRANSCODIFICACIÓN MF \_](mf-transcode-qualityvsspeed.md)               | Especifica el equilibrio entre la calidad y la velocidad de codificación.                |



 

Debe establecer los atributos de formato. Los parámetros de codificación son opcionales.

### <a name="container-attributes"></a>Atributos de contenedor

Los atributos de contenedor definen las características de nivel de archivo del archivo de salida. Para establecer atributos de contenedor, llame a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Se definen los siguientes atributos.



| Atributo                                                                          | Descripción                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Perfil de ajuste de TRANScodificación de MF \_ \_](mf-transcode-adjust-profile.md)                  | Define la configuración de la secuencia que se va a utilizar para la topología de transcodificación. Puede establecer las marcas para usar la configuración de origen de entrada o usar atributos de secuencia personalizados. |
| [\_CONTAINERTYPE de TRANSCODIFICACIÓN MF \_](mf-transcode-containertype.md)                     | Especifica el formato de archivo del archivo de salida, como MP4 o ASF. En función de este valor, se agrega el receptor de medios adecuado a la topología.            |
| [\_REcodificar \_ omitir \_ transferencia de metadatos \_](mf-transcode-skip-metadata-transfer.md) | Especifica si los metadatos del origen se copian en el archivo de salida.                                                                               |
| [\_TOPOLOGYMODE de TRANSCODIFICACIÓN MF \_](mf-transcode-topologymode.md)                       | Especifica si los códecs basados en hardware se pueden usar durante la transcodificación.                                                                                |
| [\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_](mft-fieldofuse-unlock-attribute.md)          | Desbloquea un códec que tiene restricciones de campo de uso. Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md).              |



 

El atributo [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) es obligatorio. Los demás atributos de contenedor son opcionales.

## <a name="creating-a-transcode-topology"></a>Creación de una topología de transcodificación

La topología de transcodificación es una topología parcial que contiene el origen de medios, los códecs adecuados y el receptor de medios. Para crear la topología de transcodificación, llame a la función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) . Esta función toma los siguientes parámetros como entrada:

-   Puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.
-   Nombre del archivo de salida.
-   Puntero a la interfaz [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) del perfil de transcodificación.

La función devuelve un puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .

## <a name="running-the-encoding-session"></a>Ejecutar la sesión de codificación

Después de crear la topología, está listo para codificar el archivo. Puede descartar el perfil en este momento.

1.  Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear la sesión multimedia.
2.  Llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.
3.  Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la sesión de codificación.
4.  Espere el evento [MESessionEnded](mesessionended.md) .
5.  Llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.
6.  Espere el evento [MESessionClosed](mesessionclosed.md) .
7.  Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

La mayor parte del tiempo empleado en la codificación se produce entre los pasos 3 y 4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de transcodificación](transcode-api.md)
</dt> <dt>

[Acerca de la sesión multimedia](about-the-media-session.md)
</dt> </dl>

 

 



