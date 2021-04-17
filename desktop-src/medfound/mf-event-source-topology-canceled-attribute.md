---
description: Especifica si el origen del secuenciador canceló una topología.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659989"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>Atributo MF de \_ topología de origen de eventos \_ \_ \_ cancelada

Especifica si el [origen del secuenciador](sequencer-source.md) canceló una topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se utiliza con los siguientes eventos:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Si este atributo está presente y es distinto de cero, significa que el segmento de presentación finalizó porque el origen del secuenciador canceló la topología. De lo contrario, el segmento de presentación finalizó con normalidad.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Eventos de origen de Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




