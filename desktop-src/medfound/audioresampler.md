---
description: El resampler de audio realiza una o ambas de las siguientes acciones en una secuencia de audio. Cambie la frecuencia de muestreo. Cambie el número de canales.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: DSP de remuestreador de audio (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf5e640ffd128a5b9249514284ecef16c5f57e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119420"
---
# <a name="audio-resampler-dsp"></a>Audio Resampler DSP

El resampler de audio realiza una o ambas de las siguientes acciones en una secuencia de audio.

-   Cambie la frecuencia de muestreo.
-   Cambie el número de canales.

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formatos

PUNTO FLOTANTE DE PCM o IEEE

El tipo de medio debe especificar un formato de audio de punto flotante o PCM sin comprimir.

-   Para la [**interfaz IMFTransform,**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) inicialice el tipo de medio como se describe en [Tipos de medios de audio sin comprimir](uncompressed-audio-media-types.md).
-   Para la [**interfaz IMediaObject,**](/previous-versions/ms785953%28v%3dvs.85%29) el tipo de medio debe ser **un tipo FORMAT \_ WaveFormatEx.** Para obtener más información, vea [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [ANCHO DE BANDA \_ \_ LOWPASS DE MFPKEY WMRESAMP \_](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Atributos necesarios

El resampler requiere que se establezcan los siguientes atributos en él:

-   [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)
-   [PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Asignación de canales personalizados

El resampler de audio asigna los canales de audio de entrada a los canales de audio de salida, en función de la siguiente información:

-   El número de canales. Esto se da en el atributo [MF MT AUDIO NUM \_ \_ \_ \_ CHANNELS](mf-mt-audio-num-channels-attribute.md) del tipo de medio, o en el **miembro nChannels** de la [estructura DESATEX.](mf-mt-audio-prefer-waveformatex-attribute.md)
-   Máscara de canal, que asigna canales a la posición del hablante. La máscara de canal se da en el atributo MF MT AUDIO CHANNEL MASK del tipo de medio, o en el miembro dwChannelMask de la estructura \_ \_ \_ \_ [**DESATEXTENSIBLE.**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) 
-   Matriz de ponderaciones de asignación.

La matriz contiene una serie de pesos, de forma que cada canal de salida es un promedio ponderado de los canales de entrada.

Puede especificar una matriz personalizada para la asignación de canales llamando a [**IWMResamplerProps::SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) o estableciendo la propiedad [**\_ MFPKEY WMRESAMP \_ CHANNELMTX.**](mfpkey-wmresamp-channelmtx.md) Si no se proporciona una matriz personalizada, Audio Resampler usa un conjunto de matrices predeterminadas.

## <a name="default-channel-mapping"></a>Asignación de canal predeterminada

Si no especifica una matriz personalizada, el DSP de Resampler de audio usa los valores predeterminados para la asignación de canales.

En las tablas siguientes, los canales se abrevian:

-   L: Izquierda
-   R: Derecha
-   C: Centro
-   LFE: Efectos de baja frecuencia
-   BL: Atrás a la izquierda
-   BR: Atrás a la derecha
-   SL: Rodear a la izquierda
-   SR: Rodear a la derecha

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 6 canales (máscara 0x3F) a 2 canales.



|     | L     | R     | C     | Lfe   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0,314 | 0     | 0,222 | 0.031 | 0,268 | 0.164 |
| **R**   | 0     | 0,314 | 0,222 | 0.031 | 0.164 | 0,268 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 6 canales (máscara 0x60F) a 2 canales.



|     | L     | R     | C     | Lfe   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0.320 | 0     | 0.226 | 0.032 | 0.292 | 0.130 |
| **R**   | 0     | 0.320 | 0.226 | 0.032 | 0.130 | 0.292 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 6 canales (máscara 0x3F o 0x60F) a 1 canal.



|     | L     | R     | C     | Lfe   | BL(SL) | BR(SR) |
|-----|-------|-------|-------|-------|--------|--------|
| **C**   | 0.192 | 0.192 | 0.192 | 0.038 | 0.192  | 0.192  |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (máscara 0x63F) a 2 canales.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0,222 | 0     | 0.157 | 0.022 | 0.189 | 0.116 | 0.203 | 0.090 |
| **R**   | 0     | 0,222 | 0.157 | 0.022 | 0.116 | 0.189 | 0.090 | 0.203 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (máscara 0x63F) a 1 canal.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **C**   | 0.139 | 0.139 | 0.139 | 0.028 | 0.139 | 0.139 | 0.139 | 0.139 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (máscara 0x63F) a 6 canales (máscara 0x3F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.518 | 0     | 0     | 0     | 0     | 0     | 0.189 | 0     |
| **R**   | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     | 0.189 |
| **C**   | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     |
| **BL**  | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 | 0     |
| **BR**  | 0     | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (máscara 0x63F) a 6 canales (máscara 0x60F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| **R**   | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     |
| **C**   | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     |
| **Sl**  | 0     | 0     | 0     | 0     | 0.429 | 0.124 | 0.447 | 0     |
| **SR**  | 0     | 0     | 0     | 0     | 0.124 | 0.429 | 0     | 0.447 |



 

Para entender cómo interpretar las tablas de coeficientes, considere la primera tabla, que asigna 6 canales a 2. La primera fila de la tabla (0,314, 0, 0,222, 0,031, 0,268, 0,164) es un vector de pesos que especifica la contribución de cada canal de entrada al canal izquierdo de la salida. La segunda fila de la tabla (0, 0,314, 0,222, 0,031, 0,164, 0,268) es un vector de pesos que especifica la contribución de cada canal de entrada al canal derecho de la salida.

Las fórmulas siguientes muestran cómo se calculan los canales de salida.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Si usa el DSP de resampler de audio para aumentar el número de canales, a los canales agregados se les asignarán valores de 0.

 

## <a name="output-quality"></a>Calidad de salida

Puede especificar la calidad de salida del DSP de resampler de audio llamando a [**IWMResamplerProps::SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) o estableciendo la propiedad [**\_ MFPKEY WMRESAMP \_ FILTERQUALITY.**](mfpkey-wmresamp-filterquality.md) Si no especifica la calidad de salida, el DSP de Resampler de audio usa un valor de calidad predeterminado de 30.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
