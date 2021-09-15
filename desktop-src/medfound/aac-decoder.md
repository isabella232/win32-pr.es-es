---
description: 'El descodificador Microsoft Media Foundation AAC es una transformación de Media Foundation que descodifica los siguientes perfiles de Codificación de audio avanzada (AAC) y AAC de alta eficacia (HE-AAC):'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Descodificador de AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf50196029f484264ddb33c8e10a25e61cb0dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466567"
---
# <a name="aac-decoder"></a>Descodificador de AAC

El descodificador Microsoft Media Foundation AAC es una transformación de [Media Foundation](media-foundation-transforms.md) que descodifica los siguientes perfiles de Codificación de audio avanzada (AAC) y AAC de alta eficacia (HE-AAC):

-   Perfil de baja complejidad (LC) de AAC MPEG-2 (multicanal).
-   MPEG-4 HE-AAC v1 (multicanal) con núcleo AAC-LC.
-   MPEG-4 HE-AAC v2 (estéreo) con núcleo AAC-LC.

El descodificador de AAC admite tanto secuencias AAC sin procesar sin encabezados como AAC en una secuencia de transporte de datos de audio (ADTS).

A partir Windows 8, el descodificador de AAC también admite la descodificación de secuencias de transporte de audio MPEG-4 con una capa multiplex (LATM) y una capa de sincronización (LOAS). También puede convertir una secuencia LATM/LOAS en ADTS.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador AAC es **\_ CLSID CMSAACDecMFT**, definido en el archivo de encabezado wmcodecdsp.h.

## <a name="media-types"></a>Tipos de medios

El descodificador de AAC admite los siguientes tipos de medios.

### <a name="input-types"></a>Tipos de entrada

El descodificador de AAC admite los siguientes subtipos de audio:



| Subtype                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Encabezado       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC sin procesar o AAC de ADTS.<br/> Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y estéreo paramétrico (PS), si están presentes. El efecto de la herramienta SBR es duplicar la frecuencia de muestreo descodificada en relación con la frecuencia de muestreo principal de AAC-LC. El efecto de la herramienta PS es descodificar estéreo de una secuencia AAC-LC de núcleo monocanal.<br/> Este subtipo es equivalente **a MEDIASUBTYPE_MPEG_HEAAC**, definido en wmcodecdsp.h. Consulte [GUID de subtipo de audio.](audio-subtype-guids.md) <br/> El [origen de archivo MPEG-4](mpeg-4-file-source.md) y el analizador de ADTS emiten este subtipo. <br/> | mfapi.h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC sin procesar. <br/> Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp.h |



 

Para configurar el descodificador de AAC, establezca los siguientes atributos en el tipo de medio de entrada.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de audio. | Consulte la descripción anterior para obtener más información. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Perfil y nivel de audio. <br /> | Opcional. Solo se aplica a <strong>MFAudioFormat_AAC</strong>. <br /> El valor de este atributo es el <strong>campo audioProfileLevelIndication,</strong> tal como se define en ISO/IEC 14496-3. <br /> Si es desconocido, establezca en cero o 0xFE ("no se especificó ningún perfil de audio").<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo de carga.<br /> | Solo se aplica a <strong>MFAudioFormat_AAC</strong>. El descodificador admite los siguientes tipos de carga: <br /><ul><li>0: AAC sin formato. La secuencia solo raw_data_block(), tal como se define en MPEG-2.</li><li>1: ADTS. La secuencia contiene un adts_sequence(), tal como se define en MPEG-2. Solo se permite raw_data_block() por adts_frame().</li><li>3: Secuencia de transporte de audio con una capa de sincronización (LOAS) y una capa multiplex (LATM). De los tres tipos de LOAS, solo <strong>se admite AudioSyncStream.</strong> La capa multiplex es <strong>AudioMuxElement,</strong>restringida a un programa de audio y una capa.</li></ul><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE es</a> opcional. Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia solo raw_data_block elementos.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profundidad de bits deseada del audio PCM descodificado. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Para obtener más información, vea <a href="#format-constraints">Restricciones de formato</a>. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.<br /> | La interpretación de este valor depende del subtipo de medios, como se describió anteriormente.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Frecuencia de muestreo, en muestras por segundo.<br /> | La interpretación de este valor depende del subtipo de medios, como se describió anteriormente.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | Información de formato adicional. | El valor de este atributo depende del subtipo.<br /><ul><li><strong>MFAudioFormat_AAC:</strong>contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>DESACWAVEATEX</strong> (es decir, después del <strong>miembro wfx).</strong> Esto va seguido de los datos AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1:</strong>contiene los datos audioSpecificConfig(). Estos datos deben aparecer; De lo contrario, el descodificador rechazará el tipo de medio.</li></ul>La longitud de los datos de AudioSpecificConfig() es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS. Es más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.<br /> El valor de <strong>audioObjectType</strong> tal como se define en AudioSpecificConfig() debe ser 2, lo que indica AAC-LC. El valor de <strong>extensionAudioObjectType</strong> debe ser 5 para SBR o 29 para PS. <br /> | 




 

