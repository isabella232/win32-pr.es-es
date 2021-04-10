---
title: Mensaje de DTM_GETSYSTEMTIME (commctrl. h)
description: Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura SYSTEMTIME especificada. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetSystemtime de DateTime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150673"
---
# <a name="dtm_getsystemtime-message"></a>DTM \_ GETSYSTEMTIME Message

Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetSystemtime de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Si **DTM \_ GETSYSTEMTIME** devuelve GDT \_ Valid, esta estructura contendrá la hora seleccionada actualmente. De lo contrario, no contendrá información válida. Este parámetro debe ser un puntero válido; no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve GDT \_ válido si la información de hora se colocó correctamente en *lParam*. Devuelve GDT \_ None si el control se estableció en el estilo [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) y no se activó la casilla Control. Devuelve \_ un error de GDT si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

