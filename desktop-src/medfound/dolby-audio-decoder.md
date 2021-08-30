---
description: El descodificador de audio Dolby es un MFT que descodifica Dolby Digital (AC-3) y Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Descodificador de audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae38516edd935def5d9b2b041c942a729c45c61
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479871"
---
# <a name="dolby-audio-decoder"></a>Descodificador de audio Dolby

El descodificador de audio Dolby [es Media Foundation transformación](media-foundation-transforms.md) (MFT) que descodifica los siguientes tipos de secuencia:

-   Dolby Digital, también denominado Dolby AC-3
-   Dolby Digital Plus, también denominado AC-3 mejorado (E-AC-3)

> [!IMPORTANT]
> Para las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby Digital para su uso por parte de las aplicaciones de Microsoft.

 

Para obtener más información sobre estos formatos, consulte el documento Del Comité de sistemas de televisión avanzada (ATSC) sobre la compresión de audio digital estándar *(AC-3, E-AC-3) Revisión B*.

El descodificador también puede convertir una secuencia de Dolby Digital Plus al formato Dolby Digital para la salida AC-3 S/PIDF, o dar formato a una secuencia de Dolby Digital Plus para la salida digital HDMI.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de audio Dolby es **\_ CLSID CMSDDPlusDecMFT**, definido en el archivo de encabezado wmcodecdsp.h.

## <a name="input-types"></a>Tipos de entrada

El descodificador de audio Dolby admite los siguientes subtipos de entrada.



| Subtype                                 | Descripción                                                                                                                                                 | Encabezado       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ DOLBY \_ AC3**            | Audio Dolby Digital.                                                                                                                                        | mfapi.h      |
| **MEDIASUBTYPE \_ DVM**                   | Audio Dolby Digital; vea [**Subtipos de audio.**](../directshow/audio-subtypes.md) Este subtipo se puede usar indistintamente **con MEDIASUBTYPE \_ DOLBY \_ AC3.**<br/> | wmcodecdsp.h |
| **MFAudioFormat \_ Dolby \_ Digital \_ Plus** | Audio De Dolby Digital Plus.                                                                                                                                   | mfapi.h      |



 

En la tabla siguiente se enumeran los atributos necesarios y opcionales para el tipo de medio de entrada.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Consulte la tabla anterior para obtener más información. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Frecuencia de muestreo, en muestras por segundo. | Opcional. Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000. Si no se establece este atributo, el valor predeterminado es 48000. <br /><blockquote>[!Note]<br />Las secuencias Ac-3 de Dolby se limitan a las tres tasas más altas de esta lista.</blockquote><br /> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales, incluido el canal de baja frecuencia (LFE), si está presente. | Opcional. Los valores válidos están en el intervalo de 1 (mono) a 8 (configuración del canal 7.1). Si no se establece este atributo, el valor predeterminado es 2 (estéreo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Si se especifica, el valor debe ser coherente con el número de canales de audio. Si no se establece el atributo, el descodificador usa una máscara de canal predeterminada, en función del número de canales. | 




 

En la tabla siguiente se enumeran las configuraciones admitidas del canal Dolby.




| Configuración del canal | Número de canales | Máscaras de canal | 
|-----------------------|--------------------|---------------|
| 1/0 (mono) | 1 | 0x4 (<strong>SPEAKER_FRONT_CENTER</strong>) | 
| 2/0 (estéreo) o 1+1 (mono dual) | 2 | 0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>) | 
| 3/0 | 3 | 0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER) | 
| 2/1 | 3 | 0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>) | 
| 3/1 | 4 | 0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>) | 
| 2/2 | 4 | 0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> o<br /> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>) <br /> | 
| 3/2 | 5 | 0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> o<br /> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>) <br /> | 
| 3/2 + LFE | 6 | 0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)<br /> o<br /> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)<br /> | 
| 3/2/2 + LFE<blockquote>[!Note]<br />Solo Dolby Digital Plus.</blockquote><br /><br /> | 8 | 0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT) | 




 

Además, las configuraciones de canal 1/0, 2/0, 3/0, 2/1, 3/1 y 2/2 también pueden aparecer con un canal LFE.

## <a name="output-types"></a>Tipos de salida

El descodificador de audio Dolby admite los siguientes subtipos de salida.



| Subtype                                                   | Descripción                                                                                                                               | Encabezado    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**                      | Audio Dolby AC-3 con formato de salida digital S/PDIF.                                                                                     | mfapi.h   |
| **SUBTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL \_ PLUS** | Audio Dolby Digital Plus con formato para salida digital HDMI.                                                                               | ksmedia.h |
| **MFAudioFormat \_ Float**                                  | Audio PCM de punto flotante IEEE de 32 bits<br/> **Windows 10:** estéreo, 5.1, 7.1<br/> **Versiones anteriores:** estéreo, 5.1<br/> | mfapi.h   |
| **MFAudioFormat \_ PCM**                                    | Audio PCM de 16 bits<br/> **Windows 10:** estéreo, 5.1, 7.1<br/> **Versiones anteriores:** estéreo, 5.1<br/>                     | mfapi.h   |



 

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Consulte la tabla anterior para obtener más información. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Frecuencia de muestreo, en muestras por segundo. | Necesario. Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000. La frecuencia de muestreo de salida debe ser idéntica a la velocidad de muestreo de entrada. El descodificador no puede cambiar la frecuencia de muestreo de la secuencia. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales, incluido el canal de baja frecuencia (LFE), si está presente. | Se requiere para la salida de PCM. <br /> No es necesario para la salida digital. <br /> Si el tipo de entrada es mono, estéreo o mono dual (todo sin canal LFE), el único valor válido es 2 para la salida estéreo. De lo contrario, el valor puede ser: <br /><ul><li>2 para la mezcla estéreo</li><li>6 para configuraciones de canal 5.1</li><li>8 para configuraciones de canal 7.1</li></ul> | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Se requiere para la salida de PCM si el número de canales es mayor que 2. El valor debe ser:<br /><ul><li>0x3 salida estéreo</li><li>0x3F para la salida del canal 5.1</li><li>0x63F para la salida del canal 7.1</li></ul>No es necesario para la salida digital. <br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Número de bits por muestra de audio. | Se requiere para la salida de PCM. El valor debe ser 32 <strong>para MFAudioFormat_Float</strong>y 16 para <strong>MFAudioFormat_PCM</strong>.<br /> No es necesario para la salida digital.<br /> | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Número de bits válidos de datos de audio en cada muestra de audio. | Opcional para la salida de PCM. Si se establece, el valor debe ser idéntico <a href="mf-mt-audio-bits-per-sample-attribute.md">al MF_MT_AUDIO_BITS_PER_SAMPLE</a>.<br /> No es necesario para los subtipos de salida digital.<br /> | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Alineación de bloques, en bytes. | Opcional para la salida de PCM. No es necesario para la salida digital. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Número medio de bytes por segundo. | Opcional para la salida de PCM. No es necesario para la salida digital. | 




 

