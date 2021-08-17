---
description: Desplazamiento entre la marca de tiempo de cada muestra recibida por el tomador de la muestra y la hora en que el tomador de la muestra presenta la muestra.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad8086d7820a9f7c642fb049af8696521f675be3f7606ff19166a4570ee8000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875996"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>Atributo \_ MF SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET

Desplazamiento entre la marca de tiempo de cada muestra recibida por el tomador de la muestra y la hora en que el tomador de la muestra presenta la muestra.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Puede establecer este atributo en el objeto [**MFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto por la [**función MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Este atributo permite que la función de devolución de llamada del capturador de ejemplo reciba muestras antes del tiempo de presentación.

Cuando el capturador de ejemplo recibe una nueva muestra, presenta la muestra en el momento *t* - *offset*, donde *t* es la marca de tiempo en la muestra y *offset* es el valor de este atributo. Si no se establece este atributo, el valor predeterminado es cero.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**SAMPLESampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




