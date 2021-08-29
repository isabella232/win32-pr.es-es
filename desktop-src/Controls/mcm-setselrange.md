---
title: MCM_SETSELRANGE mensaje (Commctrl.h)
description: Establece la selección de un control de calendario mensual en un intervalo de fechas determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdf6708aa382abfa92562aa55943c06180d0231cff568b74de380416e48731a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018983"
---
# <a name="mcm_setselrange-message"></a>Mensaje \_ SETELRANGE de MCM

Establece la selección de un control de calendario mensual en un intervalo de fechas determinado. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetSelRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contienen información de fecha que representa los límites de selección. La primera fecha seleccionada debe especificarse en *lpSysTimeArray* 0 y la última fecha seleccionada debe especificarse en \[ \] *lpSysTimeArray* \[ \] 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. Este mensaje producirá un error si se aplica a un control de calendario mensual que no usa el estilo [**\_ MULTISELECT de MCS.**](month-calendar-control-styles.md)

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

 

