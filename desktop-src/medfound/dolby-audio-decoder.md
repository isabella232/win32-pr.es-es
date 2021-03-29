---
description: El descodificador de audio Dolby es un MFT que descodifica Dolby Digital (AC-3) y Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Descodificador de audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808096"
---
# <a name="dolby-audio-decoder"></a>Descodificador de audio Dolby

El descodificador de audio Dolby es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que descodifica los tipos de secuencia siguientes:

-   Dolby digital, también denominado Dolby AC-3
-   Dolby Digital Plus, también denominado AC-3 mejorado (E-AC-3)

> [!IMPORTANT]
> En el caso de las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en lo que respecta al programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.

 

Para obtener más información acerca de estos formatos, consulte el documento sobre el Comité de sistemas de televisión avanzado (ATSC) ( *AC-3, E-AC-3) revisión B*.

El descodificador también puede convertir una secuencia Dolby Digital Plus en el formato Dolby digital para la salida AC-3 S/PIDF o dar formato a un flujo Dolby Digital Plus para la salida digital HDMI.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de audio Dolby es **CLSID \_ CMSDDPlusDecMFT**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="input-types"></a>Tipos de entrada

El descodificador de Dolby audio admite los siguientes subtipos de entrada.



| Subtype                                 | Descripción                                                                                                                                                 | Encabezado       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MEDIASUBTYPE \_ Dolby \_ AC3**            | Audio Dolby digital.                                                                                                                                        | mfapi. h      |
| **MEDIASUBTYPE \_ DVM**                   | Audio Dolby digital; vea [**subtipos de audio**](../directshow/audio-subtypes.md). Este subtipo se puede usar indistintamente con **MEDIASUBTYPE \_ Dolby \_ AC3**.<br/> | wmcodecdsp. h |
| **MFAudioFormat \_ Dolby \_ digital \_ Plus** | Audio Dolby Digital Plus.                                                                                                                                   | mfapi. h      |



 

En la tabla siguiente se enumeran los atributos requires y opcionales para el tipo de medio de entrada.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obligatorio. Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de audio.</td>
<td>Obligatorio. Vea la tabla anterior para obtener más información.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Frecuencia de muestreo, en muestras por segundo.</td>
<td>Opcional. Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000. Si no se establece este atributo, el valor predeterminado es 48000. <br/>
<blockquote>
[!Note]<br />
Los flujos Dolby AC-3 se limitan a las tres tasas más altas de esta lista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</td>
<td>Opcional. Los valores válidos están en el intervalo de 1 (mono) a 8 (configuración de canal 7,1). Si no se establece este atributo, el valor predeterminado es 2 (estéreo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Si se especifica, el valor debe ser coherente con el número de canales de audio. Si no se establece el atributo, el descodificador utiliza una máscara de canal predeterminada, en función del número de canales.</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las configuraciones de canal Dolby admitidas.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Configuración del canal</th>
<th>Número de canales</th>
<th>Máscaras de canal</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1/0 (mono)</td>
<td>1</td>
<td>0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/0 (estéreo) o 1 + 1 (mono dual)</td>
<td>2</td>
<td>0X3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</td>
</tr>
<tr class="odd">
<td>3/0</td>
<td>3</td>
<td>0X7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</td>
</tr>
<tr class="even">
<td>2/1</td>
<td>3</td>
<td>0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="odd">
<td>3/1</td>
<td>4</td>
<td>0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</td>
</tr>
<tr class="even">
<td>2/2</td>
<td>4</td>
<td>0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> or<br/> 0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="odd">
<td>3/2</td>
<td>5</td>
<td>0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> or<br/> 0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) <br/></td>
</tr>
<tr class="even">
<td>3/2 + LFE</td>
<td>6</td>
<td>0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)<br/> or<br/> 0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)<br/></td>
</tr>
<tr class="odd">
<td>3/2/2 + LFE
<blockquote>
[!Note]<br />
Solo Dolby Digital Plus.
</blockquote>
<br/> <br/></td>
<td>8</td>
<td>0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</td>
</tr>
</tbody>
</table>



 

