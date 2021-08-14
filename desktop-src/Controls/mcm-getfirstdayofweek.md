---
title: MCM_GETFIRSTDAYOFWEEK mensaje (Commctrl.h)
description: Recupera el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319655"
---
# <a name="mcm_getfirstdayofweek-message"></a>Mensaje \_ GETFIRSTDAYOFWEEK de MCM

Recupera el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetFirstDayOfWeek.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene dos valores. La palabra alta es un valor **BOOL** distinto de cero si el primer día de la semana se establece en un valor distinto de LOCALE \_ IFIRSTDAYOFWEEK o cero en caso contrario. La palabra baja es un valor INT que representa el primer día de la semana, donde 0 es lunes, 1 es martes, y así sucesivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





