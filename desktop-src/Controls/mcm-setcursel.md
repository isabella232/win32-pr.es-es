---
title: Mensaje de MCM_SETCURSEL (commctrl. h)
description: Establece la fecha seleccionada actualmente para un control de calendario mensual. Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca en la vista. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658376"
---
# <a name="mcm_setcursel-message"></a>Mensaje de MCM \_ SETCURSEL

Establece la fecha seleccionada actualmente para un control de calendario mensual. Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca en la vista. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la fecha que se va a establecer como la selección actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario. Se producirá un error en este mensaje si se aplica a un control de calendario mensual que use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas en el control de calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

