---
description: 'El codificador de vídeo H. 264 Microsoft Media Foundation es una transformación de Media Foundation que admite los siguientes perfiles H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715450"
---
# <a name="h264-video-encoder"></a>Codificador de vídeo H. 264

El codificador de vídeo H. 264 Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite los siguientes perfiles H. 264:

-   Perfil de línea base
-   Perfil Main
-   Perfil alto (requiere Windows 8)

El codificador de vídeo H. 264 expone las siguientes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

El tipo de medio de entrada debe tener uno de los siguientes subtipos:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

El tipo de salida debe establecerse antes que el tipo de entrada. Hasta que se establezca el tipo de salida, el método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificador devuelve **MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipos de salida

El codificador admite un solo subtipo de salida:

-   **MFVideoFormat_H264**

Establezca los siguientes atributos en el tipo de medio de salida.



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal. Debe ser <strong>MFMediaType_Video</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de vídeo. Debe ser <strong>MFVideoFormat_H264</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>Velocidad media de bits codificada, en bits por segundo. Debe ser mayor que cero.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Velocidad de fotogramas.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Tamaño del marco.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modo entrelazado.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></td>
<td>Perfil de codificación H. 264.<br/> Los valores admitidos son:<br/>
<ul>
<li><strong>eAVEncH264VProfile_Base</strong> (valor predeterminado)</li>
<li><strong>eAVEncH264VProfile_Main</strong></li>
<li><strong>eAVEncH264VProfile_High</strong> (requiere Windows 8)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Opcional. Especifica el nivel de codificación H. 264.<br/> El valor predeterminado es-1, lo que indica que el codificador seleccionará el nivel de codificación.<br/> Se recomienda no establecer el nivel en el tipo de medio y permitir que el codificador Seleccione el nivel. El codificador puede derivar el nivel adecuado para un flujo de vídeo determinado, teniendo en cuenta las restricciones de formato y las características del vídeo. Para obtener más información acerca de las restricciones de perfil y de nivel, consulte el anexo a de ITU-T H. 264.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Opcional. Especifica la relación de aspecto de píxeles. El valor predeterminado es 1:1.</td>
</tr>
</tbody>
</table>



 

Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando el atributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) . Este atributo contiene el encabezado de secuencia.

## <a name="codec-properties"></a>Propiedades de códec

El codificador H. 264 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer los parámetros de codificación. Admite las siguientes propiedades.

Para conocer los requisitos de códec para la certificación del codificador de HCK, consulte la sección sobre el **codificador de hardware certificado** a continuación.

Las siguientes propiedades se admiten en Windows 7.



| Propiedad                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Establece el modo de control de velocidad. Vea la sección Comentarios. El modo predeterminado es la velocidad de bits variable (VBR) sin restricciones.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Establece el nivel de calidad. Esta propiedad se aplica cuando el modo de control de velocidad es VBR basada en la calidad (**eAVEncCommonRateControlMode_Quality**). El intervalo válido es de 1 a 100. El valor predeterminado es 70. <br/> Para establecer este parámetro, establezca la propiedad antes de llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> Para establecer este parámetro en Windows 7, establezca la propiedad antes de llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). El codificador omite los cambios después de establecer el tipo de salida. <br/> En Windows 8, esta propiedad se puede establecer en cualquier momento durante la codificación. Los cambios se aplican a partir del siguiente fotograma de entrada. <br/> Internamente, el codificador convierte esta propiedad en un valor [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) . <br/> |



 

