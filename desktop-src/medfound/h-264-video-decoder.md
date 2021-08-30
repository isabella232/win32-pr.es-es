---
description: El descodificador de vídeo Media Foundation H.264 es una transformación de Media Foundation que admite la descodificación de perfiles de línea de base, principal y alto, hasta el nivel 5.1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Descodificador de vídeo H.264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4488328fed3fe6a46feabb7eac99761ee673c3f4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468852"
---
# <a name="h264-video-decoder"></a>Descodificador de vídeo H.264

El descodificador de vídeo Media Foundation H.264 es una transformación de [Media Foundation](media-foundation-transforms.md) que admite la descodificación de perfiles de línea de base, principal y alto, hasta el nivel 5.1.

El descodificador de vídeo H.264 expone las interfaces siguientes.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para crear una instancia del descodificador, realice una de las acciones siguientes:

-   Llame a [**la función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) [**o MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
-   Llame [**a CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) El CLSID del descodificador es **CLSID \_ CMSH264DecoderMFT,** declarado en wmcodecdsp.h.

## <a name="input-types"></a>Tipos de entrada

El tipo de entrada debe contener al menos los dos atributos siguientes:



| Atributo                                                 | Descripción                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MF MT \_ \_**](mf-mt-major-type-attribute.md) | **VÍDEO \_ MFMediaType**                                                                        |
| [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ H264](video-subtype-guids.md) o MFVideoFormat \_ H264 \_ ES |



 

Si el tipo de entrada contiene solo estos dos atributos, el descodificador ofrecerá un tipo de salida predeterminado, que actúa como marcador de posición. Cuando el descodificador recibe suficientes muestras de entrada para generar un marco de salida, señala un cambio de formato devolviendo **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE** de [**MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Consulte la **documentación de ProcessOutput** para obtener más información sobre cómo controlar los cambios de formato.

Para evitar un cambio de formato inicial, proporcione tanta información en el tipo de entrada como sea posible, como:




| Atributo | Descripción | 
|-----------|-------------|
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Velocidad de fotogramas. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Dimensiones de marco. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modo de interlace.<blockquote>[!Note]<br />En el vídeo H.264, la estructura de interlace puede cambiar dinámicamente, por lo que el valor recomendado de este <strong>atributo MFVideoInterlace_MixedInterlaceOrProgressive</strong>. La información de intercalación en la secuencia elemental de vídeo tiene prioridad sobre el tipo de medio. Para obtener más información, vea <a href="video-interlacing.md">Video Interlacing</a>.</blockquote><br /><br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Relación de aspecto de píxeles. | 




 

El tipo de entrada debe establecerse antes que el tipo de salida. Hasta que se establece el tipo de entrada, el método [**MFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) del codificador devuelve **MF E TRANSFORM TYPE NOT \_ \_ \_ \_ \_ SET**.

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes subtipos de salida:

-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obtener más información sobre estos subtipos, vea [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Transformar atributos

El descodificador H.264 implementa el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Las aplicaciones pueden usar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | Habilita o deshabilita la aceleración de hardware.                                                 |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                             |
| [MF \_ SA \_ D3D \_ AWARE](mf-sa-d3d-aware-attribute.md)                                             | Indica que el descodificador admite la aceleración de vídeo de DirectX (DXVA). Tratar como de solo lectura. |



 

En Windows 8, el descodificador H.264 también admite los atributos siguientes.



| Atributo                                                                                                     | Descripción                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita o deshabilita el modo de decodificación de baja latencia.                                                              |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | Establece el número de subprocesos de trabajo utilizados por el descodificador.                                                      |
| [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Establece el ancho máximo de imagen que el descodificador aceptará como tipo de entrada.                               |
| [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | Establece el alto máximo de la imagen que el descodificador aceptará como tipo de entrada.                              |
| [RECUENTO \_ MÍNIMO DE MUESTRAS DE SALIDA \_ \_ \_ DE \_ MF SA](mf-sa-minimum-output-sample-count.md)                               | Especifica el número máximo de muestras de salida.                                                             |
| [EL DESCODIFICADOR DE MFT \_ EXPONE LOS TIPOS DE SALIDA EN ORDEN \_ \_ \_ \_ \_ \_ NATIVO](mft-decoder-expose-output-types-in-native-order.md) | Especifica si un descodificador expone tipos de salida IYUV/I420 (adecuados para la transcodificación) antes que otros formatos. |



 

En Windows 8, el descodificador H.264 admite la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi) Esta interfaz proporciona una API alternativa para establecer las siguientes propiedades de códec.

-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Restricciones de formato

El descodificador admite los siguientes formatos:




| | | Perfiles o niveles | Perfiles de línea base, principal y alto, hasta el nivel 5.1. (Consulte la especificación ITU-T H.264 para obtener más información). | | Formatos de | 4:2:0 grama o monocroma | | Resolución mínima | 48 × 48 píxeles | | Resolución máxima | 4096 × 2304 píxeles<br /> La resolución máxima garantizada para la aceleración dxva es de 1920 × 1088 píxeles; a resoluciones más altas, la descodización se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, lacodización se realiza con software.<br /><blockquote>[!Note]<br />En Windows 7, la resolución máxima admitida es de 1920 × 1088 píxeles tanto para el software como para la decodificación de DXVA.</blockquote><br /><br /> | | | DXVA El descodificador admite DXVA versión 2, pero no DXVA versión 1. Lacoding dxva solo se admite para las secuencias de bits de perfil principal, principal y de perfil alto compatibles. (Las secuencias de bits de línea de base compatibles con main se definen <strong>profile_idc</strong>=66 <strong>y constrained_set1_flag</strong>=1). | 




 

Los datos de entrada deben cumplir el anexo B de ISO/IEC 14496-10. Los datos deben incluir los códigos de inicio. El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) válido y un conjunto de parámetros de imagen (PPS) en la secuencia de bytes.

El descodificador no es compatible con la tecnología De película.

> [!Note]  
> Una versión anterior de la documentación indicaba incorrectamente que el descodificador se admite en Windows Server 2008 R2.

 

Si el complemento de actualización de plataforma para Windows Vista está instalado, el descodificador de vídeo H.264 está disponible en Windows Vista, pero solo es accesible en Windows Vista mediante el Lector de origen [.](source-reader.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 
