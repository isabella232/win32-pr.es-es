---
description: Especifica las características actuales del origen de medios.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: MF_EVENT_SOURCE_CHARACTERISTICS atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a9b72adaa5869d806ab0a3c8afcddff7892f93872e86aa6dfe96bde1b8348b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956595"
---
# <a name="mf_event_source_characteristics-attribute"></a>Atributo MF \_ EVENT \_ SOURCE \_ CHARACTERISTICS

Especifica las características actuales del origen de medios.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un **OR** bit a bit de marcas de la [**enumeración MFMEDIASOURCE \_ CHARACTERISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

Este atributo se usa con el [evento MESourceCharacteristicsChanged.](mesourcecharacteristicschanged.md)

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
</dt> </dl>

 

 




