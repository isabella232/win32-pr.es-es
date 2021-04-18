---
title: Mensaje de MCM_GETMONTHRANGE (commctrl. h)
description: Recupera información de fecha (mediante estructuras SYSTEMTIME) que representa los límites máximo y mínimo de la presentación de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE controles de mensajes de Windows
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
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658414"
---
# <a name="mcm_getmonthrange-message"></a>Mensaje de MCM \_ GETMONTHRANGE

Recupera información de fecha (mediante estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) que representa los límites máximo y mínimo de la presentación de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica el ámbito de los límites de intervalo que se van a recuperar. Este valor debe ser uno de los siguientes:



| Value                                                                                                                                                      | Significado                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Incluye los meses anteriores y finales del intervalo visible que solo se muestran parcialmente. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ visible**</dt> </dl>    | Incluye solo los meses que se muestran por completo. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá los límites inferior y superior del ámbito especificado por *wParam*. Los límites inferior y superior se colocan en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 \] , respectivamente. Este parámetro debe ser una dirección válida y no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el intervalo, en meses, que abarcan los dos límites devueltos en *lParam*.

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

 

