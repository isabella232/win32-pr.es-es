---
description: El descodificador de vídeo MPEG-2 es una transformación Media Foundation que descodifica vídeo MPEG-1 y MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Descodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543894"
---
# <a name="mpeg-2-video-decoder"></a>Descodificador de vídeo MPEG-2

El descodificador de vídeo MPEG-2 es una [transformación Media Foundation](media-foundation-transforms.md) que DESCODIFICA vídeo MPEG-1 y MPEG-2. El descodificador admite el vídeo MPEG-2 simple y el perfil principal (H. 262, ISO/IEC 13818-2) y MPEG-1 (ISO/IEC 11172-2).

## <a name="input-types"></a>Tipos de entrada

El descodificador admite los siguientes tipos de medios de entrada.

| Atributo                                                 | Descripción                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo de MFMediaType \_**                                                  |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes tipos de salida.

| Atributo                                                 | Descripción                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo de MFMediaType \_**                                                                                                                                                         |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ i420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Observaciones

El descodificador de vídeo MPEG-2 expone las siguientes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

La entrada para el descodificador debe ser una secuencia elemental. La resolución máxima admitida es 1920 × 1088 píxeles.

El descodificador es compatible con DirectX video Acceleration (DXVA) mediante Microsoft Direct3D 9 o Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modos de descodificación especiales

-   **Modo de baja latencia.** Este modo es adecuado para escenarios como las comunicaciones en tiempo real. Reduce la latencia de inicio, por lo que el descodificador genera el primer ejemplo de salida antes. Sin embargo, el descodificador almacena menos muestras en este modo, lo que puede provocar problemas, porque el descodificador no descodifica tantas tramas de antemano. Para habilitar el modo de baja latencia, establezca el atributo [ \_ AVLowLatencyMode de CODECAPI](codecapi-avlowlatencymode.md) .
-   **Invoca.** Para una búsqueda precisa, llame al método [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) . Cuando se llama a este método, el descodificador solo genera fotogramas que se encuentran dentro del intervalo de marcas de tiempo especificado por el llamador.
-   **Modo de generación de miniaturas**. Este modo está diseñado para la generación rápida de imágenes en miniatura. En este modo, el descodificador descodifica inicialmente solo I fotogramas. Si no se encuentra ningún fotograma I dentro de un número determinado de fotogramas, el descodificador inicia la descodificación de los fotogramas P y genera las tramas que no son I en un intervalo fijo (uno por *N* imágenes) hasta que se alcanza un fotograma I. Para habilitar el modo de generación de miniaturas, establezca la propiedad [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .
-   **Juegue.** El descodificador puede descodificar a velocidades más rápido que en tiempo real. Con una velocidad de reproducción mayor, el descodificador cambiará a descodificar solo I fotogramas. Para la reproducción inversa, solo se descodifican las tramas I.

### <a name="codec-properties"></a>Propiedades de códec

El descodificador admite las siguientes propiedades a través del método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .



| Propiedad                                                                                                      | Descripción                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Habilita o deshabilita el modo de generación de miniaturas.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Habilita o deshabilita la descodificación acelerada de hardware.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita o deshabilita el modo de baja latencia.                                                                      |
| [el \_ DEScodificador \_ de MFT expone \_ \_ tipos \_ de salida en \_ \_ orden nativo](mft-decoder-expose-output-types-in-native-order.md) | Especifica si el descodificador expone los tipos de salida adecuados para la transcodificación antes de otros formatos. |



 

De estas propiedades, también se pueden establecer las siguientes opciones a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limitaciones

-   El descodificador no se admite en las plataformas basadas en IA-64.
-   El descodificador no admite el descifrado de CSS ni la reproducción de DVDs cifrados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