Además, las configuraciones de canal 1/0, 2/0, 3/0, 2/1, 3/1 y 2/2 también pueden aparecer con un canal LFE.

## <a name="output-types"></a>Tipos de salida

El descodificador de audio Dolby admite los siguientes subtipos de salida.



| Subtype                                                   | Descripción                                                                                                                               | Encabezado    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **MFAudioFormat \_ Dolby \_ AC3 ( \_ SPDIF)**                      | Audio Dolby AC-3 con formato de salida digital S/PDIF.                                                                                     | mfapi. h   |
| **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus** | Audio Dolby Digital Plus con formato de salida digital HDMI.                                                                               | ksmedia. h |
| **MFAudioFormat \_ float**                                  | Audio PCM de punto flotante IEEE 32-bit<br/> **Windows 10**: estéreo, 5,1, 7,1<br/> **Versiones anteriores**: estéreo, 5,1<br/> | mfapi. h   |
| **MFAudioFormat \_ PCM**                                    | audio PCM de 16 bits<br/> **Windows 10**: estéreo, 5,1, 7,1<br/> **Versiones anteriores**: estéreo, 5,1<br/>                     | mfapi. h   |



 

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obligatorio. Debe ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de audio.</td>
<td>Obligatorio. Vea la tabla anterior para obtener más información.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Frecuencia de muestreo, en muestras por segundo.</td>
<td>Obligatorio. Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000. La velocidad de muestra de salida debe ser idéntica a la velocidad de muestra de entrada. El descodificador no puede cambiar la velocidad de muestreo de la secuencia.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</td>
<td>Se requiere para la salida del PCM. <br/> No es necesario para la salida digital. <br/> Si el tipo de entrada es mono, estéreo o dual mono (todo sin canal LFE), el único valor válido es 2, para la salida estéreo. De lo contrario, el valor puede ser: <br/>
<ul>
<li>2 para downmix estéreo</li>
<li>6 para configuraciones de canal 5,1</li>
<li>8 para configuraciones de canal 7,1</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Se requiere para la salida del PCM si el número de canales es mayor que 2. El valor debe ser:<br/>
<ul>
<li>0X3 para la salida estéreo</li>
<li>0x3F para la salida del canal 5,1</li>
<li>0x63F para la salida del canal 7,1</li>
</ul>
No es necesario para la salida digital. <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Número de bits por muestra de audio.</td>
<td>Se requiere para la salida del PCM. El valor debe ser 32 para <strong>MFAudioFormat_Float</strong>y 16 para <strong>MFAudioFormat_PCM</strong>.<br/> No es necesario para la salida digital.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Número de bits válidos de datos de audio en cada ejemplo de audio.</td>
<td>Opcional para la salida de PCM. Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.<br/> No es necesario para los subtipos de salida digital.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alineación de bloque, en bytes.</td>
<td>Opcional para la salida de PCM. No es necesario para la salida digital.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Número promedio de bytes por segundo.</td>
<td>Opcional para la salida de PCM. No es necesario para la salida digital.</td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a>Atributos de transformación

