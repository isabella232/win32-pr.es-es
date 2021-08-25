---
title: DTM_CLOSEMONTHCAL mensaje (Commctrl.h)
description: Cierra un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro DateTime \_ CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f458592d2842625b9826eda5963c66cbd182e3f052a2b2a70ff5219a054e8cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878245"
---
# <a name="dtm_closemonthcal-message"></a>Mensaje \_ DTM CLOSEMONTHCAL

Cierra un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro [**DateTime \_ CloseMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Comentarios

Destruye el control y envía una notificación [DTN \_ CLOSEUP](dtn-closeup.md) de que el control se está cerrando en lugar de que el control se abra (desplegable como en la notificación DESPLEGABLE de [DTN) \_ ](dtn-dropdown.md) al elemento primario del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[LISTA DESPLEGABLE DE DTN \_](dtn-dropdown.md)
</dt> <dt>

[CIERRE \_ DE DTN](dtn-closeup.md)
</dt> </dl>

 

 





