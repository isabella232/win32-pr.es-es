---
description: Tiempo de presentación de una muestra que se representó durante la limpieza.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: MF_EVENT_SCRUBSAMPLE_TIME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57045fcf5fd4faf20d2207778b91aa8ff0fd959dd42571882a21b5a1dceacba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104822"
---
# <a name="mf_event_scrubsample_time-attribute"></a>Atributo MF \_ EVENT \_ SCRUBSAMPLE \_ TIME

Tiempo de presentación de una muestra que se representó durante la limpieza.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="remarks"></a>Comentarios

Este atributo se usa con el [evento MEStreamSinkScrubSampleComplete.](mestreamsinkscrubsamplecomplete.md)

Este atributo es un valor con firma, aunque se almacena como **UINT64.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




