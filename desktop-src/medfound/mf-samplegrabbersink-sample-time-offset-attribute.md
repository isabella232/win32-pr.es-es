---
description: Desplazamiento entre la marca de tiempo de cada muestra recibida por el tomador de la muestra y la hora en que el tomador de la muestra presenta la muestra.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257783"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>Atributo \_ MF SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET

Desplazamiento entre la marca de tiempo de cada muestra recibida por el tomador de la muestra y la hora en que el tomador de la muestra presenta la muestra.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Puede establecer este atributo en el objeto [**MFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto por la [**función MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Este atributo permite que la función de devolución de llamada del capturador de ejemplo reciba muestras antes del tiempo de presentación.

Cuando el capturador de ejemplo recibe una nueva muestra, presenta la muestra en el momento *t* - *offset*, donde *t* es la marca de tiempo en la muestra y *offset* es el valor de este atributo. Si no se establece este atributo, el valor predeterminado es cero.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 




