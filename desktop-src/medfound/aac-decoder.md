---
description: 'El descodificador AAC Microsoft Media Foundation es una transformación de Media Foundation que descodifica los siguientes perfiles de codificación de audio avanzado (AAC) y AAC (HE-AAC) de alta eficacia:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Descodificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705567"
---
# <a name="aac-decoder"></a>Descodificador AAC

El descodificador AAC Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que descodifica los siguientes perfiles de codificación de audio avanzado (AAC) y AAC (HE-AAC) de alta eficacia:

-   Perfil de baja complejidad (LC) de MPEG-2 AAC (multicanal).
-   MPEG-4 HE-AAC V1 (multicanal) con núcleo AAC-LC.
-   MPEG-4 HE-AAC V2 (estéreo) con núcleo AAC-LC.

El descodificador AAC admite las secuencias AAC sin procesar sin encabezados y AAC en una secuencia de transporte de datos de audio (ADTS).

A partir de Windows 8, el descodificador AAC también admite la descodificación de secuencias de transporte de audio MPEG-4 con una capa de multiplexación (LATM) y una capa de sincronización (Loa). También puede convertir una secuencia LATM/Loa a ADTS.

## <a name="media-types"></a>Tipos de medios

El descodificador AAC admite los siguientes tipos de medios.

### <a name="input-types"></a>Tipos de entrada

El descodificador AAC admite los siguientes subtipos de audio:



| Subtype                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Encabezado       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC sin procesar o ADTS AAC.<br/> Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y de estéreo paramétricos (PS), si está presente. El efecto de la herramienta SBR es duplicar la velocidad de muestra descodificada en relación con la velocidad de muestra de núcleo AAC-LC. El efecto de la herramienta PS es descodificar estéreo de una secuencia de núcleos AAC-LC de canal mono.<br/> Este subtipo es equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definido en wmcodecdsp. h. Vea [GUID de subtipo de audio](audio-subtype-guids.md). <br/> El [origen de archivo MPEG-4](mpeg-4-file-source.md) y el analizador ADTS generan este subtipo. <br/> | mfapi. h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC sin procesar. <br/> Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp. h |



 

