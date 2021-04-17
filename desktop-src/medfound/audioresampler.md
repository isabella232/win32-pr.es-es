---
description: El remuestreador de audio realiza una o las dos acciones siguientes en una secuencia de audio. Cambiar la frecuencia de muestreo. Cambiar el número de canales.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: DSP de remuestreador de audio (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698016"
---
# <a name="audio-resampler-dsp"></a>DSP de remuestreador de audio

El remuestreador de audio realiza una o las dos acciones siguientes en una secuencia de audio.

-   Cambiar la frecuencia de muestreo.
-   Cambiar el número de canales.

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formatos

PCM o punto flotante IEEE

El tipo de medio debe especificar un PCM sin comprimir o un formato de audio de punto flotante.

-   Para la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , inicialice el tipo de medio como se describe en [tipos de medios de audio sin comprimir](uncompressed-audio-media-types.md).
-   Para la interfaz [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) , el tipo de medio debe ser un tipo **\_ WaveFormatEx de formato** . Para obtener más información, consulte [**DMO \_ media \_ Type**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ paso bajo \_ ancho de banda](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Atributos necesarios

El remuestreador requiere que se establezcan los siguientes atributos:

-   [\_máscara de \_ canal de audio MF MT \_ \_](mf-mt-audio-channel-mask-attribute.md)
-   [\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [\_alineación del \_ bloque de audio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Asignación de canal personalizada

El remuestreador de audio asigna los canales de audio de entrada a los canales de audio de salida, en función de la siguiente información:

-   El número de canales. Esto se proporciona en el atributo [MF \_ MT \_ audio \_ NUM \_ Channels](mf-mt-audio-num-channels-attribute.md) del tipo de medio, o el miembro **nChannels** de la estructura [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .
-   La máscara del canal, que asigna los canales a la posición del altavoz. La máscara del canal se proporciona en el \_ \_ atributo de \_ máscara de canal de audio MF MT \_ del tipo de medio, o el miembro **dwChannelMask** de la estructura [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) .
-   Matriz de pesos de asignación.

La matriz contiene una serie de pesos, de modo que cada canal de salida es una media ponderada de los canales de entrada.

Puede especificar una matriz personalizada para la asignación de canales llamando a [**IWMResamplerProps:: SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) o estableciendo la propiedad [**MFPKEY \_ WMRESAMP \_ CHANNELMTX**](mfpkey-wmresamp-channelmtx.md) . Si no se proporciona una matriz personalizada, el remuestreador de audio utiliza un conjunto de matrices predeterminadas.

## <a name="default-channel-mapping"></a>Asignación de canal predeterminada

Si no especifica una matriz personalizada, el DSP de remuestreador de audio usa los valores predeterminados para la asignación de canal.

En las tablas siguientes, se abrevian los canales:

-   L: izquierda
-   R: derecha
-   C: Centro
-   LFE: efectos frecuencia bajos
-   BL: atrás a la izquierda
-   BR: atrás a la derecha
-   SL: hacia la izquierda
-   SR: envolvente derecha

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 6 canales (Mask 0x3F) a 2 canales.



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,314 | 0     | 0,222 | 0,031 | 0,268 | 0,164 |
| R   | 0     | 0,314 | 0,222 | 0,031 | 0,164 | 0,268 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 6 canales (Mask 0x60F) a 2 canales.



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,320 | 0     | 0,226 | 0,032 | 0,292 | 0,130 |
| R   | 0     | 0,320 | 0,226 | 0,032 | 0,130 | 0,292 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para la asignación de canales 6 (Mask 0x3F o 0x60F) a 1 canal.



|     | L     | R     | C     | LFE   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0,192 | 0,192 | 0,192 | 0,038 | 0,192  | 0,192  |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (Mask 0x63F) a 2 canales.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,222 | 0     | 0,157 | 0,022 | 0,189 | 0,116 | 0,203 | 0,090 |
| R   | 0     | 0,222 | 0,157 | 0,022 | 0,116 | 0,189 | 0,090 | 0,203 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (Mask 0x63F) a 1 canal.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0,139 | 0,139 | 0,139 | 0,028 | 0,139 | 0,139 | 0,139 | 0,139 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (Mask 0x63F) a 6 canales (Mask 0x3F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| R   | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| C   | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 |



 

En la tabla siguiente se muestran los coeficientes predeterminados para asignar 8 canales (Mask 0x63F) a 6 canales (Mask 0x60F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0,429 | 0,124 | 0,447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0,124 | 0,429 | 0     | 0,447 |



 

Para entender cómo interpretar las tablas de coeficientes, considere la primera tabla, que asigna 6 canales a 2. La primera fila de la tabla (0,314, 0, 0,222, 0,031, 0,268, 0,164) es un vector de pesos que especifica en qué medida contribuye cada canal de entrada al canal izquierdo de la salida. La segunda fila de la tabla (0, 0,314, 0,222, 0,031, 0,164, 0,268) es un vector de pesos que especifica en qué medida contribuye cada canal de entrada al canal adecuado de la salida.

En las fórmulas siguientes se muestra cómo se calculan los canales de salida.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Si usa el DSP de remuestreador de audio para aumentar el número de canales, se asignarán valores de 0 a los canales agregados.

 

## <a name="output-quality"></a>Calidad de salida

Puede especificar la calidad de salida del DSP del remuestreador de audio llamando a [**IWMResamplerProps:: SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) o estableciendo la propiedad [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY**](mfpkey-wmresamp-filterquality.md) . Si no especifica la calidad de salida, el DSP de remuestreador de audio usa un valor de calidad predeterminado de 30.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
