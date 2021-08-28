---
description: El codificador de audio Microsoft Media Foundation MPEG-2 es una transformación Media Foundation que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o audio MPEG-2 (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c75956f55dfa22034b27465082ced0888fbe03b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475541"
---
# <a name="mpeg-2-audio-encoder"></a>Codificador de audio MPEG-2

El codificador de audio Microsoft Media Foundation MPEG-2 es una transformación [de Media Foundation](media-foundation-transforms.md) que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o audio MPEG-2 (ISO/IEC 13818-3).

El codificador admite audio de capa 1 y de capa 2. No admite audio MPEG-Layer 3 (MP3). Para MPEG-2, el codificador admite la parte Frecuencias de muestreo baja (LSF) del audio MPEG-2. No admite las extensiones multicanal. El MFT genera una secuencia elemental MPEG. No puede generar secuencias elementales en paquetes, secuencias de programa o secuencias de transporte.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador de audio MEPG-2 es **\_ CLSID CMPEG2AudioEncoderMFT,** definido en el archivo de encabezado wmcodecdsp.h.

## <a name="output-types"></a>Tipos de salida

El tipo de salida debe establecerse primero, antes del tipo de entrada. En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Debe ser <strong>MFAudioFormat_MPEG</strong>. Este subtipo se usa para el audio MPEG-1 y MPEG-2. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Ejemplos por segundo. | Necesario. Se admiten los siguientes valores para MPEG-1 y MPEG-2:<ul><li>32000</li><li>44100</li><li>48000</li></ul>Además, se admiten los siguientes valores para MPEG-2 LSF: <br /><ul><li>16000</li><li>22050</li><li>24000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales. | Necesario. Debe ser 1 (mono) o 2 (estéreo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Si se establece, el valor debe ser 0x3 para estéreo (canales front-left y right) o 0x4 para mono (canal front-center). | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocidad de bits de la secuencia MPEG codificada, en bytes por segundo. | Opcional.<br /> Las especificaciones ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definen varias velocidades de bits, en función de la frecuencia de muestreo, el número de canales y la capa de audio (1 o 2). <br /> El codificador tiene como valor predeterminado audio de capa 2. Si el <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> no está establecido, el codificador usa las siguientes velocidades de bits predeterminadas:<br /><ul><li>MPEG-1 estéreo: 224 000 bits por segundo (bps) = 28 000 bytes por segundo.</li><li>MPEG-1 mono: 192 000 bps = 24 000 bytes por segundo.</li><li>MPEG-2 LSF, mono o estéreo: 160 000 bps = 20 000 bytes por segundo.</li></ul>Este atributo se puede establecer en otros valores. Si el valor no es válido según las especificaciones mpeg, MFT rechazará el tipo de medio.<br /> También puede establecer la velocidad de bits mediante la <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>interfaz ICodecAPI.</strong></a> Vea Comentarios para obtener más información.<br /> | 




 

Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="input-types"></a>Tipos de entrada

En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.




| Atributo | Descripción | Observaciones | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Necesario. Debe ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de audio. | Necesario. Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Número de bits por muestra de audio. | Necesario. El valor debe ser 16 si el subtipo es <strong>MFAudioFormat_PCM</strong>o 32 si el subtipo es <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Ejemplos por segundo. | Necesario. Debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canales. | Necesario. Debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Alineación de bloques, en bytes. | Necesario. Calcule el valor de la siguiente manera:<ul><li><strong>MFAudioFormat_PCM:</strong>número de canales × 2.</li><li><strong>MFAudioFormat_Float:</strong>número de canales × 4.</li></ul> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Velocidad de bits de la secuencia AC3 codificada, en bytes por segundo. | Necesario. Debe ser igual a la alineación × muestras por segundo. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica la asignación de canales de audio a las posiciones del hablante. | Opcional. Si se establece, el valor debe coincidir con el tipo de salida. | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Número de bits válidos de datos de audio en cada muestra de audio. | Opcional. Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>. | 




 

El codificador no admite la conversión de frecuencia de muestreo ni la conversión estéreo/mono. Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.

## <a name="codec-properties"></a>Propiedades del códec

El codificador admite las siguientes propiedades a través de la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)



| Propiedad                                                                                | Descripción                                                                                      | Valor predeterminado                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Especifica la velocidad de bits codificada media, en bits por segundo.                                      | Como se describe para el atributo [MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Especifica el modo de codificación de audio MPEG.                                                          | Estéreo para audio de 2 canales o canal único para audio de 1 canal.<br/> En el caso del audio de 2 canales, el codificador también admite doble canal y estéreo conjunto.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Especifica si se debe establecer el bit de copyright en la secuencia de audio MPEG.                             | Sin copyright.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Especifica el tipo de filtro de des-énfasis que se debe usar cuando se descodifica la secuencia codificada. | No se ha especificado ningún énfasis.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Especifica si se va a agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco.                    | Se escribe una suma de comprobación CRC en la secuencia de bits.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Especifica la capa de audio MPEG.                                                                  | Audio de capa 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Especifica si se debe establecer para el bit original en la secuencia de audio MPEG.                          | El bit "Original" está desactivado.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Especifica si se debe establecer para el bit de usuario privado en la secuencia de audio MPEG.                      | El bit de usuario privado está desactivado.                                                                                                                                               |



 

Para obtener un puntero a la [**interfaz ICodecAPI,**](/windows/win32/api/strmif/nn-strmif-icodecapi) llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en MFT.

MFT implementa los siguientes métodos [**ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Todos los demás [**métodos ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) **devuelven E \_ NOTIMPL**.

## <a name="remarks"></a>Comentarios

Cada fotograma de audio MPEG contiene 384 (capa 1) o 1152 (capa 2) muestras de audio por canal. Sin embargo, cada búfer de entrada al codificador puede contener cualquier número de muestras de PCM. El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque. El codificador almacena en caché los ejemplos de entrada hasta que tiene suficiente para un fotograma de audio MPEG.

Cada búfer de salida contiene un marco MPEG sin formato. El tamaño de cada búfer de salida depende de la velocidad de bits y la frecuencia de muestreo.

### <a name="configuring-the-encoder"></a>Configuración del codificador

Para cambiar cualquiera de los valores predeterminados en el codificador, realice los pasos siguientes:

1.  Cree una instancia de MFT del codificador.
2.  Llame [**a IMFTransform::GetOutputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) obtener la lista de los tipos de salida preferidos. El codificador enumera todas las velocidades de muestreo para mono y estéreo. Seleccione uno de estos tipos de medios, en función de la frecuencia de muestreo y el número de canales. El [atributo MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocidad de bits predeterminada, en bytes por segundo.
3.  Opcional: puede invalidar la velocidad de bits predeterminada estableciendo un nuevo valor para [MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida. Las velocidades de bits válidas dependen de la frecuencia de muestreo, el número de canales y la capa de audio.
    > [!Note]  
    > En este punto del proceso de configuración, el codificador tiene como valor predeterminado audio de capa 2 y solo aceptará velocidades de bits de nivel 2. Podrá cambiar el codificador a Capa 1 en un paso posterior (consulte el paso 7). En ese caso, deje la velocidad de bits predeterminada por ahora; puede cambiarlo de nuevo en el paso 8.

     

4.  Llame [**a IMFTransform::SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) establecer el tipo de medio de salida. Si establece su propio valor para [MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) y MFT rechaza el tipo de medio de salida, es probable que se deba a que especificó una velocidad de bits no válida.
5.  Llame [**a IMFTransform::GetInputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) enumerar el tipo de medio de entrada. Dado que la frecuencia de muestreo y el número de canales deben ser idénticos al tipo de salida, solo se enumeran dos opciones: entrada PCM de punto flotante de 32 bits y entrada PCM de entero de 16 bits. Seleccione uno de ellos.
6.  Llame [**a IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) establecer el tipo de medio de entrada.
7.  Opcional: para codificar audio de capa 1, establezca la propiedad [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) en **eAVEncMPALayer \_ 1.**
8.  Opcional: para cambiar la velocidad de bits, establezca la [propiedad CODECAPI \_ AVEncCommonMeanBitRate.](../directshow/avenccommonmeanbitrate-property.md) La velocidad de bits debe ser una de las velocidades de bits válidas enumeradas en las especificaciones de LSF MPEG-1 o MPEG-2. Como alternativa, puede llamar a [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obtener una lista de velocidades de bits válidas, en función de la configuración actual.
9.  Opcional: con audio de 2 canales, puede establecer la propiedad [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para cambiar el modo de codificación a doble canal o estéreo conjunto. Puede llamar a [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obtener las opciones válidas. (Para el audio de 1 canal, la única opción es mono).
10. Opcional: establezca cualquiera de las otras [**propiedades de ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) enumeradas anteriormente.

Es importante seguir el orden de estos pasos. En concreto, establezca el tipo de medio de salida antes de cambiar las [**propiedades de ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi) Además, debe establecer las **propiedades de ICodecAPI** antes de que MFT reciba el primer ejemplo de entrada. Una vez que MFT recibe la entrada, las propiedades del códec son de solo lectura e [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) devuelve el valor **S \_ FALSE.**

### <a name="supported-bit-rates"></a>Velocidades de bits admitidas

El codificador admite las siguientes velocidades de bits.



MPEG-1

MPEG-2

Capa 1

Capa 2

Capa 1

Capa 2

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



 

<dl> \* Solo Mono  
\*\* Solo estéreo  
</dl>

### <a name="example-media-types"></a>Tipos de medios de ejemplo

Este es un ejemplo de los tipos de medios necesarios para codificar un PCM entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada.

Tipo de medio de salida:

| Atributo                                                                           | Valor                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**  |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Tipo de medio de entrada:

| Atributo                                                                                | Valor                  |
|------------------------------------------------------------------------------------------|------------------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ MUESTRA](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
