---
title: DTM_GETMONTHCAL mensaje (Commctrl.h)
description: Obtiene el identificador del control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c91538c9a60d0ecc3db43436ef029c9a3fbd9e35ca33bbfa67e586ad137ef7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878085"
---
# <a name="dtm_getmonthcal-message"></a>Mensaje \_ GETMONTHCAL de DTM

Obtiene el identificador del control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de calendario del mes secundario de un control DTP si se realiza correctamente o **NULL** en caso contrario.

## <a name="remarks"></a>Comentarios

Los controles DTP crean un control de calendario de mes secundario cuando el usuario hace clic en la flecha desplegable[(notificación DTN \_ DROPDOWN).](dtn-dropdown.md) Cuando ya no se necesita el calendario mensual, se destruye (se envía una notificación [ \_ DE CIERRE](dtn-closeup.md) DE DTN al destruirse). Por lo tanto, la aplicación no debe basarse en un identificador estático para el calendario del mes secundario del control DTP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[CIERRE \_ DE DTN](dtn-closeup.md)
</dt> <dt>

[LISTA DESPLEGABLE DE DTN \_](dtn-dropdown.md)
</dt> </dl>

 

 





