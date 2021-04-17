---
description: La hora aproximada a la que la sesión multimedia generó un evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716492"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>\_Atributo de \_ \_ tiempo de \_ repetición de evento \_ de sesión MF aprox.

La hora aproximada a la que la sesión multimedia generó un evento.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

Algunos eventos de la sesión multimedia tienen este atributo. El valor proporciona el tiempo de presentación aproximado en que se produjo el evento.

Este atributo es un valor con signo, aunque se almacena como **UINT64**.

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

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




