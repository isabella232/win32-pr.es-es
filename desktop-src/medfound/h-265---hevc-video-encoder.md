---
description: El Media Foundation de vídeo H.265 es una transformación de Media Foundation que admite la codificación de contenido en el formato H.265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificador de vídeo H.265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b95eee96d3313df2604919883cf631b0aef999f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248534"
---
# <a name="h265--hevc-video-encoder"></a>Codificador de vídeo H.265/HEVC

El Media Foundation de vídeo H.265 es un Media Foundation [Transform](media-foundation-transforms.md) que admite la codificación de contenido en el formato H.265/HEVC. El codificador admite los perfiles siguientes:

-   Perfil Main

El codificador de vídeo H.265 expone las interfaces siguientes:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

El tipo de medio de entrada debe tener uno de los subtipos siguientes:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obtener más información sobre estos subtipos, vea [GUID de subtipo de vídeo](video-subtype-guids.md).

El tipo de salida debe establecerse antes que el tipo de entrada. Hasta que se establece el tipo de salida, el método [**MFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificador devuelve **MF E TRANSFORM TYPE NOT \_ \_ \_ \_ \_ SET**.

## <a name="output-types"></a>Tipos de salida

El codificador admite un único subtipo de salida:

-   **MFVideoFormat \_ H265**

Establezca los atributos siguientes en el tipo de medio de salida.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Debe ser <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de vídeo. Debe ser <strong>MFVideoFormat_HEVC</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Velocidad de bits codificada media, en bits por segundo. Debe ser mayor que cero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Velocidad de fotogramas. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Tamaño del marco. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modo de interlace. | 
| <a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a> | Perfil de codificación H.265.<br /> Los valores admitidos son: <br /><ul><li><strong>eAVEncH265VProfile_Main_420_8</strong></li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Especifica el nivel del vídeo codificado. Para obtener más información sobre las restricciones de perfil y nivel, consulte el anexo A de ITU-T H.265.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Opcional. Especifica la relación de aspecto de píxeles. El valor predeterminado es 1:1. | 




 

Una vez establecido el tipo de salida, el codificador de vídeo actualiza el tipo agregando el atributo [**MF MT MPEG SEQUENCE \_ \_ \_ \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) Este atributo contiene el encabezado de secuencia.

## <a name="supported-imftransform-methods"></a>Métodos DETRANSFORM admitidos

Se admiten los métodos siguientes de la interfaz [**DETRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para el codificador H.265/HEVC:

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

Todos los [**demás métodos DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devolverán el error E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Métodos ICodecAPI admitidos

Se admiten los métodos siguientes de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para el codificador H.265/HEVC:

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Todos los demás [**métodos ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) devolverán el error E \_ NOTIMPL.

## <a name="codec-properties"></a>Propiedades del códec

El codificador H.265 implementa la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para establecer parámetros de codificación. Admite las siguientes propiedades.

Para ver los requisitos de códec para la certificación del codificador HCK, consulte la **sección Codificador de hardware certificado a** continuación.




| Propiedad | Descripción | 
|----------|-------------|
| <a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a> | Establece el modo de control de velocidad. Los modos admitidos son:<br /><ul><li><strong>eAVEncCommonRateControlMode_CBR</strong></li><li><strong>eAVEncCommonRateControlMode_Quality</strong></li></ul>Si se especifican otros modos, <strong>se usará eAVEncCommonRateControlMode_CBR</strong> control de velocidad.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Establece la velocidad de bits media de la secuencia de bits codificada, en bits por segundo. <br /> El intervalo válido es [1 ... 2):1]. <br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Establece el tamaño del búfer, en bytes, para la codificación de velocidad de bits constante (CBR).<br /> El intervalo válido es [1 ... 2):1]. <br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Establece la velocidad de bits máxima para los modos de control de velocidad que permiten una velocidad de bits máxima. <br /> El intervalo válido es [1 ... 2):1]. <br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Establece el número de imágenes de un encabezado GOP al siguiente, incluido el delimitador inicial, pero no el siguiente. <br /> El intervalo válido es [0 ... 2):1]. Si es cero, el codificador selecciona el tamaño de GOP. El valor predeterminado es cero. <br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Habilita o deshabilita el modo de baja latencia. <br /> Se trata de un VT_BOOL predeterminado.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Establece la diferencia entre calidad y velocidad. Este valor afecta a cómo el codificador realiza varias operaciones de codificación, como la compensación de movimiento. En niveles de complejidad más altos, el codificador se ejecuta más lentamente, pero genera una mejor calidad a la misma velocidad de bits. <br /> El intervalo válido es de 0 a 100. Internamente, este valor se asigna a un conjunto más pequeño de niveles de calidad y velocidad admitidos por el codificador.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Fuerza al codificador a codificar el fotograma siguiente como un fotograma clave.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Cuando se establece esta propiedad, el codificador usará el QP especificado para codificar el fotograma siguiente y todos los fotogramas posteriores hasta que se especifique un nuevo QP. <br /> Intervalo válido: 0–51, ambos inclusive <br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Esta propiedad establecerá un límite en el QP mínimo que el codificador puede usar durante el control ratecontrol de CBR.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a> | Esta propiedad establecerá un límite en el QP máximo que el codificador puede usar durante el control de velocidad CBR.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a> | Establece si el contenido es vídeo de pantalla completa, en lugar de contenido de pantalla que podría tener una ventana de vídeo más pequeña o no tener ningún vídeo.<br /> Se trata de VT_UI4 valor.<br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Establece el número de subprocesos utilizados para realizar la operación de compresión. El codificador dividirá el marco en mosaicos para que el número de subprocesos sea igual al número de iconos.<br /><ul><li>Número de procesadores lógicos. El número de subprocesos debe ser menor o igual que el número de procesadores lógicos.</li><li>Tamaño del marco. El tamaño de un icono debe ser mayor o igual que 265 x 64 píxeles.</li><li>Paridad. El número de subprocesos debe ser un valor par. Si el valor especificado es impar, se usará el siguiente valor par inferior.</li></ul>Se trata de VT_UI4 valor.<br /> | 




 

## <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Si hay un codificador de hardware certificado, normalmente se usará en lugar del codificador del sistema de bandeja de entrada para Media Foundation escenarios relacionados. Los codificadores certificados son necesarios para admitir un determinado conjunto de propiedades **ICodecAPI** y, opcionalmente, pueden admitir otro conjunto de propiedades. El proceso de certificación debe garantizar que las propiedades necesarias se admiten correctamente y, si se admite una propiedad opcional, que también se admite correctamente.

A continuación se muestra el conjunto de propiedades **ICodecAPI** obligatorias y opcionales para que los codificadores pasen la certificación del codificador HCK.

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
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
