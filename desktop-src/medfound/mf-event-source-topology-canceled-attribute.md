---
description: Especifica si el origen del secuenciador canceló una topología.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef612c8a1081ecc26eaa9dc593a5906ff965d0387ab02490eedd68f7fbf5e813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060662"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>Atributo \_ \_ \_ CANCELY CANCELY DE LA TOPOLOGÍA \_ DE ORIGEN DE EVENTOS MF

Especifica si el [origen del secuenciador](sequencer-source.md) canceló una topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo se usa con los siguientes eventos:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Si este atributo está presente y es distinto de cero, significa que el segmento de presentación finalizó porque el origen del secuenciador canceló la topología. De lo contrario, el segmento de presentación finalizó con normalidad.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Eventos de origen del secuenciador](sequencer-source-events.md)
</dt> </dl>

 

 




