---
description: El codificador de vídeo H. 265 Media Foundation es una transformación de Media Foundation que admite la codificación de contenido en el formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC de vídeo codificador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001407"
---
# <a name="h265--hevc-video-encoder"></a>H. 265/HEVC de vídeo codificador

El codificador de vídeo H. 265 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la codificación de contenido en el formato H. 265/HEVC. El codificador admite los siguientes perfiles:

-   Perfil Main

El codificador de vídeo H. 265 expone las siguientes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

El tipo de medio de entrada debe tener uno de los siguientes subtipos:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

El tipo de salida debe establecerse antes que el tipo de entrada. Hasta que se establezca el tipo de salida, el método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificador devuelve el **tipo de \_ transformación MF E \_ \_ \_ no \_ establecido**.

## <a name="output-types"></a>Tipos de salida

El codificador admite un solo subtipo de salida:

-   **MFVideoFormat \_ H265**

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
<td>Subtipo de vídeo. Debe ser <strong>MFVideoFormat_HEVC</strong>.</td>
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
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>Perfil de codificación H. 265.<br/> Los valores admitidos son: <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Especifica el nivel del vídeo codificado. Para obtener más información acerca de las restricciones de perfil y de nivel, consulte el anexo a de ITU-T H. 265.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Opcional. Especifica la relación de aspecto de píxeles. El valor predeterminado es 1:1.</td>
</tr>
</tbody>
</table>



 

Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando el atributo de [**\_ encabezado de secuencia MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) . Este atributo contiene el encabezado de secuencia.

## <a name="supported-imftransform-methods"></a>Métodos de IMFTransform admitidos

Los siguientes métodos de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) son compatibles con el codificador H. 265/HEVC:

-   [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Todos los demás métodos de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devolverán el error E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Métodos de ICodecAPI admitidos

Los siguientes métodos de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) son compatibles con el codificador H. 265/HEVC:

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Todos los demás métodos de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) devolverán el error E \_ NOTIMPL.

## <a name="codec-properties"></a>Propiedades de códec

El codificador H. 265 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer los parámetros de codificación. Admite las siguientes propiedades.

Para conocer los requisitos de códec para la certificación del codificador de HCK, consulte la sección sobre el **codificador de hardware certificado** a continuación.



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
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>Establece el modo de control de velocidad. Los modos admitidos son:<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
Si se especifican otros modos, se usará el control de velocidad de <strong>eAVEncCommonRateControlMode_CBR</strong> .<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Establece la velocidad de bits promedio para el flujo de bits codificado, en bits por segundo. <br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).<br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Establece la velocidad de bits máxima para los modos de control de velocidad que permiten una velocidad de bits máxima. <br/> El intervalo válido es [1... 2 ³ ² – 1]. <br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Establece el número de imágenes desde un encabezado GOP hasta el siguiente, incluido el delimitador inicial, pero no el siguiente. <br/> El intervalo válido es [0... 2 ³ ² – 1]. Si el valor es cero, el codificador selecciona el tamaño de GOP. El valor predeterminado es cero. <br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Habilita o deshabilita el modo de baja latencia. <br/> Se trata de un valor de VT_BOOL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Establece el equilibrio de calidad/velocidad. Este valor afecta al modo en que el codificador realiza varias operaciones de codificación, como la compensación de movimiento. En los niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits. <br/> El intervalo válido es de 0 a 100. Internamente, este valor se asigna a un conjunto más pequeño de niveles de calidad/velocidad que admite el codificador.<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Obliga al codificador a codificar el siguiente fotograma como un fotograma clave.<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Cuando se establece esta propiedad, el codificador usará el QP especificado para codificar el fotograma siguiente y todos los fotogramas posteriores hasta que se especifique un nuevo QP. <br/> Intervalo válido: 0 – 51, ambos incluidos <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Esta propiedad establecerá un límite en el valor de QP mínimo que el codificador puede utilizar durante RateControl CBR.<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>Esta propiedad establecerá un límite en el valor de QP máximo que el codificador puede utilizar durante RateControl CBR.<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>Establece si el contenido está en pantalla completa, en lugar de en el contenido de pantalla que podría tener una ventana de vídeo más pequeña o no tener ningún vídeo.<br/> Se trata de un valor de VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Establece el número de subprocesos utilizados para realizar la operación de compresión. El codificador dividirá el marco en mosaicos de forma que el número de subprocesos sea igual al número de mosaicos.<br/>
<ul>
<li>El número de procesadores lógicos. El número de subprocesos debe ser menor o igual que el número de procesadores lógicos.</li>
<li>Tamaño del marco. El tamaño de un icono debe ser mayor o igual que 265x64 píxeles.</li>
<li>Paridad. El número de subprocesos debe ser un valor par. Si el valor especificado es impar, se utilizará el siguiente valor par inferior.</li>
</ul>
Se trata de un valor de VT_UI4.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Si hay un codificador de hardware certificado, se usará generalmente en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados. Los codificadores certificados son necesarios para admitir un conjunto determinado de propiedades de **ICodecAPI** y, opcionalmente, admiten otro conjunto de propiedades. El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.

El siguiente es el conjunto de propiedades **ICodecAPI** necesarias y opcionales para los codificadores para pasar la certificación del codificador HCK.

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
