---
title: MCM_SETCURSEL mensaje (Commctrl.h)
description: Establece la fecha seleccionada actualmente para un control de calendario mensual. Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL controles de Windows mensaje
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
ms.openlocfilehash: e63238f11f93e56c18e1897fcdd3cb96977f23fe16bde19123b5c063f99c0ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061895"
---
# <a name="mcm_setcursel-message"></a>Mensaje \_ SETCURSEL de MCM

Establece la fecha seleccionada actualmente para un control de calendario mensual. Si la fecha especificada no está en la vista, el control actualiza la pantalla para que aparezca. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la fecha que se va a establecer como la selección actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. Este mensaje producirá un error si se aplica a un control de calendario mensual que usa el [**estilo \_ MULTISELECT de MCS.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas del control Calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

