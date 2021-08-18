---
description: Especifica si la secuencia de imagen de un origen de captura de vídeo es independiente de la secuencia de vídeo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956685"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>Atributo \_ MF DEVICESTREAM \_ INDEPENDENT IMAGE \_ \_ STREAM

Especifica si la secuencia de imagen de un origen de captura de vídeo es independiente de la secuencia de vídeo.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Algunas cámaras de vídeo USB exponen una secuencia que genera imágenes fijas. En algunas cámaras, la secuencia de imagen simplemente devuelve el siguiente fotograma de la secuencia de vídeo. En otras cámaras, el flujo de imagen funciona independientemente de la secuencia de vídeo. Si la cámara tiene un flujo de imagen independiente, el origen multimedia del dispositivo de captura establece este atributo en **TRUE** en el flujo de imagen.

Para obtener este atributo, haga lo siguiente:

1.  Consulte el origen de medios para la [**interfaz IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
2.  Llame [**a IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.
3.  Llame [**aATTRIBUTEAttributes::GetUINT32 para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) obtener el atributo.

Este atributo solo se aplica cuando el atributo [ \_ MF DEVICESTREAM IMAGE \_ \_ STREAM](mf-devicestream-image-stream.md) es **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