### <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes tipos de salida:




| Subtype | Descripción | 
|---------|-------------|
| <strong>MFAudioFormat_Float</strong> | Audio de punto flotante IEEE. | 
| <strong>MFAudioFormat_PCM</strong> | Audio PCM de 16 bits. | 
| <strong>MFAudioFormat_AAC</strong> | Requiere Windows 8. <br /> Este tipo de salida se puede usar para convertir una secuencia de AAC en el formato LOAS/LATM al formato ADTS. <br /> Para convertir un flujo LOAS/LATM en un flujo de ADTS, establezca el tipo de entrada <strong>en MFAudioFormat_AAC</strong> con el tipo de carga 3 (LOAS). A continuación, establezca el tipo <strong>de salida MFAudioFormat_AAC</strong> con el tipo de carga 1 (ADTS). El descodificador volverá a formatear el conainter sin descodificar la secuencia de bits. <br /><blockquote>[!Note]<br />El descodificador no <strong>registra</strong> MFAudioFormat_AAC como un tipo de salida. Sin embargo, <strong>si</strong> la aplicación establece el tipo de entrada como se describe, el método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> devuelve MFAudioFormat_AAC en la lista de tipos de salida disponibles.</blockquote><br /><br /> | 




 

Si el flujo de entrada contiene más de dos canales, el descodificador de AAC proporciona dos opciones para el formato de salida:

-   La misma configuración de canal que el tipo de entrada.
-   Plegado estéreo hacia abajo.

## <a name="format-constraints"></a>Restricciones de formato

La frecuencia de muestreo de audio descodificado debe ser una de las siguientes, después de aplicar SBR (si está presente):

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

No se admiten velocidades de muestreo superiores a 48 kHz.

El descodificador admite hasta 6 canales de audio. Para cada configuración del hablante, el descodificador espera que los elementos sintácticos de AAC aparezcan en un orden determinado. En la tabla siguiente se enumeran las configuraciones admitidas del hablante. En la tercera columna de la tabla se enumeran los elementos sintácticos esperados y su orden, mediante la siguiente notación:

-   &lt;SCE1: &gt; el single_channel_element (SCE) asociado al altavoz del centro frontal.
-   &lt;SCE2: &gt; SCE asociado al altavoz del centro posterior.
-   &lt;CPE1: &gt; el channel_pair_element (CPE) asociado a los altavoces frontales.
-   &lt;CPE2: el CPE asociado a los altavoces de la parte posterior &gt; (o lateral)
-   &lt;&gt;LFE: el lfe_channel_element (LFE).

Para obtener más información sobre estos elementos sintácticos, consulte ISO/IEC 13818-7.



