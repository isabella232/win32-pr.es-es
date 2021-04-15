---
description: Especifica si el flujo de imagen en un origen de captura de vídeo es independiente de la secuencia de vídeo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648261"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>\_Atributo de \_ \_ secuencia de imagen independiente MF DEVICESTREAM \_

Especifica si el flujo de imagen en un origen de captura de vídeo es independiente de la secuencia de vídeo.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Algunas cámaras de vídeo USB exponen un flujo que genera imágenes fijas. En algunas cámaras, el flujo de imagen simplemente devuelve el siguiente fotograma de la secuencia de vídeo. En otras cámaras, el flujo de imágenes funciona independientemente de la secuencia de vídeo. Si la cámara tiene una secuencia de imágenes independiente, el origen de medios del dispositivo de captura establece este atributo en **true** en el flujo de imagen.

Para obtener este atributo, haga lo siguiente:

1.  Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.
3.  Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el atributo.

Este atributo solo se aplica cuando el atributo de [ \_ \_ \_ secuencia de imagen MF DEVICESTREAM](mf-devicestream-image-stream.md) es **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




