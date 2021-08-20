---
title: MCM_GETCURSEL mensaje (Commctrl.h)
description: Recupera la fecha seleccionada actualmente. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40ed6797cd7f40eb68e40a9eac90eb250badd461011e5490c0f4c8473571bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170212"
---
# <a name="mcm_getcursel-message"></a>Mensaje \_ GETCURSEL de MCM

Recupera la fecha seleccionada actualmente. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha seleccionada actualmente. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. Este mensaje siempre producirá un error cuando se aplique a los controles de calendario mensuales establecidos en el [**estilo \_ MULTISELECT de MCS.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas del control Calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