Para configurar el descodificador AAC, establezca los siguientes atributos en el tipo de medio de entrada.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal.</td>
<td>Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de audio.</td>
<td>Consulte la descripción anterior para obtener más información.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Nivel y Perfil de audio. <br/></td>
<td>Opcional. Solo se aplica a <strong>MFAudioFormat_AAC</strong>. <br/> El valor de este atributo es el campo <strong>audioProfileLevelIndication</strong> , tal y como se define en ISO/IEC 14496-3. <br/> Si es desconocido, establezca en cero o 0xFE (no se ha &quot; especificado ningún perfil de audio &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo de carga.<br/></td>
<td>Solo se aplica a <strong>MFAudioFormat_AAC</strong>. El descodificador admite los siguientes tipos de carga: <br/>
<ul>
<li>0: AAC sin formato. El flujo contiene solo los elementos raw_data_block (), tal y como se define en MPEG-2.</li>
<li>1: ADTS. La secuencia contiene un adts_sequence (), tal y como se define en MPEG-2. Solo se permite un raw_data_block () por adts_frame ().</li>
<li>3: flujo de transporte de audio con un nivel de sincronización (Loa) y una capa de multiplexación (LATM). De los tres tipos de loa, solo se admite <strong>AudioSyncStream</strong> . La capa Multiplex es <strong>AudioMuxElement</strong>, está restringida a un programa de audio y una capa.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> es opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que el flujo solo contiene elementos raw_data_block.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profundidad de bits deseada del audio PCM descodificado.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Para obtener más información, consulta <a href="#format-constraints">Format Constraints</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.<br/></td>
<td>La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Frecuencia de muestreo, en muestras por segundo.<br/></td>
<td>La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Información de formato adicional.</td>
<td>El valor de este atributo depende del subtipo.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>WAVEFORMATEX</strong> (es decir, después del miembro de <strong>WFX</strong> ). A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene los datos de AudioSpecificConfig (). Estos datos deben aparecer; de lo contrario, el descodificador rechazará el tipo de medio.</li>
</ul>
La longitud de los datos AudioSpecificConfig () es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS. Tiene más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.<br/> El valor de <strong>audioObjectType</strong> tal y como se define en AudioSpecificConfig () debe ser 2, lo que indica AAC-LC. El valor de <strong>extensionAudioObjectType</strong> debe ser 5 para SBR o 29 para PS. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes tipos de salida:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Audio de punto flotante IEEE.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>audio PCM de 16 bits.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Requiere Windows 8. <br/> Este tipo de salida se puede usar para convertir una secuencia AAC en formato loa/LATM al formato ADTS. <br/> Para convertir una secuencia loa/LATM en una secuencia ADTS, establezca el tipo de entrada en <strong>MFAudioFormat_AAC</strong> con el tipo de carga 3 (Loa). A continuación, establezca el tipo de salida en <strong>MFAudioFormat_AAC</strong> con el tipo de carga 1 (ADTS). El descodificador volverá a formatear el conainter sin descodificar el fragmentada. <br/>
<blockquote>
[!Note]<br />
El descodificador no registra <strong>MFAudioFormat_AAC</strong> como un tipo de salida. Sin embargo, si la aplicación establece el tipo de entrada como se describe, el método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> devuelve <strong>MFAudioFormat_AAC</strong> en la lista de tipos de salida disponibles.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Si el flujo de entrada contiene más de dos canales, el descodificador AAC proporciona dos opciones para el formato de salida:

-   La misma configuración de canal que el tipo de entrada.
-   Plegado estéreo.

## <a name="format-constraints"></a>Restricciones de formato

La velocidad de muestreo de audio descodificada debe ser una de las siguientes, después de aplicar SBR (si existe):

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

No se admiten las tasas de muestreo por encima de 48 kHz.

El descodificador admite hasta 6 canales de audio. Para cada configuración de altavoz, el descodificador espera que los elementos sintácticos AAC aparezcan en un orden determinado. En la tabla siguiente se enumeran las configuraciones de altavoz compatibles. En la tercera columna de la tabla se enumeran los elementos sintácticos esperados y su orden mediante la notación siguiente:

-   <SCE1>: El single_channel_element (SCE) asociado al altavoz del centro frontal.
-   <SCE2>: El SCE asociado al altavoz del centro trasero.
-   <CPE1>: El channel_pair_element (CPE) asociado a los altavoces frontales.
-   <CPE2>: El CPE asociado a los altavoces traseros (o laterales)
-   <LFE>: El lfe_channel_element (LFE).

Para obtener más información acerca de estos elementos sintácticos, consulte ISO/IEC 13818-7.



| Configuración       | Máscara de canal                                                                                                                                                              | Elementos sintácticos AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Estéreo o dual mono | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

En el AAC sin procesar, cada muestra de entrada debe contener exactamente un fotograma comprimido AAC completo.

En el caso de ADTS, cada ejemplo de entrada puede contener varios fotogramas de audio, así como fotogramas parciales, es decir, los fotogramas pueden abarcar los límites de ejemplo. Cada encabezado ADTS debe ir seguido de un marco AAC.

El descodificador AAC no es compatible con ninguno de los siguientes elementos:

-   Perfil principal, perfil de Sample-Rate escalable (SRS) o Perfil de predicción a largo plazo (LTP).
-   Formato de intercambio de datos de audio (ADIF).
-   Flujos de transporte de LATM/LAOS.
-   Acoplamiento de elementos de canal (CCEs). El descodificador omitirá los fotogramas de audio con CCEs.
-   AAC-LC con un tamaño de fotograma 960 de ejemplo. Solo se admiten los fotogramas de ejemplo 1024.

## <a name="transform-attributes"></a>Atributos de transformación

El descodificador AAC implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Especifica si el audio de 2 canales se codifica como estéreo o dual mono. Tratar como de solo lectura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Especifica cómo el descodificador Reproduce audio mono dual. El valor predeterminado es <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: CH1 de salida a los altavoces izquierdo y derecho. <br/> Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>El descodificador AAC no controla los cambios de formato dinámico y se debe vaciar o purgar antes de que se establezca un nuevo tipo de medio de entrada. Trate este atributo como de solo lectura. <br/>
<blockquote>
[!Note]<br />
El descodificador AAC informa incorrectamente de un valor de <strong>true</strong> para este atributo.
</blockquote>
<br/> <br/> En Windows 7, el descodificador informa incorrectamente de un valor de <strong>true</strong> para este atributo. En Windows 8, el descodificador informa de <strong>false</strong>, que es el valor correcto.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo del tipo de medio de entrada necesario para una secuencia de 6 canales AAC-LC de 48 kHz mediante una carga de AAC sin procesar:



| Atributo                                                                                      | Value                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (opcional)                                                                      |



 

Los 12 primeros bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corresponden a los siguientes miembros de la estructura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :

-   **wPayloadType** = 0 (AAC sin procesar)
-   **wAudioProfileLevelIndication** = 0X2a (perfil AAC, nivel 4)
-   **wStructType** = 0

Los dos últimos bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contienen el valor de AudioSpecificConfig (), tal y como se define en MPEG-4.

-   AudioSpecificConfig. audioObjectType = 2 (LC AAC) (5 bits)
-   AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)
-   AudioSpecificConfig. channelConfiguration = 6 (4 bits)
-   GASpecificConfig. frameLengthFlag = 0 (1 bit)
-   GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)
-   GASpecificConfig. extensionFlag = 0 (1 bit)

Dado este tipo de entrada, use el siguiente tipo de medio de salida para obtener el audio PCM de punto flotante de 32 bits de 6 canales del descodificador:



| Atributo                                                                                    | Value                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (opcional)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (opcional)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3F (opcional)          |



 

Si está instalado el complemento de actualización de plataforma para Windows Vista, el descodificador de audio AAC está disponible en Windows Vista, pero solo es accesible en Windows Vista mediante el [lector de origen](source-reader.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                                                                                                     |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll en Windows 7; </dt> <dt>MSAudDecMFT.dll en Windows 8</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Tipos de medios AAC](aac-media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[**Descodificador de audio MPEG-1/DD/AAC de Microsoft**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
