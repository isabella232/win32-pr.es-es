---
title: MCM_SETDAYSTATE mensaje (Commctrl.h)
description: Establece los estados de día de todos los meses que están visibles actualmente dentro de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a0f06c3082d04f9d0e50ba76b92f214c358cbc61cbdbfb5992c4b3b14e5fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078999"
---
# <a name="mcm_setdaystate-message"></a>Mensaje \_ SETDAYSTATE de MCM

Establece los estados de día de todos los meses que están visibles actualmente dentro de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetDayState.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica cuántos elementos hay en la matriz a la que *apunta lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**valores MONTHDAYSTATE**](monthdaystate.md) que definen cómo el control de calendario mensual dibujará cada día en su presentación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

Una aplicación puede establecer explícitamente la información de estado de día mediante el envío de este mensaje, pero el estado no se conservará cuando una parte diferente del calendario se desplace a la vista. La información de estado de día normalmente se establece en respuesta al código de notificación [ \_ GETDAYSTATE de MCN,](mcn-getdaystate.md) que se envía cada vez que es necesario actualizar el control.

La matriz *en lParam* debe contener tantos elementos como el valor devuelto por la macro siguiente:

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Tenga en cuenta que la matriz en *lParam* debe contener valores [**MONTHDAYSTATE**](monthdaystate.md) que se correspondan con todos los meses que se muestran actualmente en la pantalla del control, en orden cronológico. Esto incluye los dos meses que se pueden mostrar parcialmente antes del primer mes y después del último mes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Usar controles de calendario mensual](using-month-calendar-controls.md)
</dt> </dl>

 

 





