---
description: 'El Microsoft Media Foundation de vídeo H.264 es una transformación de Media Foundation que admite los siguientes perfiles H.264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H.264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467532"
---
# <a name="h264-video-encoder"></a>Codificador de vídeo H.264

El Microsoft Media Foundation de vídeo H.264 es una [transformación](media-foundation-transforms.md) de Media Foundation que admite los siguientes perfiles H.264:

-   Perfil de línea base
-   Perfil Main
-   Perfil alto (requiere Windows 8)

El codificador de vídeo H.264 expone las interfaces siguientes:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

El tipo de medio de entrada debe tener uno de los subtipos siguientes:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Para obtener más información sobre estos subtipos, vea [GUID de subtipo de vídeo](video-subtype-guids.md).

El tipo de salida debe establecerse antes que el tipo de entrada. Hasta que se establece el tipo de salida, el método [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) **del codificador devuelve MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipos de salida

El codificador admite un único subtipo de salida:

-   **MFVideoFormat_H264**

Establezca los siguientes atributos en el tipo de medio de salida.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Debe ser <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de vídeo. Debe ser <strong>MFVideoFormat_H264</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Velocidad de bits codificada media, en bits por segundo. Debe ser mayor que cero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Velocidad de fotogramas. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Tamaño del marco. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modo de interlace. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | Perfil de codificación H.264.<br /> Los valores admitidos son:<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (valor predeterminado)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (requiere Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Opcional. Especifica el nivel de codificación H.264.<br /> El valor predeterminado es –1, lo que indica que el codificador seleccionará el nivel de codificación.<br /> Se recomienda no establecer el nivel en el tipo de medio y permitir que el codificador seleccione el nivel. El codificador puede derivar el nivel adecuado para una secuencia de vídeo determinada, teniendo en cuenta las restricciones de formato y las características del vídeo. Para obtener más información sobre las restricciones de nivel y perfil, consulte el anexo A de ITU-T H.264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Opcional. Especifica la relación de aspecto de píxeles. El valor predeterminado es 1:1. | 




 

Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando [**el atributo MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) salida. Este atributo contiene el encabezado de secuencia.

## <a name="codec-properties"></a>Propiedades del códec

El codificador H.264 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer parámetros de codificación. Admite las siguientes propiedades.

Para ver los requisitos de códec para la certificación del codificador HCK, consulte la **sección Codificador de hardware certificado a** continuación.

Las siguientes propiedades se admiten en Windows 7.



| Propiedad                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Establece el modo de control de velocidad. Vea la sección Comentarios. El modo predeterminado es la velocidad de bits variable sin restricciones (VBR).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Establece el nivel de calidad. Esta propiedad se aplica cuando el modo de control de velocidad está basado en la calidad de VBR (**eAVEncCommonRateControlMode_Quality**). El intervalo válido es de 1 a 100. El valor predeterminado es 70. <br/> Para establecer este parámetro, establezca la propiedad antes de llamar [**a IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> Para establecer este parámetro en Windows 7, establezca la propiedad antes de llamar a [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). El codificador omite los cambios después de establecer el tipo de salida. <br/> En Windows 8, esta propiedad se puede establecer en cualquier momento durante la codificación. Los cambios se aplican a partir del siguiente marco de entrada. <br/> Internamente, el codificador convierte esta propiedad en un [valor AVEncVideoEncodeQP.](codecapi-avencvideoencodeqp.md) <br/> |



 

Las siguientes propiedades requieren Windows 8.




| Propiedad | Descripción | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Establece el modo de codificación adaptable. El codificador H.264 admite los siguientes modos en Windows 8:<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Sin codificación adaptable. (Valor predeterminado).</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Cambie la velocidad de fotogramas de forma adaptable.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).<br /> El intervalo válido es [1 ... 2):1]. <br /> Requiere Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Para la codificación VBR restringida, especifica la velocidad a la que se purga el "cubo de fugas", en bits por segundo. Esta propiedad se aplica cuando el modo de control de velocidad <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br /> El intervalo válido es [1 ... 2):1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Establece la velocidad de bits media de la secuencia de bits codificada, en bits por segundo. Esta propiedad se omite si el modo de control de velocidad <strong>es eAVEncCommonRateControlMode_Quality</strong>. <br /> El intervalo válido es [1 ... 2):1]. <br /> En los modos CBR y VBR sin restricciones, la velocidad de bits media determina el tamaño final del archivo. En el modo CBR, la velocidad de bits media también es la velocidad a la que se purgan los bits comprimidos del "cubo de pérdidas". (Para obtener más información, vea <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>). <br /> En Windows 7, la velocidad de bits media se especifica mediante <a href="mf-mt-avg-bitrate-attribute.md">el atributo MF_MT_AVG_BITRATE</a> en el tipo de medio. <br /> En Windows 8, puede establecer la velocidad de bits media mediante el atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> o la <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> propiedad . Si ambos están establecidos, CODECAPI_AVEncCommonMeanBitRate invalidaciones. En Windows 8, puede establecer la velocidad de bits media durante la codificación. Si cambia la velocidad de bits, el codificador usa la codificación adaptable.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Establece la diferencia entre calidad y velocidad. Intervalo válido:<ul><li>0–33: Baja complejidad</li><li>34-66: Complejidad media (valor predeterminado)</li><li>67-100: Alta complejidad</li></ul><br /> Este valor afecta a cómo el codificador realiza varias operaciones de codificación, como la compensación de movimiento. En niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Habilita o deshabilita CABAC (codificación aritmética binaria adaptable al contexto) para la codificación de entropía H.264. El valor predeterminado es <strong>VARIANT_FALSE</strong>. <br /> CABAC no se usa para el perfil de línea de base.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Establece el valor de <strong>seq_parameter_set_id</strong> en la unidad NAL de SPS de la secuencia de bits H.264. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Establece el número máximo de fotogramas B consecutivos en la secuencia de bits de salida. Los valores válidos son:<ul><li>0: No use fotogramas B (valor predeterminado).</li><li>1: Use un marco B.</li><li>2: Use dos fotogramas B.</li></ul>Para establecer este parámetro, establezca la propiedad antes de llamar <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>a IMFTransform::SetOutputType</strong></a>. <br /> Para el perfil de línea de base, el número de fotogramas B siempre es cero. El codificador invalidará los valores distintos de cero.<br /> Para otros perfiles H.264, si esta propiedad es distinta de cero, el patrón de codificación es IBBPBBP, donde el número máximo de fotogramas B consecutivos es igual a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Establece el número de imágenes de un encabezado GOP al siguiente, incluido el delimitador inicial, pero no el siguiente. <br /> El intervalo válido es [0 ... 2):1]. Si es cero, el codificador selecciona el tamaño de GOP. El valor predeterminado es cero. <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Establece el número de subprocesos de trabajo utilizados por un codificador.<br /> El intervalo válido es de 0 a 16. Si es cero, el codificador selecciona el número de subprocesos. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Indica el tipo de contenido de vídeo.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Intervalo válido: 16–51. El valor predeterminado es 24. <br /> Esta propiedad se aplica cuando el modo de control de velocidad <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> Esta propiedad configura la misma configuración de codificación <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>que AVEncCommonQuality</strong></a>. Sin embargo, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite a la aplicación especificar el valor de QP directamente. Si se establecen ambas propiedades, AVEncVideoEncodeQP invalida . <br /> El valor predeterminado de 24 corresponde al valor predeterminado de 70 para la configuración <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality.</strong></a><br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Fuerza al codificador a codificar el fotograma siguiente como un fotograma clave.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Intervalo válido: 0–51. El valor predeterminado es 0. <br /> Esta propiedad se aplica a todos los modos de control de velocidad. El codificador no debe generar un valor de QP inferior al especificado por la <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> propiedad .<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Habilita o deshabilita el modo de baja latencia. Vea "Multithreading" en la sección Comentarios.<br /> | 




 

