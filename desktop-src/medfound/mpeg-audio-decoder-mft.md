---
description: El descodificador de audio MPEG de Microsoft es una transformación de Media Foundation sincrónica (MFT) que permite descodificar formatos de secuencia elementales de audio MPEG mediante la canalización de Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Descodificador de audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001449"
---
# <a name="mpeg-audio-decoder"></a>Descodificador de audio MPEG

El descodificador de audio MPEG de Microsoft es una [transformación de Media Foundation](media-foundation-transforms.md) sincrónica (MFT) que permite descodificar formatos de secuencia elementales de audio MPEG mediante la canalización de Media Foundation (MF).

El descodificador admite los siguientes formatos de flujo elemental de MPEG.

-   MPEG-1 capas de audio I y II (ISO/IEC 11172-3). 2. MPEG-2 compatible con versiones anteriores, las capas I y II (ISO

-   MPEG-2 compatible con versiones anteriores, las capas I y II (ISO/IEC 13818-3), mono y estéreo únicamente

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador de audio MPEG es **CLSID \_ MSMPEGAudDecMFT**, definido en el archivo de encabezado wmcodecdsp. h.

## <a name="input-media-types"></a>Tipos de medios de entrada

El descodificador de audio MPEG admite los siguientes atributos de tipo de medio de entrada.



| Atributo                                                                               | Value                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**                                                                                                                                                                                                                                                |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)              | Opta Normalmente 1 para mono o 2 para estéreo, pero puede tener hasta 6 canales.<br/>                                                                                                                                                                                |
| [**\_máscara de \_ canal de audio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)              | Opta Normalmente, 0x4 para mono o 0X3 para estéreo, pero también puede ser cualquiera de las máscaras de canal asociadas a un máximo de 6 canales (3/2/1, 3/2, 3/1, 2/2, 2/1). Si está presente, la máscara de canal debe ser coherente con el número de canales de entrada especificado.<br/> |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) | Opta Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000. Si se especifica, la frecuencia de muestreo de entrada debe ser una de las velocidades de muestreo de MPEG válidas.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Tipos de medios de salida

El descodificador de audio MPEG admitirá hasta cuatro subtipos de medios de salida, en el orden siguiente.

<dl> 1. Estéreo, punto flotante.  
2. PCM de 16 bits estéreo.  
3. Mono, punto flotante (solo si la entrada es mono o dual mono).  
4. Mono de 16 bits, PCM (solo si la entrada es mono o dual mono).  
</dl>

El descodificador siempre admite la salida estéreo y se enumera como el primer tipo de medio de salida.

El descodificador admite los siguientes atributos de tipo de medio de salida.



| Atributo                                                                           | Value                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**                                                     |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** o **MFAudioFormat \_ float**                  |
| [MF \_ MT \_ audio \_ bits \_ por \_ muestra](mf-mt-audio-bits-per-sample-attribute.md)       | 16 o 32                                                                   |
| [\_canales de \_ número de audio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 1 o 2                                                                     |
| [\_máscara de \_ canal de audio MF MT \_ \_](mf-mt-audio-channel-mask-attribute.md)              | 0x4 para mono o 0X3 para estéreo                                             |
| [\_muestras de audio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | Uno de los siguientes: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Atributos de transformación

El descodificador de audio MPEG implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                               | Descripción                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Especifica si el audio de 2 canales que se está descodificando es dual mono o no. Solo lectura. Establecido por la MFT. Para obtener más información, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Especifica cómo el descodificador Reproduce audio mono dual. El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ \_** a la izquierda.<br/> Lectura y escritura. Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado. Para obtener más información, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Especifica la velocidad de bits de flujo comprimido. Solo lectura. Establecido por la MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
