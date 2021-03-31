---
title: Mensaje de MCM_GETCURSEL (commctrl. h)
description: Recupera la fecha seleccionada actualmente. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL controles de mensajes de Windows
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
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491447"
---
# <a name="mcm_getcursel-message"></a>Mensaje de MCM \_ GETCURSEL

Recupera la fecha seleccionada actualmente. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha seleccionada actualmente. Este parámetro debe ser una dirección válida y no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario. Este mensaje siempre producirá un error cuando se aplique a los controles de calendario mensual establecidos en el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

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

 

