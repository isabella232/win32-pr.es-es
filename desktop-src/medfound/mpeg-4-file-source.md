---
description: El origen del archivo MPEG-4 analiza los archivos MP4 y 3GPP.
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: Origen de archivo MPEG-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece07ec0f2a2d94b477335e885f11c0d36769bffd11002ba464cec1d9c6ffb21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848055"
---
# <a name="mpeg-4-file-source"></a>Origen de archivo MPEG-4

El origen del archivo MPEG-4 analiza los archivos MP4 y 3GPP. Para obtener más información sobre el formato de archivo MP4, consulte los siguientes documentos de estándar:

-   ISO/IEC 14496-12: Tecnología de la información: codificación de objetos audio visuales -- *Parte 12: Formato* de archivo multimedia base ISO
-   ISO/IEC 14496-14: Tecnología de la información: codificación de *objetos audio visuales -- Parte 14: Formato* de archivo MP4

> [!Note]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

 

El origen de archivo MPEG-4 no descodifica los datos de audio y vídeo del archivo.

Este tema contiene las siguientes secciones:

## <a name="file-extensions-and-mime-types"></a>Extensiones de archivo y tipos MIME

El origen de archivo MPEG-4 es el origen multimedia predeterminado para las siguientes extensiones de nombre de archivo.



| Extensión de archivo | Descripción           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | Audio MPEG-4          |
| .m4v           | Vídeo MPEG-4          |
| .mov           | Apple QuickTime Movie |
| .mp4           | Audio o vídeo MPEG-4 |
| .mp4v          | Vídeo MPEG-4          |



 

También es el origen multimedia predeterminado para los siguientes tipos MIME.



| Tipo de MIME   | Descripción  |
|-------------|--------------|
| audio/3gpp  | Audio 3GPP   |
| audio/3gpp2 | Audio 3GPP2  |
| audio/mp4   | Audio MPEG-4 |
| video/3gpp  | Vídeo de 3GPP   |
| video/3gpp2 | Vídeo de 3GPP2  |
| video/mp4   | Vídeo MPEG-4 |



 

## <a name="media-types"></a>Tipos de medios

MP4 es un formato de contenedor extensible. La especificación MP4 no define una estructura fija para describir los tipos de medios en un contenedor MP4. En su lugar, define una jerarquía de objetos que permite definir estructuras personalizadas para cada formato. La descripción del formato se almacena en el cuadro de descripción de ejemplo ('stsd') de esa secuencia. El cuadro de descripción del ejemplo contiene una lista de entradas de ejemplo. Para cada entrada de ejemplo, un código de 4 bytes, similar a fourcc, define la estructura de formato.

Esta extensibilidad significa que el origen de archivo MPEG-4 no puede reconocer todas las posibles descripciones de formato. En su lugar, adopta un enfoque de dos niveles al crear tipos de medios para las secuencias. Como mínimo, cada tipo de medio contiene los atributos siguientes.



| Atributo                                                                     | Descripción                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)                     | Es igual **a MFMediaType \_ Audio** o **MFMediaType \_ Video**.     |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)                            | Especifica el subtipo de secuencia.                                  |
| [DESCRIPCIÓN \_ DEL \_ EJEMPLO MPEG4 \_ DE \_ MF MT](mf-mt-mpeg4-sample-description.md)      | Contiene el cuadro de descripción de ejemplo completo como un blob binario. |
| [ENTRADA \_ DE EJEMPLO ACTUAL DE MF MT \_ MPEG4 \_ \_ \_](mf-mt-mpeg4-current-sample-entry.md) | Especifica la entrada actual en el cuadro de descripción de ejemplo.     |



 

El origen de archivo MPEG-4 reconoce algunos tipos de entrada de ejemplo. Para estas entradas, puede analizar la estructura de formato y crear un tipo de medio completo, con atributos adicionales que describen los detalles del formato. Vea [Atributos de tipo de medio](media-type-attributes.md).

El origen de archivo MPEG-4 puede analizar las siguientes entradas de ejemplo.