## <a name="transform-attributes"></a>Transformar atributos

El descodificador de audio Dolby implementa [**el método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) La aplicación puede usar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                | Descripción                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | Especifica si una secuencia de audio Dolby de 2 canales está codificada como estéreo o doble mono. Antes de descodificar el primer fotograma Dolby, el valor es **eAVDecAudioDualMono \_ UnSpecified.** Una vez que comienza la decodificación, el valor refleja el fotograma Dolby más reciente.<br/> Solo lectura. <br/> |
| [CODECAPI \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | Especifica cómo el descodificador reproduce el audio mono dual. El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**. La aplicación puede establecer esta propiedad en cualquier momento.<br/> Lectura/escritura<br/>                                                                            |
| [CODECAPI \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | Para secuencias Dolby Digital (AC-3), especifica la velocidad de bits del flujo de entrada en bits por segundo. Para Dolby Digital Plus (E-AC3), el valor siempre es cero.<br/> Solo lectura.<br/>                                                                                              |
| [CODECAPI \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | Corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico.<br/> Lectura/escritura<br/>                                                                                                                                                                                    |
| [CODECAPI \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | Aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico.<br/> Lectura/escritura<br/>                                                                                                                                                                                   |
| [CODECAPI \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | Modo de control de compresión.<br/> Lectura/escritura<br/>                                                                                                                                                                                                                          |
| [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | Tipo de mezcronía estéreo. Esta propiedad se aplica cuando la entrada es una secuencia multicanal y la salida es una secuencia estéreo.<br/> Lectura/escritura<br/>                                                                                                                           |
| [MFT \_ ADMITE EL CAMBIO DE FORMATO \_ \_ \_ DINÁMICO](mft-support-dynamic-format-change-attribute.md) | Este atributo devuelve **FALSE**, lo que indica que el descodificador debe purgarse antes de establecer un nuevo tipo de entrada.<br/> Lectura/escritura<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

El descodificador solo acepta secuencias Dolby sin procesar, tal como se define en A/52B. No se admiten cargas como paquetes Secuencias paquetes (PES). Para Dolby Digital Plus, el descodificador descodifica hasta 5,1 canales. En Windows 10, las secuencias de canal 7.1 se descodifican sin mezclen. En versiones anteriores del sistema operativo, si la secuencia es de 7.1 canales, solo se descodificará la mezcla de canales 5.1. Si la secuencia es Dolby Digital Plus con más de una subtransmisión independiente, solo se descodifica la subsección independiente 0. El descodificador omite otras subdiciones independientes. Además, el descodificador omite todas las subdiciones dependientes. El descodificador admite el descifrado y descodificación de secuencias protegidas por la tecnología Rights Management digital (DRM).

Si el tipo de medio de entrada tiene una configuración de canal que no sea mono, estéreo o dual-mono (todo ello sin canal LFE), el descodificador proporciona dos opciones para las configuraciones del canal de salida:

-   Salida de 8 canales (configuración del canal 7.1)
-   Salida de 6 canales (configuración del canal 5.1)
-   Mezclada estéreo

Si se selecciona la reducción estéreo, el tipo de reducción se puede establecer en MFT mediante la propiedad [ \_ AVDecDDStereoDownMixMode de CODECAPI.](codecapi-avdecddstereodownmixmode.md)

Si el tipo de salida **es MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF,** cada búfer de salida contiene 6144 bytes. El búfer comienza con un encabezado S/PDIF de 8 bytes, seguido de un marco AC-3 comprimido, seguido del relleno cero a 6144 bytes.

Si el tipo de salida es **KSDATAFORMAT \_ SUBTYPE \_ IEC61937 \_ DOLBY DIGITAL \_ \_ PLUS,** cada búfer de salida contiene 24 576 bytes. El búfer comienza con un encabezado S/PDIF de 8 bytes, seguido de 1 a 6 fotogramas Dolby Digital Plus comprimidos correspondientes a 1536 muestras de PCM, seguido de relleno cero a 24 576 bytes. Para la salida HDMI, solo se empaqueta la subsección 0 independiente.

El descodificador MFT se registra con la marca **MFT \_ ENUM \_ FLAG \_ FIELDOFUSE**, que indica que el MFT que debe desbloquear la aplicación antes de su uso. Para obtener más información, vea [Restricciones de campo de uso.](field-of-use-restrictions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