| Configuración       | Máscara de canal                                                                                                                                                              | Elementos sintácticos de AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | &lt;SCE1&gt;                                    |
| Mono estéreo o dual | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | &lt;CPE1&gt;                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | &lt;CPE1 &gt; &lt; SCE1&gt;                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | &lt;CPE1 &gt; &lt; CPE2&gt;                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | &lt;SCE1 &gt; &lt; CPE1&gt;                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | &lt;SCE1 &gt; &lt; CPE1 &gt; &lt; SCE2&gt;            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | &lt;SCE1 &gt; &lt; CPE1 &gt; &lt; CPE2&gt;            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | &lt;SCE1 &gt; &lt; CPE1 &gt; &lt; CPE2 &gt; &lt; LFE&gt; |



 

En el caso de AAC sin procesar, cada ejemplo de entrada debe contener exactamente un marco comprimido de AAC completo.

Para ADTS, cada ejemplo de entrada puede contener varios fotogramas de audio, así como fotogramas parciales, es decir, los fotogramas pueden abarcar los límites de la muestra. Cada encabezado de ADTS debe ir seguido de un marco de AAC.

El descodificador de AAC no admite ninguno de los siguientes elementos:

-   Perfil principal, Sample-Rate perfil escalable (SRS) o perfil de predicción a largo plazo (LTP).
-   Formato de intercambio de datos de audio (ADIF).
-   Secuencias de transporte LATM/LAOS.
-   Elementos de canal de acoplamiento (CCE). El descodificador omitirá los fotogramas de audio con LOS CCE.
-   AAC-LC con un tamaño de marco de 960 muestras. Solo se admiten 1024 fotogramas de ejemplo.

## <a name="transform-attributes"></a>Transformar atributos

El descodificador de AAC implementa el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Las aplicaciones pueden usar este método para obtener o establecer los atributos siguientes.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a> | Especifica si el audio de 2 canales se codifica como estéreo o mono dual. Tratar como de solo lectura. | 
| <a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a> | Especifica cómo el descodificador reproduce el audio mono dual. El valor predeterminado es <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>salida Ch1 a los altavoces izquierdo y derecho. <br /> Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado.<br /> | 
| <a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a> | El descodificador de AAC no controla los cambios de formato dinámico y se debe vaciar o purgar antes de establecer un nuevo tipo de medio de entrada. Trate este atributo como de solo lectura. <br /><blockquote>[!Note]<br />El descodificador de AAC notifica incorrectamente un valor <strong>de TRUE</strong> para este atributo.</blockquote><br /><br /> En Windows 7, el descodificador notifica incorrectamente un valor de <strong>TRUE</strong> para este atributo. En Windows 8, el descodificador notifica <strong>FALSE</strong>, que es el valor correcto.<br /> | 




 

## <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo del tipo de medio de entrada necesario para una secuencia AAC-LC de 6 canales y 48 kHz, mediante una carga de AAC sin formato:



| Atributo                                                                                      | Value                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (opcional)                                                                      |



 

Los primeros 12 bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corresponden a los siguientes miembros de la estructura [**HEAACWAVEINFO:**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)

-   **wPayloadType** = 0 (AAC sin procesar)
-   **wAudioProfileLevelIndication** = 0x2a (perfil de AAC, nivel 4)
-   **wStructType** = 0

Los dos últimos bytes [**de MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contienen el valor de AudioSpecificConfig(), tal como se define en MPEG-4.

-   AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)
-   AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)
-   AudioSpecificConfig.channelConfiguration = 6 (4 bits)
-   GASpecificConfig.frameLengthFlag = 0 (1 bit)
-   GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)
-   GASpecificConfig.extensionFlag = 0 (1 bit)

Dado este tipo de entrada, use el siguiente tipo de medio de salida para obtener audio PCM de punto flotante de 6 canales y 32 bits del descodificador:



| Atributo                                                                                    | Value                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (opcional)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (opcional)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3f (opcional)          |



 

Si se instala el complemento de actualización de plataforma para Windows Vista, el descodificador de audio AAC está disponible en Windows Vista, pero solo se puede acceder a él en Windows Vista mediante el lector de origen [.](source-reader.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                                                                                                     |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll en Windows 7;</dt> <dt>MSAudDecMFT.dll en Windows 8</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Tipos de medios de AAC](aac-media-types.md)
</dt> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[**Descodificador de audio Microsoft MPEG-1/DD/AAC**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