| Código de entrada de ejemplo | Tipo principal | Subtype                                                               | Descripción                                         | Notas                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 'alaw'            | Audio      | **FORMATO \_ WAVE \_ ALAW**                                                | Codificación A-Law                                        |                                                                                                                                                                                                  |
| 'jpeg'            | Vídeo      | **MFVideoFormat \_ MJPG**                                               | Secuencia photo-JPEG                                   | El formato de contenedor QuickTime también admite secuencias JPEG de movimiento con entradas "mjpa" o "mfpb", pero el origen de archivo MPEG-4 no proporciona un tipo de medio completo para esos tipos.               |
| 'avc1'            | Vídeo      | **MFVideoFormat \_ H264**                                               | Vídeo de H.264                                         |                                                                                                                                                                                                  |
| 'mp4a'            | Audio      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC o MP3                                          | La entrada "mp4a" puede describir otros formatos de audio MPEG, pero el origen de archivo MPEG-4 no analiza la estructura de formato.                                                                          |
| 'mp4v'            | Vídeo      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG-4, parte 2                                       | **MFVideoFormat \_ M4S2 se** usa para mpeg-4, parte 2, perfil simple.<br/> **MFVideoFormat \_ MP4V se** usa para todos los demás perfiles mpeg-4, parte 2, incluido el perfil simple avanzado.<br/> |
| 'raw'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM de 8 bits                                     |                                                                                                                                                                                                  |
| 'sowt'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio de PCM little-endian de 16 bits                      |                                                                                                                                                                                                  |
| 'twos'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio de PCM big-endian de 16 bits                         | El origen de archivo MPEG-4 convierte los datos de audio al formato little-endian.                                                                                                                          |
| 'ulaw'            | Audio      | **WAVE \_ FORMAT \_ MULAW**                                               | μ código de ley                                        |                                                                                                                                                                                                  |
| 'vc-1'            | Vídeo      | **MFVideoFormat \_ WVC1**                                               | Vídeo de VC-1                                          |                                                                                                                                                                                                  |
| 'NONE'            | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM big-endian de 8 o 16 bits                | El origen de archivo MPEG-4 convierte los datos de audio al formato little-endian.                                                                                                                          |
| 0x00000000        | Audio      | **MFAudioFormat \_ PCM**                                                | Audio PCM big-endian de 8 o 16 bits                | El origen de archivo MPEG-4 convierte los datos de audio al formato little-endian.                                                                                                                          |
| 0x6d730002        | Audio      | **FORMATO \_ WAVE \_ ADPCM**                                               | Consonación de código de pulso diferencial adaptable (ADPCM) |                                                                                                                                                                                                  |
| 0x6d730011        | Audio      | **FORMATO \_ WAVE \_ IMA \_ ADPCM**                                          | Adpcm                                               |                                                                                                                                                                                                  |



 

Para cualquier otro código que no se muestra en la tabla anterior, el origen de archivo MPEG-4 establece el subtipo de la siguiente manera:

1.  *subtipo* = MFMPEG4Format \_ Base
2.  *subtipo*. Data1 = código de entrada de ejemplo

Para los códigos que no se muestran en la tabla, un descodificador debe usar el atributo [MF \_ MT \_ MPEG4 SAMPLE \_ \_ DESCRIPTION](mf-mt-mpeg4-sample-description.md) para analizar el cuadro de descripción del ejemplo.

