---
description: Microsoft MPEG Audio Decoder es una transformación sincrónica de Media Foundation (MFT) que permite descodificar formatos de secuencia elementales de audio MPEG mediante la canalización Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Descodificador de audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb908509f9c9f1c55ef7434b33d3265be875bf56443bc69c5a4cf829774bded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722285"
---
# <a name="mpeg-audio-decoder"></a>Descodificador de audio MPEG

Microsoft MPEG Audio Decoder [](media-foundation-transforms.md) es una transformación sincrónica de Media Foundation (MFT) que permite descodificar formatos de secuencias elementales de audio MPEG mediante la canalización Media Foundation (MF).

El descodificador admite los siguientes formatos de secuencia elemental MPEG.

-   Capas de audio MPEG-1 I y II (ISO/IEC 11172-3). 2. Compatible con versiones anteriores de MPEG-2, capas I y II (ISO)

-   COMPATIBLE con versiones anteriores de MPEG-2, capas I y II (ISO/IEC 13818-3), solo mono y estéreo

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador MPEG Audio es **CLSID \_ MSMPEGAudDecMFT**, definido en el archivo de encabezado wmcodecdsp.h.

## <a name="input-media-types"></a>Tipos de medios de entrada

El descodificador MPEG Audio admite los siguientes atributos de tipo de medio de entrada.



| Atributo                                                                               | Value                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                                                                                                                                                                                                                |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**CANALES \_ NUM \_ DE AUDIO \_ MF MT \_**](mf-mt-audio-num-channels-attribute.md)              | (Opcional) Normalmente, 1 para mono o 2 para estéreo, pero puede ser hasta 6 canales.<br/>                                                                                                                                                                                |
| [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)              | (Opcional) Normalmente 0x4 mono o 0x3 para estéreo, pero también puede ser cualquiera de las máscaras de canal asociadas a hasta 6 canales (3/2/1, 3/2, 3/1, 2/2, 2/1). Si está presente, la máscara de canal debe ser coherente con el número de entrada especificado de canales.<br/> |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md) | (Opcional) Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000. Si se especifica, la velocidad de muestreo de entrada debe ser una de las velocidades de muestreo MPEG válidas.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Tipos de medios de salida

El descodificador MPEG Audio admitirá hasta cuatro subtipos de medios de salida, en el orden siguiente.

<dl> 1. Estéreo, punto flotante.  
2. PCM estéreo de 16 bits.  
3. Mono, punto flotante (solo si la entrada es mono o dual-mono).  
4. Mono, PCM de 16 bits (solo si la entrada es mono o dual-mono).  
</dl>

El descodificador siempre admite la salida estéreo y se enumera como el primer tipo de medio de salida.

El descodificador admite los siguientes atributos de tipo de medio de salida.



| Atributo                                                                           | Value                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [TIPO \_ PRINCIPAL DE MT \_ DE \_ MF](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**                                                     |
| [\_SUBTIPO DE MT DE MF \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM o** **MFAudioFormat \_ Float**                  |
| [BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ MUESTRA](mf-mt-audio-bits-per-sample-attribute.md)       | 16 o 32                                                                   |
| [CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT](mf-mt-audio-num-channels-attribute.md)              | 1 o 2                                                                     |
| [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)              | 0x4 para mono o 0x3 para estéreo                                             |
| [MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md) | Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Transformar atributos

El descodificador MPEG Audio implementa el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Las aplicaciones pueden usar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                               | Descripción                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Especifica si el audio de 2 canales que se descodifica es mono dual o no. Solo lectura. Establecido por MFT. Para obtener más información, [**vea eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Especifica cómo el descodificador reproduce el audio mono dual. El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**.<br/> Lectura y escritura. Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado. Para obtener más información, [**vea eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Especifica la velocidad de bits de la secuencia comprimida. Solo lectura. Establecido por MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
