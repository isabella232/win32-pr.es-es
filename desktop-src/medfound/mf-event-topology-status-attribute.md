---
description: Especifica el estado de una topología durante la reproducción.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: MF_EVENT_TOPOLOGY_STATUS atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fecee6003b0275301a29b32ac34d03db32a22017ab1e828536c0631327f79ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973754"
---
# <a name="mf_event_topology_status-attribute"></a>Atributo \_ MF EVENT \_ TOPOLOGY \_ STATUS

Especifica el estado de una topología durante la reproducción.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un miembro de la [**enumeración MF \_ TOPOSTATUS.**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus)

Este atributo se usa con el [evento MESessionTopologyStatus.](mesessiontopologystatus.md)

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

 

 




