---
title: Mensaje de DTM_GETMONTHCAL (commctrl. h)
description: Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetMonthCal de fecha y hora \_ .
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL controles de mensajes de Windows
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
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996755"
---
# <a name="dtm_getmonthcal-message"></a>DTM \_ GETMONTHCAL

Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de calendario mensual del control de DTP si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Los controles de DTP crean un control de calendario mensual secundario cuando el usuario hace clic en la flecha desplegable (notificación de desplegable[DTN \_ ](dtn-dropdown.md) ). Cuando el calendario mensual ya no es necesario, se destruye (se envía una notificación [DTN \_ primer plano](dtn-closeup.md) en la destrucción). Por lo tanto, la aplicación no debe basarse en un identificador estático para el calendario mensual del control de DTP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[DTN \_ primer plano](dtn-closeup.md)
</dt> <dt>

[\_lista desplegable DTN](dtn-dropdown.md)
</dt> </dl>

 

 





