---
description: Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita la simplificación. Para obtener una definición de la simplificación, vea Acerca del control de velocidad.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9305df2b17e00b03bd9788ecd8caf26db82b8e331d1c72626374b63e7dcaf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104941"
---
# <a name="mf_event_do_thinning-attribute"></a>Atributo \_ MF EVENT DO \_ \_ THINNING

Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita la simplificación. Para obtener una definición de la simplificación, vea [About Rate Control](about-rate-control.md).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo se usa con el [evento MESourceRateChangeRequested.](mesourceratechangerequested.md) Si el valor es **TRUE**, el origen multimedia solicita un cambio a la reproducción fina.

El valor predeterminado es **FALSE**.

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




