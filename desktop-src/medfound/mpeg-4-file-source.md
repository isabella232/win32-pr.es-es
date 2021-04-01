---
description: El origen de archivo MPEG-4 analiza los archivos MP4 y 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Origen de archivo MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275838"
---
# <a name="mpeg-4-file-source"></a>Origen de archivo MPEG-4

El origen de archivo MPEG-4 analiza los archivos MP4 y 3GPP. Para obtener más información sobre el formato de archivo MP4, consulte los siguientes documentos de estándares:

-   ISO/IEC 14496-12: *tecnología de la información: codificación de objetos visuales de audio, parte 12: formato de archivo multimedia básico ISO*
-   ISO/IEC 14496-14: *tecnología de la información: codificación de objetos visuales de audio, parte 14: formato de archivo MP4*

> [!Note]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

 

El origen de archivo MPEG-4 no descodifica los datos de audio y vídeo del archivo.

Este tema contiene las siguientes secciones:

## <a name="file-extensions-and-mime-types"></a>Extensiones de archivo y tipos MIME

El origen de archivo MPEG-4 es el origen de medios predeterminado para las siguientes extensiones de nombre de archivo.



| Extensión de archivo | Descripción           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | Audio MPEG-4          |
| .m4v           | Vídeo MPEG-4          |
| .mov           | Apple QuickTime película |
| .mp4           | Audio o vídeo MPEG-4 |
| .mp4v          | Vídeo MPEG-4          |



 

También es el origen de medios predeterminado para los siguientes tipos MIME.



| Tipo de MIME   | Descripción  |
|-------------|--------------|
| audio/3GPP  | audio 3GPP   |
| audio/3GPP2 | audio 3GPP2  |
| audio/MP4   | Audio MPEG-4 |
| vídeo/3GPP  | vídeo de 3GPP   |
| vídeo y 3GPP2 | vídeo de 3GPP2  |
| vídeo/MP4   | Vídeo MPEG-4 |



 

## <a name="media-types"></a>Tipos de medios

MP4 es un formato de contenedor extensible. La especificación MP4 no define una estructura fija para describir los tipos de medios en un contenedor MP4. En su lugar, define una jerarquía de objetos que permite definir estructuras personalizadas para cada formato. La descripción del formato se almacena en el cuadro Descripción del ejemplo (' stsd ') de la secuencia. El cuadro Descripción del ejemplo contiene una lista de entradas de ejemplo. Para cada entrada de ejemplo, un código de 4 bytes, similar a un FOURCC, define la estructura de formato.

Esta extensibilidad significa que el origen de archivo MPEG-4 no puede reconocer todas las descripciones de formato posibles. En su lugar, adopta un enfoque de dos niveles al crear tipos de medios para las secuencias. Como mínimo, cada tipo de medio contiene los siguientes atributos.



| Atributo                                                                     | Descripción                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                     | Igual a **MFMediaType \_ Audio** o **MFMediaType \_ video**.     |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                            | Especifica el subtipo de flujo.                                  |
| [\_Descripción del \_ ejemplo de MPEG4 MT \_ de MF \_](mf-mt-mpeg4-sample-description.md)      | Contiene el cuadro de Descripción del ejemplo completo como un BLOB binario. |
| [\_Entrada de \_ \_ ejemplo actual \_ MPEG4 \_ de MF MT](mf-mt-mpeg4-current-sample-entry.md) | Especifica la entrada actual en el cuadro Descripción del ejemplo.     |



 

El origen de archivo MPEG-4 reconoce algunos tipos de entrada de ejemplo. Para estas entradas, puede analizar la estructura de formato y crear un tipo de medio completo, con atributos adicionales que describen los detalles del formato. Consulte [atributos de tipo de medio](media-type-attributes.md).

El origen de archivo MPEG-4 puede analizar las siguientes entradas de ejemplo.



