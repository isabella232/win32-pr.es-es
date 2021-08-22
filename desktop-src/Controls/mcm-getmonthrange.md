---
title: MCM_GETMONTHRANGE mensaje (Commctrl.h)
description: Recupera información de fecha (mediante estructuras SYSTEMTIME) que representa los límites altos y bajos de la presentación de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la \_ macro MonthCal GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc55f9732199f2e6e031248003c6dcad4abe8cb713182081666cfbee6a4ce50b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319585"
---
# <a name="mcm_getmonthrange-message"></a>Mensaje \_ GETMONTHRANGE de MCM

Recupera información de fecha (mediante [**estructuras SYSTEMTIME)**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que representa los límites altos y bajos de la presentación de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetMonthRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica el ámbito de los límites de intervalo que se van a recuperar. Este valor debe ser uno de los siguientes:



| Valor                                                                                                                                                      | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Incluya los meses anteriores y finales del intervalo visible que solo se muestran parcialmente. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ VISIBLE**</dt> </dl>    | Incluya solo los meses que se muestran por completo. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá los límites inferior y superior del ámbito especificado por *wParam*. Los límites inferior y superior se colocan *en lprgSysTimeArray* 0 y \[ \] *lprgSysTimeArray* \[ \] 1, respectivamente. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el intervalo, en meses, abarcado por los dos límites devueltos en *lParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Horas del control Calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

