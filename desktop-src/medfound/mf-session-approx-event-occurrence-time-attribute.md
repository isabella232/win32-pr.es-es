---
description: Hora aproximada a la que la sesión multimedia ha producido un evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6cbaa7d12cebe14b015c4d568b36b081930ef4b302797dba76fc728e92cf01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740032"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>Atributo MF \_ SESSION APPROX EVENT OCCURRENCE \_ \_ \_ \_ TIME

Hora aproximada a la que la sesión multimedia ha producido un evento.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **un valor LONGLONG.**

## <a name="remarks"></a>Observaciones

Algunos eventos de la sesión multimedia tienen este atributo. El valor proporciona el tiempo aproximado de presentación en el que se ha producido el evento.

Este atributo es un valor con firma, aunque se almacena como **UINT64**.

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

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




