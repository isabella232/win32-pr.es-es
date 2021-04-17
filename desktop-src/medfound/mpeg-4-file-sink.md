---
description: El receptor de archivos MPEG-4 crea archivos MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Receptor de archivos MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105653117"
---
# <a name="mpeg-4-file-sink"></a>Receptor de archivos MPEG-4

El receptor de archivos MPEG-4 crea archivos MP4. Para obtener más información sobre el formato de archivo MP4, consulte los siguientes documentos de estándares:

-   ISO/IEC 14496-12: *tecnología de la información: codificación de objetos visuales de audio, parte 12: formato de archivo multimedia básico ISO*
-   ISO/IEC 14496-14: *tecnología de la información: codificación de objetos visuales de audio, parte 14: formato de archivo MP4*

> [!Note]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

 

El receptor de archivos MPEG-4 no encapsula la funcionalidad de codificación.

Para crear el receptor de archivos MPEG-4, llame a la función [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) . El receptor de archivos MPEG-4 expone las siguientes interfaces a través de **QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Cuadro de Descripción del ejemplo

MP4 es un formato de contenedor extensible. La especificación MP4 no define una estructura fija para describir los tipos de medios en un contenedor MP4. En su lugar, define una jerarquía de objetos que permite definir estructuras personalizadas para cada formato. La descripción del formato se almacena en el cuadro Descripción del ejemplo (' stsd ') para cada flujo. El cuadro Descripción del ejemplo contiene una lista de entradas de ejemplo. Para cada entrada de ejemplo, un código de 4 bytes, similar a un FOURCC, define la estructura de formato.

El receptor de archivos MPEG-4 puede generar el cuadro de Descripción del ejemplo para los siguientes formatos:

-   Vídeo H. 264/AVC
-   Audio AAC
-   Audio MP3

Para otros formatos, el cuadro Descripción del ejemplo debe proporcionarse en el tipo de medio para cada flujo. Para especificar el cuadro Descripción del ejemplo, establezca los siguientes atributos en el tipo de medio:



| Atributo                                                                     | Descripción                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Descripción del \_ ejemplo de MPEG4 MT \_ de MF \_](mf-mt-mpeg4-sample-description.md)      | Contiene el cuadro de Descripción del ejemplo como un BLOB binario.                                                                                                         |
| [\_Entrada de \_ \_ ejemplo actual \_ MPEG4 \_ de MF MT](mf-mt-mpeg4-current-sample-entry.md) | Especifica cuál de las entradas de ejemplo en el cuadro Descripción del ejemplo está activa actualmente. (Opcional).<br/> Actualmente, el valor debe ser cero.<br/> |



 

En algunos casos, no es posible generar un cuadro de descripción de ejemplo hasta que todos los datos se hayan codificado. Por ejemplo, la información como la velocidad de bits media podría no conocerse con anterioridad. En ese caso, puede actualizar el tipo de medio mediante la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en el receptor de archivos MPEG-4. Esto debe hacerse antes de finalizar el receptor de medios.

Normalmente, el tipo de medio lo crea un codificador de nivel superior. El codificador puede generar un nuevo tipo de medio durante el streaming, a través de un cambio de formato dinámico. Para obtener más información, consulte [Dynamic Format Changes](basic-mft-processing-model.md).

## <a name="h264avc-video"></a>Vídeo H. 264/AVC

El receptor de archivos MPEG-4 admite la versión de la secuencia AVC que tiene una secuencia de vídeo elemental, con el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs contenidos en el cuadro Descripción del ejemplo, como se define en la sección 5,1 de ISO/IEC 14496. El receptor de archivos no admite el método alternativo para almacenar SP/PPS NALUs como una secuencia elemental de conjunto de parámetros independiente.

El receptor de archivos MPEG-4 puede generar el cuadro Descripción del ejemplo, pero debe proporcionarse con los SPS y el NALUs de PPS. Especifique esta información en el tipo de medio estableciendo el atributo de [**\_ encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) . El valor del atributo es el encabezado de secuencia H. 264. El encabezado de secuencia debe constar de los SPS y el NALUs de PPS delimitados por códigos de inicio de 3 bytes o de 4 bytes.

Opcionalmente, al configurar el receptor de archivos, puede omitir el atributo de [**\_ encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) del tipo de medio inicial. En ese caso, debe actualizar el tipo de medio más adelante para incluir el encabezado de secuencia.

El receptor de archivos MPEG-4 tiene los siguientes requisitos para AVC bitstreams:

-   Fragmentada debe ajustarse a la especificación de formato H. 264 Annex B. En concreto, NALUs debe delimitarse con códigos de inicio de 3 o 4 bytes.
-   Los ejemplos de medios deben contener todos los NALUs de segmentos y datos que correspondan a un único tiempo de presentación.
-   Al escribir fotogramas B en un archivo MP4, debe establecer la marca de tiempo de presentación y la marca de tiempo de descodificación. Si Stream tiene un fotograma B y no se establece la marca de tiempo de descodificación, el escritor MP4 verá que la hora del fotograma va hacia atrás y quitará el marco. 

## <a name="aac-audio"></a>Audio AAC

En el caso del audio AAC, el receptor de archivos MPEG-4 puede generar el cuadro de Descripción del ejemplo para los siguientes subtipos:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ raw \_ AAC1**

Para obtener más información acerca de estos substypes, consulte [tipos de medios AAC](aac-media-types.md).

En el caso del subtipo **\_ AAC MFAudioFormat** , el tipo de medio contiene opcionalmente el atributo de [**\_ datos del \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) . Si está presente, este atributo es la parte de la estructura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece después de la estructura **WAVEFORMATEX** (es decir, después del miembro de **WFX** ). A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3. Si no está presente el atributo de **\_ datos de \_ usuario \_ de MF MT** , se supone que el perfil de la secuencia es el perfil de la baja complejidad AAC (LC) y el receptor de archivos MPEG-4 genera un cuadro de descripción de ejemplo adecuado.

En el caso del subtipo **MEDIASUBTYPE \_ raw \_ AAC1** , el receptor de medios debe contener el atributo de [**\_ datos de \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) y el atributo debe contener los datos AudioSpecificConfig ().

El receptor de archivos MPEG-4 crea la variante MPEG-4 del cuadro de Descripción del ejemplo AAC, utilizando una entrada de ejemplo "mp4a" con objectTypeIndication = 0x40. No usa tipos de objeto MPEG-2.

## <a name="mp3-audio"></a>Audio MP3

En el caso de audio MP3, el receptor de archivos MPEG-4 puede generar el cuadro Descripción de ejemplo a partir de un tipo de medio de audio estándar. (Consulte [tipos de medios de audio](audio-media-types.md)).

El receptor de archivos MPEG-4 crea la variante MPEG-4 del cuadro de Descripción del ejemplo MP3, con una entrada de ejemplo "mp4a" con objectTypeIndication = 0x6b para audio MPEG-1.

## <a name="limitations"></a>Limitaciones

-   El tamaño máximo del archivo creado es 4 GB. En Windows 8, se admiten archivos de más de 4 GBGB.
-   El receptor de archivos MPEG-4 no admite listas de edición (cuadros "EDtS" y "Elst").

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
-   Los archivos de más de 4 GB se admiten en el receptor MPEG-4 de Windows 8 para MP4 no fragmentado.
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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Orígenes y receptores de medios](media-sources-and-sinks.md)
</dt> <dt>

[Receptores de medios](media-sinks.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
