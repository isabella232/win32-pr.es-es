---
description: Especifica la hora de inicio de una topología de segmento.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: MF_EVENT_SOURCE_PROJECTSTART atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263324"
---
# <a name="mf_event_source_projectstart-attribute"></a>Atributo MF \_ EVENT \_ SOURCE \_ PROJECTSTART

Especifica la hora de inicio de una topología de segmento.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="remarks"></a>Observaciones

Este atributo se usa con el [evento MESourceStarted.](mesourcestarted.md) El origen del secuenciador establece este atributo cuando la topología del segmento actual tiene el atributo [**MF \_ TOPOLOGY \_ PROJECTSTART.**](mf-topology-projectstart-attribute.md) Los dos atributos tienen el mismo valor.

Este atributo es un valor con firma, aunque se almacena como **UINT64.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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

 

 




