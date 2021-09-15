---
description: Hora de presentación en la que los receptores multimedia representarán el primer ejemplo de la nueva topología.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468722"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>Atributo MF \_ EVENT START PRESENTATION TIME AT \_ \_ \_ \_ \_ OUTPUT

Hora de presentación en la que los receptores multimedia representarán el primer ejemplo de la nueva topología.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **un valor LONGLONG.**

## <a name="remarks"></a>Observaciones

Si algún objeto de canalización de los datos almacenados en búfer de la topología anterior, este valor será ligeramente menor que el valor del atributo [**MF EVENT PRESENTATION TIME \_ \_ \_ \_ OFFSET,**](mf-event-presentation-time-offset-attribute.md) porque los receptores deben representar los datos almacenados en búfer.

Este atributo es un valor con firma, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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

 

 




