---
description: El receptor de archivos MPEG-4 crea archivos MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Receptor de archivos MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e0175a5c21cc9f7c0186f70b37a5f94f5bf12151e606a2a441b4c75919d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102115"
---
# <a name="mpeg-4-file-sink"></a>Receptor de archivos MPEG-4

El receptor de archivos MPEG-4 crea archivos MP4. Para obtener más información sobre el formato de archivo MP4, consulte los siguientes documentos de estándar:

-   ISO/IEC 14496-12: Tecnología de la información: codificación de objetos audio visuales -- *Parte 12: Formato* de archivo multimedia base ISO
-   ISO/IEC 14496-14: Tecnología de la información: codificación de *objetos audio visuales -- Parte 14: Formato* de archivo MP4

> [!Note]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

 

El receptor de archivos MPEG-4 no encapsula la funcionalidad de codificación.

Para crear el receptor de archivos MPEG-4, llame a la [**función MFCreateMPEG4MediaSink.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) El receptor de archivos MPEG-4 expone las interfaces siguientes a través **de QueryInterface**:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>Cuadro de descripción de ejemplo

MP4 es un formato de contenedor extensible. La especificación MP4 no define una estructura fija para describir los tipos de medios en un contenedor MP4. En su lugar, define una jerarquía de objetos que permite definir estructuras personalizadas para cada formato. La descripción del formato se almacena en el cuadro de descripción de ejemplo ('stsd') para cada secuencia. El cuadro de descripción del ejemplo contiene una lista de entradas de ejemplo. Para cada entrada de ejemplo, un código de 4 bytes, similar a fourcc, define la estructura de formato.

El receptor de archivos MPEG-4 puede generar el cuadro de descripción de ejemplo para los siguientes formatos:

-   Vídeo de H.264/AVC
-   Audio de AAC
-   Audio MP3

Para otros formatos, el cuadro de descripción de ejemplo debe proporcionarse en el tipo de medio para cada secuencia. Para especificar el cuadro de descripción de ejemplo, establezca los siguientes atributos en el tipo de medio:



| Atributo                                                                     | Descripción                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DESCRIPCIÓN \_ DEL \_ EJEMPLO MPEG4 \_ DE \_ MF MT](mf-mt-mpeg4-sample-description.md)      | Contiene el cuadro de descripción de ejemplo como un blob binario.                                                                                                         |
| [ENTRADA \_ DE EJEMPLO ACTUAL DE MF MT \_ MPEG4 \_ \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Especifica cuál de las entradas de ejemplo del cuadro de descripción del ejemplo está activa actualmente. (Opcional).<br/> Actualmente, el valor debe ser cero.<br/> |



 

En algunos casos, no es posible generar un cuadro de descripción de ejemplo hasta que se hayan codificado todos los datos. Por ejemplo, es posible que la información como la velocidad de bits media no se conozca con antelación. En ese caso, puede actualizar el tipo de medio mediante la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en el receptor de archivos MPEG-4. Esto debe hacerse antes de que se haya finalizado el receptor de medios.

Normalmente, un codificador ascendente crea el tipo de medio. El codificador puede generar un nuevo tipo de medio durante el streaming, a través de un cambio de formato dinámico. Para obtener más información, vea [Cambios de formato dinámico.](basic-mft-processing-model.md)

## <a name="h264avc-video"></a>Vídeo de H.264/AVC

El receptor de archivos MPEG-4 admite la versión de la secuencia de AVC que tiene una secuencia de vídeo elemental, con el conjunto de parámetros de secuencia (SPS) y las NALU de parámetro de imagen (PPS) contenidas en el cuadro de descripción de ejemplo, tal como se define en iso/IEC 14496, sección 15, sección 5.1. El receptor de archivos no admite el método alternativo para almacenar NALU de SPS/PPS como una secuencia elemental independiente del conjunto de parámetros.

El receptor de archivos MPEG-4 puede generar el cuadro de descripción de ejemplo, pero debe proporcionarse con las NALU de SPS y PPS. Especifique esta información en el tipo de medio estableciendo el atributo [**MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) El valor del atributo es el encabezado de secuencia H.264. El encabezado de secuencia debe constar de las NALUs de SPS y PPS delimitadas por códigos de inicio de 3 o 4 bytes.

Opcionalmente, al configurar el receptor de archivos, puede omitir el atributo [**MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER**](mf-mt-mpeg-sequence-header-attribute.md) del tipo de medio inicial. En ese caso, debe actualizar el tipo de medio más adelante para incluir el encabezado de secuencia.

El receptor de archivos MPEG-4 tiene los siguientes requisitos para las secuencias de bits de AVC:

-   La secuencia de bits debe cumplir la especificación de formato H.264 del anexo B. En concreto, las NALUs deben delimitarse con códigos de inicio de 3 o 4 bytes.
-   Los ejemplos de medios deben contener todas las NALUs de datos y segmentos que corresponden a un único tiempo de presentación.
-   Al escribir fotogramas B en un archivo MP4, debe establecer tanto la marca de tiempo de presentación como la marca de tiempo de descodificación. Si la secuencia tiene un marco B y la marca de tiempo de descodificación no está establecida, el escritor mp4 verá el tiempo del fotograma hacia atrás y quitará el fotograma. 

## <a name="aac-audio"></a>Audio AAC

Para el audio de AAC, el receptor de archivos MPEG-4 puede generar el cuadro de descripción de ejemplo para los subtipos siguientes:

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ RAW \_ AAC1**

Para obtener más información sobre estos subtipos, vea [Tipos de medios de AAC](aac-media-types.md).

Para el **subtipo MFAudioFormat \_ AAC,** el tipo de medio contiene opcionalmente el atributo [**MF MT USER \_ \_ \_ DATA.**](mf-mt-user-data-attribute.md) Si está presente, este atributo es la parte de la estructura [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece después de la estructura **DESACWAVEATEX** (es decir, después del **miembro wfx).** Esto va seguido de los datos AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3. Si el atributo **MF \_ MT USER \_ \_ DATA** no está presente, se supone que la secuencia es un perfil de baja complejidad (LC) de AAC y el receptor de archivos MPEG-4 genera un cuadro de descripción de ejemplo adecuado.

Para el subtipo **\_ MEDIASUBTYPE RAW \_ AAC1,** el receptor multimedia debe contener el atributo [**MF MT USER \_ \_ \_ DATA**](mf-mt-user-data-attribute.md) y el atributo debe contener los datos AudioSpecificConfig().

El receptor de archivos MPEG-4 crea la variante MPEG-4 del cuadro de descripción del ejemplo de AAC, mediante una entrada de ejemplo "mp4a" con objectTypeIndication = 0x40. No usa tipos de objetos MPEG-2.

## <a name="mp3-audio"></a>MP3 Audio

En el caso del audio MP3, el receptor de archivos MPEG-4 puede generar el cuadro de descripción de ejemplo a partir de un tipo de medio de audio estándar. (Vea [Tipos de medios de audio).](audio-media-types.md)

El receptor de archivos MPEG-4 crea la variante MPEG-4 del cuadro de descripción del ejemplo MP3, mediante una entrada de ejemplo "mp4a" con objectTypeIndication = 0x6b para audio MPEG-1.

## <a name="limitations"></a>Limitaciones

-   El tamaño máximo del archivo escrito es de 4 GB. En Windows 8, se admiten archivos de más de 4 GB.
-   El receptor de archivos MPEG-4 no admite listas de edición (cuadros "edts" y "elst").

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 actualizaciones del receptor y el origen MPEG-4

-   Se ha agregado compatibilidad de lectura y escritura de rotación Windows 8 origen y receptor MPEG-4. Esto no se admite en el receptor Windows 7 MPEG-4.

    El origen MPEG-4 lee el ángulo de rotación de una pista de vídeo activa como la suma del ángulo de rotación de "mvhd" y de "tkhd".

    El receptor MPEG-4 de Microsoft escribe el ángulo de rotación en "tkhd", pero escribe matriz de 0 grados (identidad) en "mvhd". Tenga en cuenta que el receptor MPEG-4 de Microsoft solo admite una sola pista de vídeo.

    IPropertyStore lee el ángulo de rotación solo para la primera pista de vídeo como la suma del ángulo de rotación de "mvhd" y de "tkhd".

    IPropertyStore escribe el ángulo de rotación solo para la primera pista de vídeo en "tkhd" después de ajustar el ángulo de rotación según el ángulo de rotación en "mvhd", si existe.

-   Los fragmentos de película ('moof') se admiten en Windows 8 origen y receptor MPEG-4, pero 'mfra' no lo es.
-   H.263 se admite en Windows 8 origen MPEG-4.

    El origen MPEG-4 ahora asigna dos cuatrocc de "h263" y "s263" en formato de archivo MPEG-4 al tipo de medio **MFVideoFormat \_ H263.**

-   Se ha agregado más compatibilidad con fourcc para MGCEG Windows 8 origen MPEG-4.

    El origen MPEG-4 asigna foucc de 'dmb1' al tipo de medio **de MFVideoFormat \_ MJPG.**

-   Se ha agregado compatibilidad con metadatos de Furigana Windows 8 origen MPEG-4.

    El origen MPEG-4 lee los metadatos de Furigana de "soal", "soar", "soaa", "sonm" y "soco". IPropertyStore lee los metadatos de Furignana a través del conjunto de PKEYs correspondientes.

    En la tabla siguiente se muestra la asignación entre el nombre canónico del shell, la clave de propiedad y el identificador de cuadro o etiqueta en formato de archivo MPEG-4.

    

    | Campo                                | Clave de propiedad                         | Id. de etiqueta/cuadro |
    |--------------------------------------|--------------------------------------|------------|
    | Sistema. Música. AlbumTitleSortOverride  | PKEY \_ Música \_ AlbumTitleSortOverride  | soal       |
    | Sistema. Música. ArtistSortOverride      | PKEY \_ Música \_ ArtistSortOverride      | elevarse       |
    | Sistema. Música. AlbumArtistSortOverride | PKEY \_ Música \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | Sistema. Música. ComposerSortOverride    | PKEY \_ Música \_ ComposerSortOverride    | Soco       |

    

     

-   Se ha agregado compatibilidad con atomes 3D estéreo Windows 8 origen MPEG-4.

-   Compatibilidad con AC3 y DD+ agregada en Windows 8 origen y receptor MPEG-4.
-   Los archivos de más de 4 GB se admiten Windows 8 receptor MPEG-4 para MP4 no fragmentado.
-   La limpieza se ha optimizado en Windows 8 origen MPEG-4.

    Para reducir la latencia, la información de los dos fotogramas clave más cercanos para una posición de búsqueda determinada se expone a través de [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Dado que el fotograma clave no tiene fotogramas dependientes, presenta el fotograma después de descodar solo un fotograma. Use [**IMFGetService::GetService para**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) obtener esta interfaz a través del origen de medios, la canalización o la aplicación.

    Establezca la velocidad en cero en el origen MPEG-4. Cuando la canalización está en modo de limpieza, la velocidad es cero.

-   SPS y PPS se pueden almacenar en datos de ejemplo en el receptor MPEG-4.

    [MF \_ El atributo \_ \_ PASSTHROUGH MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) en el receptor MPEG-4 se define para permitir que sps y PPS se guarden junto con ejemplos de entrada (datos de vídeo H.264). Los clips mp4 producidos pueden reproducirse mediante Windows 7 MPEG-4 y otros.

-   SPS y PPS se pueden extraer de ejemplos de entrada en el receptor MPEG-4.

    Cuando SPS y PPS no se establecen a través de [MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) en el tipo de medio de entrada del receptor MPEG-4, el receptor MPEG-4 intentará extraer SPS y PPS de los ejemplos de entrada. El receptor MPEG-4 omite los ejemplos de entrada hasta que encuentra el primer SPS y PPS, porque todos los ejemplos de entrada sin SPS y PPS no pueden descodificarse.

-   La información 3D en el registro de configuración de AVC es compatible con MP4 no fragmentado.
-   La longitud de NALU se expone para las muestras comprimidas H.264 con el fin de optimizar la decodificación de DXVA de H.264 VLD.

    El origen MPEG-4 establece [MF \_ NALU \_ LENGTH SET \_ en](mf-nalu-length-set.md) el tipo de medio de salida **MFVideoFormat \_ H264** o **MFVideoFormat \_ h264**. Establece el blob de [MF \_ NALU \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) en cada muestra de salida, con una longitud de NALU de cuatro bytes para diferentes NALU en una muestra comprimida.

-   Se ha agregado compatibilidad con audio MPEG2 ADTS en el origen MP4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Orígenes multimedia y receptores](media-sources-and-sinks.md)
</dt> <dt>

[Receptores de medios](media-sinks.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
