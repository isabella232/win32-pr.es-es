---
description: El codificador de audio MPEG-2 Microsoft Media Foundation es una transformación Media Foundation que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o MPEG-2 (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908377"
---
# <a name="mpeg-2-audio-encoder"></a>Codificador de audio MPEG-2

El codificador de audio MPEG-2 Microsoft Media Foundation es una [transformación Media Foundation](media-foundation-transforms.md) que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o MPEG-2 (ISO/IEC 13818-3).

El codificador admite el audio de nivel 1 y nivel 2. No admite audio de MPEG-Layer 3 (MP3). En MPEG-2, el codificador admite la parte de bajas frecuencias de muestreo (LSF) del audio MPEG-2. No es compatible con las extensiones multicanal. La MFT genera una secuencia MPEG elemental. No puede generar secuencias elementales con paquetes, secuencias de programa o flujos de transporte.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador de audio MEPG-2 es **CLSID \_ CMPEG2AudioEncoderMFT**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="output-types"></a>Tipos de salida

Primero se debe establecer el tipo de salida, antes del tipo de entrada. En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.



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
<td>Obligatorio. Debe ser <strong>MFAudioFormat_MPEG</strong>. Este subtipo se usa para audio MPEG-1 y MPEG-2.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Muestras por segundo.</td>
<td>Obligatorio. En MPEG-1 y MPEG-2 se admiten los siguientes valores:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Además, se admiten los siguientes valores para MPEG-2 LSF: <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales.</td>
<td>Obligatorio. Debe ser 1 (mono) o 2 (estéreo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Si se establece, el valor debe ser 0X3 para los canales estéreo (Front izquierdo y derecho) o 0x4 para mono (canal de centro frontal).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocidad de bits de la secuencia MPEG codificada, en bytes por segundo.</td>
<td>Opcional.<br/> Las especificaciones ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definen varias velocidades de bits, en función de la frecuencia de muestreo, el número de canales y la capa de audio (1 o 2). <br/> El codificador tiene como valor predeterminado el audio de nivel 2. Si no se establece el atributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> , el codificador utiliza las siguientes velocidades de bits predeterminadas:<br/>
<ul>
<li>MPEG-1 estéreo: 224.000 bits por segundo (BPS) = 28.000 bytes por segundo.</li>
<li>MPEG-1 mono: 192.000 BPS = 24.000 bytes por segundo.</li>
<li>MPEG-2 LSF, mono o estéreo: 160.000 BPS = 20.000 bytes por segundo.</li>
</ul>
Este atributo se puede establecer en otros valores. Si el valor no es válido de acuerdo con las especificaciones de MPEG, el MFT rechazará el tipo de medio.<br/> También puede establecer la velocidad de bits mediante la interfaz <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> . Vea Comentarios para obtener más información.<br/></td>
</tr>
</tbody>
</table>



 

Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="input-types"></a>Tipos de entrada

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.



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
<td>Obligatorio. Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Número de bits por muestra de audio.</td>
<td>Obligatorio. El valor debe ser 16 si el subtipo es <strong>MFAudioFormat_PCM</strong>, o 32 si el subtipo es <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Muestras por segundo.</td>
<td>Obligatorio. Debe coincidir con el tipo de salida.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canales.</td>
<td>Obligatorio. Debe coincidir con el tipo de salida.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alineación de bloque, en bytes.</td>
<td>Obligatorio. Calcule el valor de la siguiente manera:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: número de canales × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: número de canales × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocidad de bits de la secuencia de AC3s codificada, en bytes por segundo.</td>
<td>Obligatorio. Debe ser igual que la alineación de bloque × ejemplos por segundo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica la asignación de canales de audio a las posiciones del hablante.</td>
<td>Opcional. Si se establece, el valor debe coincidir con el tipo de salida.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Número de bits válidos de datos de audio en cada ejemplo de audio.</td>
<td>Opcional. Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

El codificador no admite la conversión de velocidad de muestra o la conversión estéreo/mono. Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="codec-properties"></a>Propiedades de códec

El codificador admite las siguientes propiedades a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .



| Propiedad                                                                                | Descripción                                                                                      | Valor predeterminado                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Especifica la velocidad media de bits codificada, en bits por segundo.                                      | Tal y como se describe en el atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Especifica el modo de codificación de audio MPEG.                                                          | Estéreo para audio de 2 canales o canal único para audio de un canal.<br/> En el caso de audio de 2 canales, el codificador también admite canal dual y estéreo en conjunto.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Especifica si se debe establecer el bit de copyright en la secuencia de audio MPEG.                             | Sin derechos de autor.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Especifica el tipo de filtro de desacentuación que se debe usar cuando se descodifica el flujo codificado. | No se ha especificado ningún énfasis.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco.                    | Una suma de comprobación de CRC se escribe en la secuencia de bits.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Especifica la capa de audio MPEG.                                                                  | Audio de nivel 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Especifica si se va a establecer para el bit original de la secuencia de audio MPEG.                          | El bit "original" está desactivado.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Especifica si se debe establecer para el bit de usuario privado en la secuencia de audio MPEG.                      | El bit de usuario privado está desactivado.                                                                                                                                               |



 

Para obtener un puntero a la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , llame a [**QUERYINTERFACE**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la MFT.

MFT implementa los siguientes métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Todos los demás métodos de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) devuelven **E \_ NOTIMPL**.

## <a name="remarks"></a>Observaciones

Cada fotograma de audio MPEG contiene muestras de audio de 384 (capa 1) o 1152 (capa 2) por canal. Sin embargo, cada búfer de entrada del codificador puede contener cualquier número de muestras de PCM. El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque. El codificador almacena en caché los ejemplos de entrada hasta que sea suficiente para una trama de audio MPEG.

Cada búfer de salida contiene un fotograma MPEG sin formato. El tamaño de cada búfer de salida depende de la velocidad de bits y la velocidad de muestra.

### <a name="configuring-the-encoder"></a>Configurar el codificador

Para cambiar cualquiera de las opciones de configuración predeterminadas del codificador, realice los pasos siguientes:

1.  Cree una instancia de la MFT del codificador.
2.  Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener la lista de los tipos de salida preferidos. El codificador enumera todas las velocidades de muestra para mono y estéreo. Seleccione uno de estos tipos de medios, en función de la velocidad de muestra y el número de canales. El atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocidad de bits predeterminada, en bytes por segundo.
3.  Opcional: puede invalidar la velocidad de bits predeterminada si establece un nuevo valor para [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida. Las velocidades de bits válidas dependen de la velocidad de muestra, el número de canales y el nivel de audio.
    > [!Note]  
    > En este punto del proceso de configuración, el codificador tiene como valor predeterminado audio de nivel 2 y solo acepta velocidades de bits de capa 2. Podrá cambiar el codificador a la capa 1 en un paso posterior (consulte el paso 7). En ese caso, deje la velocidad de bits predeterminada por ahora; puede cambiarla de nuevo en el paso 8.

     

4.  Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de salida. Si establece su propio valor para [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) y el MFT rechaza el tipo de medio de salida, es probable que haya especificado una velocidad de bits no válida.
5.  Llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para enumerar el tipo de medio de entrada. Dado que la velocidad de muestra y el número de canales deben ser idénticos al tipo de salida, solo se enumeran dos opciones: entrada PCM de punto flotante de 32 bits y entrada PCM de 16 bits. Seleccione una de estas opciones.
6.  Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el tipo de medio de entrada.
7.  Opcional: para codificar el audio de nivel 1, establezca la propiedad [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) en **eAVEncMPALayer \_ 1**.
8.  Opcional: para cambiar la velocidad de bits, establezca la propiedad [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . La velocidad de bits debe ser una de las velocidades de bits válidas que se enumeran en las especificaciones de LSF MPEG-1 o MPEG-2. Como alternativa, puede llamar a [**ICodecAPI:: GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obtener una lista de velocidades de bits válidas, basándose en la configuración actual.
9.  Opcional: con audio de 2 canales, puede establecer la propiedad [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para cambiar el modo de codificación a canal dual o estéreo en conjunto. Puede llamar a [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obtener las opciones válidas. (Para audio de un canal, la única opción es mono).
10. Opcional: establezca cualquiera de las demás propiedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) enumeradas previamente.

Es importante seguir el orden de estos pasos. En concreto, establezca el tipo de medio de salida antes de cambiar las propiedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Además, debe establecer las propiedades de **ICodecAPI** antes de que el MFT reciba la primera muestra de entrada. Después de que el MFT reciba entradas, las propiedades del códec son de solo lectura y [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) devuelve el valor **S \_ false**.

### <a name="supported-bit-rates"></a>Velocidades de bits admitidas

El codificador admite las siguientes velocidades de bits.



MPEG-1

MPEG-2

Nivel 1

Nivel 2

Nivel 1

Nivel 2

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Solo mono  
\*\* Solo estéreo  
</dl>

### <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo de los tipos de medios que se necesitan para codificar el PCM de entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada.

Tipo de medio de salida:

| Atributo                                                                           | Value                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**  |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Tipo de medio de entrada:

| Atributo                                                                                | Value                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ MT \_ audio \_ bits \_ por \_ muestra](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_alineación del \_ bloque de audio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
