---
description: El descodificador de vídeo H. 264 Media Foundation es una transformación de Media Foundation que admite la descodificación de perfiles de línea base, principales y altos, hasta el nivel 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Descodificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496793"
---
# <a name="h264-video-decoder"></a>Descodificador de vídeo H. 264

El descodificador de vídeo H. 264 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la descodificación de perfiles de línea base, principales y altos, hasta el nivel 5,1.

El descodificador de vídeo H. 264 expone las siguientes interfaces.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para crear una instancia del descodificador, realice una de las acciones siguientes:

-   Llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). El CLSID para el descodificador es **CLSID \_ CMSH264DecoderMFT**, declarado en wmcodecdsp. h.

## <a name="input-types"></a>Tipos de entrada

El tipo de entrada debe contener al menos los dos atributos siguientes:



| Atributo                                                 | Descripción                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo de MFMediaType \_**                                                                        |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ H264](video-subtype-guids.md) o MFVideoFormat \_ H264 \_ es |



 

Si el tipo de entrada contiene solo estos dos atributos, el descodificador ofrecerá un tipo de salida predeterminado, que actúa como marcador de posición. Cuando el descodificador recibe suficientes ejemplos de entrada para generar un fotograma de salida, indica un cambio de formato devolviendo el **cambio de secuencia de \_ \_ transformación \_ \_ MF E** de [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Consulte la documentación de **ProcessOutput** para obtener más información sobre el control de los cambios de formato.

Para evitar un cambio de formato inicial, proporcione tanta información como sea posible en el tipo de entrada, entre las que se incluyen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Velocidad de fotogramas.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Dimensiones del marco.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modo entrelazado.
<blockquote>
[!Note]<br />
En el vídeo H. 264, la estructura entrelazada puede cambiar dinámicamente, por lo que el valor recomendado de este atributo es <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>. La información de entrelazado en el flujo elemental de vídeo tiene prioridad sobre el tipo de medio. Para obtener más información, vea <a href="video-interlacing.md">entrelazado de vídeo</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Relación de aspecto de píxeles.</td>
</tr>
</tbody>
</table>



 

El tipo de entrada debe establecerse antes que el tipo de salida. Hasta que se establezca el tipo de entrada, el método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) del codificador devuelve el **tipo de \_ transformación MF E \_ \_ \_ no \_ establecido**.

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes subtipos de salida:

-   **MFVideoFormat \_ i420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Atributos de transformación

El descodificador H. 264 implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | Habilita o deshabilita la aceleración de hardware.                                                 |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                             |
| [Compatible con el D3D de MF \_ SA \_ \_](mf-sa-d3d-aware-attribute.md)                                             | Indica que el descodificador admite la aceleración de vídeo de DirectX (DXVA). Tratar como de solo lectura. |



 

En Windows 8, el descodificador H. 264 también admite los siguientes atributos.



| Atributo                                                                                                     | Descripción                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Habilita o deshabilita el modo de descodificación de latencia baja.                                                              |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | Establece el número de subprocesos de trabajo utilizados por el descodificador.                                                      |
| [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Establece el ancho máximo de la imagen que el descodificador aceptará como tipo de entrada.                               |
| [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | Establece el alto máximo de la imagen que el descodificador aceptará como tipo de entrada.                              |
| [recuento de \_ \_ ejemplo de salida mínima de SA de \_ \_ MF \_](mf-sa-minimum-output-sample-count.md)                               | Especifica el número máximo de ejemplos de salida.                                                             |
| [el \_ DEScodificador \_ de MFT expone \_ \_ tipos \_ de salida en \_ \_ orden nativo](mft-decoder-expose-output-types-in-native-order.md) | Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos. |



 

En Windows 8, el descodificador H. 264 admite la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Esta interfaz proporciona una API alternativate para configurar las siguientes propiedades de códec.

-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Restricciones de formato

El descodificador admite los siguientes formatos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Perfiles/niveles</td>
<td>Perfiles de línea base, principal y alto, hasta el nivel 5,1. (Consulte Especificación de ITU-T H. 264 para más información).</td>
</tr>
<tr class="even">
<td>Formatos de croma</td>
<td>4:2:0 croma o monocromo</td>
</tr>
<tr class="odd">
<td>Resolución mínima</td>
<td>48 × 48 píxeles</td>
</tr>
<tr class="even">
<td>Resolución máxima</td>
<td>4096 × 2304 píxeles<br/> La resolución máxima garantizada para la aceleración de DXVA es 1920 × 1088 píxeles; con resoluciones más altas, la descodificación se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, la descodificación se realiza con el software.<br/>
<blockquote>
[!Note]<br />
En Windows 7, la resolución máxima admitida es 1920 × 1088 píxeles para la descodificación de software y de DXVA.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>El descodificador admite DXVA versión 2, pero no la versión 1 de DXVA. La descodificación de DXVA solo se admite para la bitstreams de línea de base, principal y de perfil alto compatible con Main. (Las bitstreams de línea de base compatibles con Main se definen como <strong>profile_idc</strong>= 66 y <strong>constrained_set1_flag</strong>= 1).</td>
</tr>
</tbody>
</table>



 

Los datos de entrada deben ajustarse al Anexo B de ISO/IEC 14496-10. Los datos deben incluir los códigos de inicio. El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) y un conjunto de parámetros de imagen (PPS) válidos en el flujo de bytes.

El descodificador no admite la tecnología de grano de películas.

> [!Note]  
> Una versión anterior de la documentación indicó incorrectamente que el descodificador es compatible con Windows Server 2008 R2.

 

Si está instalado el complemento de actualización de plataforma para Windows Vista, el descodificador de vídeo H. 264 está disponible en Windows Vista, pero solo es accesible en Windows Vista mediante el [lector de origen](source-reader.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Compatibilidad con MPEG-4 en Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 