Para obtener una lista de códigos de entrada de ejemplo y vínculos a las especificaciones pertinentes, consulte el sitio web de la entidad de [registro "MP4".](https://mp4ra.org)

## <a name="limitations"></a>Limitaciones

El origen de archivo MPEG-4 no admite las siguientes características de los archivos MP4:

-   Pistas externas.
-   Fragmentos de película (cuadros "moof" o "mfra"). 'moof' se admite en Windows 8.
-   Presentaciones por secuencias. El origen de archivo MPEG-4 omite de forma silenciosa las pistas de sugerencias.
-   Búsqueda por código de tiempo SMPTE.
-   Atomes comprimidos ('cmov').

Solo se admiten secuencias de vídeo y audio. Las pistas que contienen otros tipos de secuencia se omiten de forma silenciosa. Los datos multimedia deben colocarse dentro de los átomos "mdat".

Si se instala el complemento de actualización de plataforma para Windows Vista, el origen de archivo MPEG-4 está disponible en Windows Vista, pero solo se puede acceder a él en Windows Vista mediante el Lector de origen [.](source-reader.md)

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 actualizaciones del origen y receptor MPEG-4

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

    

    | Campo                                | Clave de propiedad                         | Id. de etiqueta o de cuadro |
    |--------------------------------------|--------------------------------------|------------|
    | Sistema. Música. AlbumTitleSortOverride  | PKEY \_ Música \_ AlbumTitleSortOverride  | soal       |
    | Sistema. Música. ArtistSortOverride      | PKEY \_ Música \_ ArtistSortOverride      | elevarse       |
    | Sistema. Música. AlbumArtistSortOverride | PKEY \_ Música \_ AlbumArtistSortOverride | soaa       |
    | System.TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | Sistema. Música. ComposerSortOverride    | PKEY \_ Música \_ ComposerSortOverride    | Soco       |

    

     

-   Se ha agregado compatibilidad con atomes 3D estéreo Windows 8 origen MPEG-4.

-   Compatibilidad con AC3 y DD+ agregada en Windows 8 origen y receptor MPEG-4.
-   Los archivos de más de 4 gigabytes (GB) se admiten en Windows 8 receptor MPEG-4 para MP4 no fragmental.
-   La limpieza se ha optimizado en Windows 8 origen MPEG-4.

    Para reducir la latencia, la información de los dos fotogramas clave más cercanos para una posición de búsqueda determinada se expone a través de [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes). Dado que el fotograma clave no tiene fotogramas dependientes, presenta el fotograma después de descodar solo un fotograma. Use [**IMFGetService::GetService para**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) obtener esta interfaz a través del origen de medios, la canalización o la aplicación.

    Establezca la velocidad en cero en el origen MPEG-4. Cuando la canalización está en modo de limpieza, la velocidad es cero.

-   SPS y PPS se pueden almacenar en datos de ejemplo en el receptor MPEG-4.

    [MF \_ El atributo \_ \_ PASSTHROUGH MPEG4SINK SPSPPS](mf-mpeg4sink-spspps-passthrough.md) en el receptor MPEG-4 se define para permitir que sps y PPS se guarden junto con ejemplos de entrada (datos de vídeo H.264). Los clips mp4 producidos son capaces de reproducirse Windows 7 MPEG-4 y otros.

-   SPS y PPS se pueden extraer de ejemplos de entrada en el receptor MPEG-4.

    Cuando SPS y PPS no se establecen a través de [MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER](mf-mt-mpeg-sequence-header-attribute.md) en el tipo de medio de entrada del receptor MPEG-4, el receptor MPEG-4 intentará extraer SPS y PPS de ejemplos de entrada. El receptor MPEG-4 omite los ejemplos de entrada hasta que encuentra el primer SPS y PPS, porque todos los ejemplos de entrada sin SPS y PPS no pueden descodificarse.

-   La información 3D en el registro de configuración de AVC es compatible con MP4 no fragmentado.
-   La longitud de NALU se expone para las muestras comprimidas H.264 con el fin de optimizar la decodificación de DXVA de H.264 VLD.

    El origen MPEG-4 establece [MF \_ NALU \_ LENGTH SET \_ en](mf-nalu-length-set.md) el tipo de medio de salida **MFVideoFormat \_ H264** o **MFVideoFormat \_ h264**. Establece el blob de [MF \_ NALU \_ LENGTH \_ INFORMATION](mf-nalu-length-information.md) en cada muestra de salida, con una longitud de NALU de cuatro bytes para diferentes NALU en una muestra comprimida.

-   Se ha agregado compatibilidad con el audio MPEG2 ADTS en el origen MP4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia y receptores](media-sources-and-sinks.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