El descodificador de audio Dolby implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . La aplicación puede utilizar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                | Descripción                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecAudioDualMono](../directshow/avdecaudiodualmono-property.md)                        | Especifica si una secuencia de audio Dolby de 2 canales se codifica como estéreo o dual mono. Antes de descodificar el primer fotograma Dolby, el valor es **EAVDecAudioDualMono \_ sin especificar**. Una vez iniciada la descodificación, el valor refleja el fotograma Dolby más reciente.<br/> Solo lectura. <br/> |
| [CODECAPI \_ AVDecAudioDualMonoReproMode](../directshow/avdecaudiodualmonorepromode-property.md)      | Especifica cómo el descodificador Reproduce audio dual mono. El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ \_** a la izquierda. La aplicación puede establecer esta propiedad en cualquier momento.<br/> Lectura/escritura<br/>                                                                            |
| [CODECAPI \_ AVDecCommonMeanBitRate](../directshow/avdeccommonmeanbitrate.md)                         | En el caso de las secuencias Dolby Digital (AC-3), especifica la velocidad de bits del flujo de entrada en bits por segundo. Para Dolby Digital Plus (E-AC3), el valor siempre es cero.<br/> Solo lectura.<br/>                                                                                              |
| [CODECAPI \_ AVDecDDDynamicRangeScaleHigh](../directshow/avdecdddynamicrangescalehigh-property.md)    | El corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico.<br/> Lectura/escritura<br/>                                                                                                                                                                                    |
| [CODECAPI \_ AVDecDDDynamicRangeScaleLow](../directshow/avdecdddynamicrangescalelow-property.md)      | El aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico.<br/> Lectura/escritura<br/>                                                                                                                                                                                   |
| [CODECAPI \_ AVDecDDOperationalMode](../directshow/avdecddoperationalmode-property.md)                | Modo de control de compresión.<br/> Lectura/escritura<br/>                                                                                                                                                                                                                          |
| [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md)              | Tipo de downmix estéreo. Esta propiedad se aplica cuando la entrada es una secuencia multicanal y el resultado es una secuencia estéreo.<br/> Lectura/escritura<br/>                                                                                                                           |
| [la MFT \_ admite el \_ \_ cambio de formato dinámico \_](mft-support-dynamic-format-change-attribute.md) | Este atributo devuelve **false**, lo que indica que el descodificador se debe purgar antes de que se establezca un nuevo tipo de entrada.<br/> Lectura/escritura<br/>                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

El descodificador solo acepta secuencias Dolby sin formato, tal y como se define en/52B. No se admiten cargas como las secuencias elementales (PES) en paquetes. En el caso de Dolby Digital Plus, el descodificador descodifica hasta 5,1 canales. En Windows 10, los flujos de canal 7,1 se descodifican sin downmix. En versiones anteriores del sistema operativo, si el flujo es de 7,1 canales, solo se descodificará el canal de 5,1 downmix. Si la secuencia es Dolby Digital Plus con más de un subflujo independiente, solo se descodifica el subflujo 0 independiente. El descodificador omite otros subflujos independientes. Además, el descodificador omite todas las subsecuencias dependientes. El descodificador admite el descifrado y la descodificación de secuencias que están protegidas por la tecnología de Rights Management digital (DRM).

Si el tipo de medio de entrada tiene una configuración de canal que no es mono, estéreo o dual mono (todo sin canal LFE), el descodificador proporciona dos opciones para las configuraciones de canal de salida:

-   salida de 8 canales (configuración de canal 7,1)
-   salida de 6 canales (configuración de canal 5,1)
-   Downmix estéreo

Si se selecciona Stereo downmix, el tipo de downmix se puede establecer en la MFT mediante la propiedad [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .

Si el tipo de salida es **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, cada búfer de salida contiene 6.144 bytes. El búfer se inicia con un encabezado S/PDIF de 8 bytes, seguido de un fotograma AC-3 comprimido, seguido de un relleno de cero a 6.144 bytes.

Si el tipo de salida es **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus**, cada búfer de salida contiene 24.576 bytes. El búfer se inicia con un encabezado S/PDIF de 8 bytes, seguido de 1 – 6 fotogramas Dolby Digital Plus comprimidos correspondientes a los ejemplos de 1.536 PCM, seguidos de un relleno de ceros a 24.576 bytes. Para la salida HDMI, solo se empaqueta el subflujo 0 independiente.

La MFT del descodificador se registra con la marca de **enumeración de MFT de marca \_ \_ \_ FIELDOFUSE**, que indica que el MFT debe desbloquearse por la aplicación antes de usarse. Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msauddecmft.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
