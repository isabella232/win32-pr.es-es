---
description: Especifica el tamaño del búfer usado durante la codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propiedad AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152579"
---
# <a name="avenccommonbuffersize-property"></a>Propiedad AVEncCommonBufferSize

Especifica el tamaño del búfer usado durante la codificación. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo de valores lineal. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Los intervalos de parámetros no se admiten para los codificadores de cámara H. 264 UVC 1,5.

## <a name="remarks"></a>Observaciones

En algunos formatos de vídeo, el tamaño de búfer se especifica en bits y, en el caso de otros, se especifica en bytes. Vea los comentarios siguientes para obtener información específica.

Para vídeo MPEG, esta propiedad define el tamaño de búfer del comprobador de búfer de vídeo (VBV). El tamaño del búfer está en bits.

Para el vídeo H. 264 y el Windows Media Video, la propiedad define el tamaño hipotético del descodificador de referencia (HRD). El tamaño del búfer está en bytes.

En el caso de las cámaras de codificación UVC 1,5 H264, el valor de CPB enviado al codificador de cámara debe estar alineado con 16 bits. El tamaño del búfer está en bytes.

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

