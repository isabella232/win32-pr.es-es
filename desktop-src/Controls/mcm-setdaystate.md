---
title: Mensaje de MCM_SETDAYSTATE (commctrl. h)
description: Establece los Estados de día para todos los meses que están visibles actualmente dentro de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE controles de mensajes de Windows
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
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492850"
---
# <a name="mcm_setdaystate-message"></a>Mensaje de MCM \_ SETDAYSTATE

Establece los Estados de día para todos los meses que están visibles actualmente dentro de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que indica el número de elementos que hay en la matriz a la que se dirige *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de valores [**MONTHDAYSTATE**](monthdaystate.md) que definen cómo se dibujará el control de calendario mensual cada día en su pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer explícitamente la información de estado de los días mediante el envío de este mensaje, pero el estado no se conservará cuando se desplace una parte diferente del calendario en la vista. Normalmente, la información de estado de los días se establece como respuesta al código de notificación de [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que se envía cada vez que es necesario actualizar el control.

La matriz de *lParam* debe contener tantos elementos como el valor devuelto por la siguiente macro:

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Tenga en cuenta que la matriz de *lParam* debe contener valores [**MONTHDAYSTATE**](monthdaystate.md) que se correspondan con todos los meses que se encuentran actualmente en la pantalla del control, en orden cronológico. Esto incluye los dos meses que se pueden mostrar parcialmente antes del primer mes y después del último mes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar controles de calendario mensual](using-month-calendar-controls.md)
</dt> </dl>

 

 





