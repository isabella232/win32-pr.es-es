---
description: Especifica el tamaño del búfer utilizado durante la codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propiedad AVEncCommonBufferSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69eb0c4829d30f3eff0297b7e591686f671d0d67967a65dc76695878d74b454e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794735"
---
# <a name="avenccommonbuffersize-property"></a>Propiedad AVEncCommonBufferSize

Especifica el tamaño del búfer utilizado durante la codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Los intervalos de parámetros no se admiten para codificadores de cámara H.264 UVC 1.5.

## <a name="remarks"></a>Comentarios

Para algunos formatos de vídeo, el tamaño del búfer se especifica en bits y para otros se especifica en bytes. Consulte los comentarios siguientes para obtener información específica.

En el caso del vídeo MPEG, esta propiedad define el tamaño de búfer del comprobador de búfer de vídeo (VBV). El tamaño del búfer está en bits.

Para vídeo H.264 y Windows Vídeo multimedia, la propiedad define el tamaño del descodificador de referencia hipotético (HRD). El tamaño del búfer está en bytes.

En el caso de las cámaras de codificación UVC 1.5 H264, el valor de CPB enviado al codificador de la cámara debe estar alineado en 16 bits. El tamaño del búfer está en bytes.

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