| Código de entrada de ejemplo | Tipo principal | Subtype                                                               | Descripción                                         | Notas                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alaw            | Audio      | **formato de onda \_ \_ Alaw**                                                | Código de una ley                                        |                                                                                                                                                                                                  |
| ficheros            | Vídeo      | **MFVideoFormat \_ MJPG**                                               | Secuencia Photo-JPEG                                   | El formato de contenedor de QuickTime también admite secuencias JPEG de movimiento con las entradas ' mjpa ' o ' mjpb ', pero el origen de archivo MPEG-4 no proporciona un tipo de medio completo para esos tipos.               |
| 'avc1'            | Vídeo      | **MFVideoFormat \_ H264**                                               | Vídeo H. 264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **\_Mp3 MFAudioFormat**<br/>   | AAC o MP3                                          | La entrada ' mp4a ' puede describir otros formatos de audio MPEG, pero el origen de archivo MPEG-4 no analiza la estructura de formato.                                                                          |
| MP4V            | Vídeo      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG-4, parte 2                                       | **MFVideoFormat \_ M4S2** se usa para el perfil simple MPEG-4 parte 2.<br/> **MFVideoFormat \_ MP4V** se usa para todos los demás perfiles MPEG-4 parte 2, incluido el perfil simple avanzado.<br/> |
| Socket            | Audio      | **MFAudioFormat \_ PCM**                                                | audio PCM de 8 bits                                     |                                                                                                                                                                                                  |
| 'sowt'            | Audio      | **MFAudioFormat \_ PCM**                                                | audio PCM Little-Endian de 16 bits                      |                                                                                                                                                                                                  |
| pares            | Audio      | **MFAudioFormat \_ PCM**                                                | audio PCM Big-Endian de 16 bits                         | El origen de archivo MPEG-4 convierte los datos de audio al formato Little-Endian.                                                                                                                          |
| ULAW            | Audio      | **formato de onda \_ \_ MULAW**                                               | μ-código de ley                                        |                                                                                                                                                                                                  |
| ' VC-1 '            | Vídeo      | **MFVideoFormat \_ Wvc1**                                               | Vídeo VC-1                                          |                                                                                                                                                                                                  |
| NINGUNA            | Audio      | **MFAudioFormat \_ PCM**                                                | audio PCM Big-Endian de 8 o 16 bits                | El origen de archivo MPEG-4 convierte los datos de audio al formato Little-Endian.                                                                                                                          |
| 0x00000000        | Audio      | **MFAudioFormat \_ PCM**                                                | audio PCM Big-Endian de 8 o 16 bits                | El origen de archivo MPEG-4 convierte los datos de audio al formato Little-Endian.                                                                                                                          |
| 0x6d730002        | Audio      | **formato de onda \_ \_ ADPCM**                                               | Modulación de código de impulso diferencial adaptable (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **formato de onda \_ \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

Para cualquier otro código que no se muestre en la tabla anterior, el origen de archivo MPEG-4 establece el subtipo como se indica a continuación:

1.  *SubType* = base de MFMPEG4Format \_
2.  *subtipo*. Data1 = código de entrada de ejemplo

En el caso de los códigos que no se muestran en la tabla, un descodificador debe utilizar el atributo de [ \_ Descripción del ejemplo MF MT \_ MPEG4 \_ \_ ](mf-mt-mpeg4-sample-description.md) para analizar el cuadro Descripción del ejemplo.

Para obtener una lista de códigos de entrada de ejemplo y vínculos a especificaciones relevantes, consulte el sitio web de la [autoridad de registro ' MP4 '](https://mp4ra.org) .

## <a name="limitations"></a>Limitaciones

El origen de archivo MPEG-4 no admite las siguientes características de archivos MP4:

-   Pistas externas.
-   Fragmentos de película (cuadros ' moof ' o ' mfra '). ' moof ' es compatible con Windows 8.
-   Presentaciones transmitidas por secuencias. El origen de archivo MPEG-4 omite silenciosamente las pistas de sugerencias.
-   Búsqueda por código de tiempo SMPTE.
-   Átomos comprimidos (' CMOV ').

Solo se admiten secuencias de vídeo y audio. Cualquier pista que contenga otros tipos de flujo se omite en modo silencioso. Los datos multimedia deben colocarse dentro de los átomos ' mdat '.

Si está instalado el complemento de actualización de plataforma para Windows Vista, el origen de archivo MPEG-4 está disponible en Windows Vista, pero solo se puede acceder a él en Windows Vista mediante el [lector de origen](source-reader.md).

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Actualizaciones de Windows 8 para el origen y el receptor MPEG-4

-   Compatibilidad de lectura y escritura de rotación agregada en el origen y el receptor de MPEG-4 de Windows 8. Esto no se admite en el origen y el receptor MPEG-4 de Windows 7.

    El origen MPEG-4 Lee el ángulo de rotación de una pista de vídeo activa como la suma del ángulo de rotación de ' mvhd ' y de ' tkhd '.

    El receptor MPEG-4 de Microsoft escribe el ángulo de rotación en ' tkhd ' pero escribe una matriz de 0 grados (identidad) en ' mvhd '. Tenga en cuenta que el receptor MPEG-4 de Microsoft solo admite una pista de vídeo.

    IPropertyStore lee el ángulo de rotación solo para la primera pista de vídeo como la suma del ángulo de rotación de ' mvhd ' y de ' tkhd '.

    IPropertyStore escribe el ángulo de rotación solo para la primera pista de vídeo de ' tkhd ' después de ajustar el ángulo de giro según el ángulo de rotación en ' mvhd ', si existe.

-   Los fragmentos de película (' moof ') se admiten en el origen y el receptor de MPEG-4 de Windows 8, pero no en ' mfra '.
-   H. 263 es compatible con el origen de MPEG-4 de Windows 8.

    Ahora, el origen MPEG-4 asigna dos tipos de elemento ' H263 ' y 263 ' en formato de archivo MPEG-4 al tipo de medio de **MFVideoFormat \_ H263**.

-   Se agregó más compatibilidad con FourCC para MJPEG en el origen MPEG-4 de Windows 8.

    Los mapas de origen MPEG-4 foucc de ' dmb1 ' al tipo de medio de **MFVideoFormat \_ MJPG**.

-   Compatibilidad con metadatos furigana agregada en el origen de MPEG-4 de Windows 8.

    El origen MPEG-4 Lee los metadatos furigana de ' Soal ', ' vertiginosa ', ' SOAA ', ' SONM ' y ' Soco '. IPropertyStore Lee los metadatos de Furignana a través del conjunto de PKEYs correspondiente.

    En la tabla siguiente se muestra la asignación entre el nombre canónico del shell, la clave de la propiedad y el identificador de cuadro/etiqueta en formato de archivo MPEG-4.

    

    | Campo                                | Clave de propiedad                         | IDENTIFICADOR de etiqueta/cuadro |
    |--------------------------------------|--------------------------------------|------------|
    | System. Music. AlbumTitleSortOverride  | PKEY \_ Music \_ AlbumTitleSortOverride  | soal       |
    | System. Music. ArtistSortOverride      | PKEY \_ Music \_ ArtistSortOverride      | soar       |
    | System. Music. AlbumArtistSortOverride | PKEY \_ Music \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | System. Music. ComposerSortOverride    | PKEY \_ Music \_ ComposerSortOverride    | soco       |

    

     

-   Compatibilidad con Atom 3D estéreo agregada en el origen de MPEG-4 de Windows 8.

-   Compatibilidad con AC3 y DD + agregada en el origen y el receptor de MPEG-4 de Windows 8.
-   Los archivos de más de 4 gigabytes (GB) se admiten en el receptor MPEG-4 de Windows 8 para MP4 no fragmentado.
-   La limpieza se ha optimizado en el origen MPEG-4 de Windows 8.

    Para reducir la latencia, la información de los dos fotogramas clave más cercanos para una determinada posición de búsqueda se expone a través de [**IMFSeekInfo:: GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Dado que el fotograma clave no tiene fotogramas dependientes, presenta el marco tras descodificar un solo fotograma. Use [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener esta interfaz a través del origen de medios, la canalización o la aplicación.

    Establezca velocidad en cero en el origen MPEG-4. Cuando la canalización está en modo de limpieza, la velocidad es cero.

-   SPS y PPS se pueden almacenar en los datos de ejemplo del receptor MPEG-4.

    [MF \_ El atributo MPEG4SINK \_ SPSPPS \_ PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) del receptor MPEG-4 se define para permitir que los SPs y el PPC se guarden junto con los ejemplos de entrada (datos de vídeo H. 264). Los clips MP4 producidos se pueden reproducir con el origen de MPEG-4 de Windows 7 y otros.

-   SPS y PPS se pueden extraer de los ejemplos de entrada del receptor MPEG-4.

    Cuando SPS y PPS no se establecen mediante [el \_ \_ encabezado de \_ secuencia \_ MF MT MPEG](mf-mt-mpeg-sequence-header-attribute.md) en el tipo de medio de entrada del receptor MPEG-4, el receptor MPEG-4 intentará extraer los SPs y PPS de los ejemplos de entrada. El receptor MPEG-4 omite cualquier ejemplo de entrada hasta que encuentra el primer SPS y PPS, ya que todos los ejemplos de entrada sin SPS y PPS no se pueden descodificar.

-   la información 3D en el registro de configuración de AVC es compatible con MP4 no fragmentado.
-   La longitud de NALU se expone para los ejemplos comprimidos H. 264 para optimizar la descodificación de H. 264 VLD DXVA.

    Los conjuntos de orígenes de MPEG-4 [MF \_ Nalu de \_ longitud \_ establecida](mf-nalu-length-set.md) en el tipo de medio de salida de **MFVideoFormat \_ H264** o **MFVideoFormat \_ H264**. Establece el BLOB de [información de \_ \_ longitud \_ de MF Nalu](mf-nalu-length-information.md) en cada ejemplo de salida, con una longitud de Nalu de cuatro BYTEs para los distintos Nalu de un ejemplo comprimido.

-   Compatibilidad agregada para MPEG2 ADTS audio en el origen MP4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes y receptores de medios](media-sources-and-sinks.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




