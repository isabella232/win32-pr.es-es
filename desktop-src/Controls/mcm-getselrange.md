---
title: MCM_GETSELRANGE mensaje (Commctrl.h)
description: Recupera información de fecha que representa los límites superior e inferior del intervalo de fechas seleccionado actualmente por el usuario. Puede enviar este mensaje explícitamente o mediante la macro \_ MonthCal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7c446c98a43714a8cd839704050d2aedd1b7eab83b9199700ba24dd4e2be98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061955"
---
# <a name="mcm_getselrange-message"></a>Mensaje \_ GETSELRANGE de MCM

Recupera información de fecha que representa los límites superior e inferior del intervalo de fechas seleccionado actualmente por el usuario. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetSelRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá los límites inferior y superior de la selección del usuario. Los límites inferior y superior se colocan *en lprgSysTimeArray* 0 y \[ \] *lprgSysTimeArray* \[ \] 1, respectivamente. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. **MCM \_ GETSELRANGE producirá** un error si se aplica a un control de calendario mensual que no usa el estilo [**\_ MULTISELECT de MCS.**](month-calendar-control-styles.md)

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

 