## <a name="remarks"></a>Comentarios

El codificador admite los siguientes modos de control de velocidad.



| Modo                                  | Constante                                            | Descripción                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits constante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | El codificador intenta lograr una velocidad de bits constante, mediante un modelo de "depósito con fugas". La velocidad de bits de destino la proporciona [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) propiedad . <br/> Requiere Windows 8. <br/> |
| Velocidad de bits variable restringida (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | El codificador usa un modelo de "cubo de fugas" con una velocidad de bits máxima. La tasa de purga del cubo de fugas la proporciona [la CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) propiedad . <br/> Requiere Windows 8. <br/>     |
| Velocidad de bits variable basada en calidad (VBR) | **eAVEncCommonRateControlMode_Quality**            | El codificador intenta lograr un nivel de calidad constante, dado por la [**propiedad AVEncCommonQuality.**](../directshow/avenccommonquality-property.md)                                                                                                           |
| VBR sin restricciones                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | El codificador intenta lograr la velocidad de bits de destino dada por el [**atributo MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio de salida. Este es el modo predeterminado.                                                              |



 

Los modos CBR y VBR restringido requieren Windows 8.

En Windows 8, el codificador establece los siguientes atributos en los ejemplos de salida:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> Una versión anterior de la documentación indicaba incorrectamente que el codificador se admite en Windows Server 2008 R2.

 

### <a name="multithreading"></a>Subprocesamiento múltiple

En Windows 8, el codificador admite dos modos de codificación:

-   **Codificación de segmentos.** En este modo, los segmentos se codifican en paralelo. Cada segmento se codifica en un subproceso diferente. Este modo tiene una latencia baja, ya que una sola imagen se codifica en paralelo. Sin embargo, este enfoque no escala a medida que aumenta el número de núcleos, ya que el número de segmentos está limitado por el número de filas de macrobloqueo en la imagen de entrada.
-   **Codificación de varios fotogramas.** En este modo, el codificador acepta varios fotogramas de entrada y los codifica en paralelo. Este modo se escala mejor en un entorno de varios núcleos, pero introduce más latencia.

El codificador tiene como valor predeterminado la codificación de segmentos, para minimizar la latencia. Para habilitar la codificación de varios fotogramas, establezca la [propiedad CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) en **VARIANT_FALSE**.

Para establecer el número de subprocesos de trabajo utilizados por el codificador, establezca la [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) trabajo.

En Windows 7, el codificador siempre usa la codificación de segmentos.

### <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Si hay un codificador de hardware certificado, generalmente se usará en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados. Los codificadores certificados son necesarios para admitir un determinado conjunto de **propiedades ICodecAPI** y, opcionalmente, pueden admitir otro conjunto de propiedades. El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.

A continuación se muestra el conjunto de propiedades **ICodecAPI** obligatorias y opcionales para que los codificadores pasen la certificación del codificador HCK.

Se requieren Windows 8 y Windows 8.1 **propiedades ICodecAPI** siguientes:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Las siguientes Windows 8.1 **ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinámico)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

Las siguientes Windows 8 y Windows 8.1 **propiedades ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (estático)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Las siguientes **propiedades de ICodecAPI** son opcionales. No se prueban en HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



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

 

 
