---
description: Desplazamiento entre el tiempo de presentación y las marcas de tiempo de los orígenes multimedia.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: MF_EVENT_PRESENTATION_TIME_OFFSET atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5ff2285bc624d42f17d4662cf93e3f46a65fcbef465e731874ef255c40c076d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013085"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>Atributo MF \_ EVENT \_ PRESENTATION TIME \_ \_ OFFSET

Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

El desplazamiento se calcula de la siguiente manera: desplazamiento = tiempo de presentación - hora de origen. Este atributo se usa con los siguientes eventos:

-   [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)
-   [MESessionStarted](mesessionstarted.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