Las siguientes propiedades requieren Windows 8.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></td>
<td>Establece el modo de codificación adaptable. El codificador H. 264 admite los siguientes modos en Windows 8:
<ul>
<li><strong>eAVEncAdaptiveMode_None</strong>. Sin codificación adaptable. (Valor predeterminado).</li>
<li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Cambiar la velocidad de fotogramas de un modo adaptable.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).<br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/> Requiere Windows 8. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>En el caso de la codificación VBR restringida, especifica la velocidad a la que &quot; se purga el depósito de fugas &quot; , en bits por segundo. Esta propiedad se aplica cuando se <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>el modo de control de velocidad. <br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Establece la velocidad de bits promedio para el flujo de bits codificado, en bits por segundo. Esta propiedad se omite si el modo de control de velocidad es <strong>eAVEncCommonRateControlMode_Quality</strong>. <br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/> En los modos CBR y VBR sin restricciones, la velocidad de bits promedio determina el tamaño final del archivo. En el modo CBR, la velocidad de bits promedio es también la velocidad a la que los bits comprimidos se purgan del &quot; depósito de fugas. &quot; (para obtener más información, vea <a href="the-leaky-bucket-buffer-model.md">el modelo de búfer de depósitos con fugas</a>). <br/> En Windows 7, la velocidad de bits promedio se especifica mediante el atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> en el tipo de medio. <br/> En Windows 8, puede establecer la velocidad de bits promedio mediante el <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> atributo o la propiedad <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> . Si se establecen ambos, CODECAPI_AVEncCommonMeanBitRate invalida. En Windows 8, puede establecer la velocidad de bits promedio durante la codificación. Si la velocidad de bits cambia, el codificador utiliza la codificación adaptable.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Establece el equilibrio de calidad/velocidad. Intervalo válido:
<ul>
<li>0 – 33: baja complejidad</li>
<li>34 – 66: complejidad media (valor predeterminado)</li>
<li>67 – 100: alta complejidad</li>
</ul>
<br/> Este valor afecta al modo en que el codificador realiza varias operaciones de codificación, como la compensación de movimiento. En los niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></td>
<td>Habilita o deshabilita CABAC (codificación aritmética binaria adaptable al contexto) para la codificación de entropía H. 264. El valor predeterminado es <strong>VARIANT_FALSE</strong>. <br/> CABAC no se utiliza para el perfil de línea base.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></td>
<td>Establece el valor de <strong>seq_parameter_set_id</strong> en la unidad nal de SPS del fragmentada H. 264. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></td>
<td>Establece el número máximo de fotogramas B consecutivos en el fragmentada de salida. Los valores válidos son:
<ul>
<li>0: no usar fotogramas B (valor predeterminado).</li>
<li>1: Use un marco B.</li>
<li>2: Use dos fotogramas B.</li>
</ul>
Para establecer este parámetro, establezca la propiedad antes de llamar a <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>. <br/> Para el perfil de línea base, el número de fotogramas B siempre es cero. El codificador invalidará los valores distintos de cero.<br/> Para otros perfiles H. 264, si esta propiedad es distinta de cero, el patrón de codificación es IBBPBBP, donde el número máximo de fotogramas B consecutivos es igual que <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Establece el número de imágenes desde un encabezado GOP hasta el siguiente, incluido el delimitador inicial, pero no el siguiente. <br/> El intervalo válido es [0... 2 ³ ² – 1]. Si el valor es cero, el codificador selecciona el tamaño de GOP. El valor predeterminado es cero. <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Establece el número de subprocesos de trabajo que utiliza un codificador.<br/> El intervalo válido es de 0 a 16. Si el valor es cero, el codificador selecciona el número de subprocesos. <br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></td>
<td>Indica el tipo de contenido de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Intervalo válido: 16 – 51. El valor predeterminado es 24. <br/> Esta propiedad se aplica cuando se <strong>eAVEncCommonRateControlMode_Quality</strong>el modo de control de velocidad. <br/> Esta propiedad configura la misma configuración de codificación que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. Sin embargo, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite que la aplicación especifique el valor de QP directamente. Si se establecen ambas propiedades, AVEncVideoEncodeQP invalida. <br/> El valor predeterminado de 24 corresponde al valor predeterminado de 70 para la configuración de <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Intervalo válido: 0 – 51. El valor predeterminado es 0. <br/> Esta propiedad se aplica a todos los modos de control de velocidad. El codificador no debe producir un valor de QP inferior a lo especificado por la propiedad <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Habilita o deshabilita el modo de baja latencia. Vea &quot; multithreading &quot; en la sección Comentarios.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

El codificador admite los siguientes modos de control de velocidad.



| Mode                                  | Constante                                            | Descripción                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits constante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | El codificador intenta alcanzar una velocidad de bits constante, mediante un modelo de "depósito de fugas". La velocidad de bits de destino la proporciona la propiedad [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . <br/> Requiere Windows 8. <br/> |
| Velocidad de bits variable restringida (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | El codificador usa un modelo de "depósito de fugas" con una velocidad de bits máxima. La tasa de purga del depósito de fugas viene determinada por la propiedad [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) . <br/> Requiere Windows 8. <br/>     |
| Velocidad de bits variable basada en la calidad (VBR) | **eAVEncCommonRateControlMode_Quality**            | El codificador intenta alcanzar un nivel de calidad constante, proporcionado por la propiedad [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .                                                                                                           |
| VBR sin restricciones                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | El codificador intenta lograr la velocidad de bits de destino proporcionada por el [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) atributo en el tipo de medio de salida. Este es el modo predeterminado.                                                              |



 

Los modos CBR y VBR restringida requieren Windows 8.

En Windows 8, el codificador establece los siguientes atributos en los ejemplos de salida:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> Una versión anterior de la documentación indicó incorrectamente que el codificador es compatible con Windows Server 2008 R2.

 

### <a name="multithreading"></a>Subprocesamiento múltiple

En Windows 8, el codificador admite dos modos de codificación:

-   **Codificación del segmento.** En este modo, los segmentos se codifican en paralelo. Cada segmento se codifica en un subproceso diferente. Este modo tiene una latencia baja, porque una sola imagen está codificada en paralelo. Sin embargo, este enfoque no escala a medida que aumenta el número de núcleos, ya que el número de segmentos está limitado por el número de filas de adaptativo macrobloque en la imagen de entrada.
-   **Codificación de varios marcos.** En este modo, el codificador acepta varios fotogramas de entrada y los codifica en paralelo. Este modo se escala mejor en un entorno de varios núcleos, pero introduce más latencia.

El codificador tiene como valor predeterminado la codificación de segmentos, para minimizar la latencia. Para habilitar la codificación de varios marcos, establezca la propiedad [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) en **VARIANT_FALSE**.

Para establecer el número de subprocesos de trabajo utilizados por el codificador, establezca la propiedad [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .

En Windows 7, el codificador siempre usa la codificación de sectores.

### <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Si hay un codificador de hardware certificado, se usará generalmente en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados. Los codificadores certificados son necesarios para admitir un conjunto determinado de propiedades de **ICodecAPI** y, opcionalmente, admiten otro conjunto de propiedades. El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.

El siguiente es el conjunto de propiedades **ICodecAPI** necesarias y opcionales para los codificadores para pasar la certificación del codificador HCK.

Se requieren las siguientes propiedades **ICodecAPI** de Windows 8 y Windows 8.1:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Las siguientes Windows 8.1 propiedades de **ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.

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

Las siguientes propiedades de Windows 8 y Windows 8.1 **ICodecAPI** son opcionales, pero se prueban en HCK si se admiten.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (estático)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Las siguientes propiedades de **ICodecAPI** son opcionales. No se prueban en HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



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

 

 
