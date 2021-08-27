---
title: MCM_SETFIRSTDAYOFWEEK mensaje (Commctrl.h)
description: Establece el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la \_ macro SetFirstDayOfWeek de MonthCal.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077115"
---
# <a name="mcm_setfirstdayofweek-message"></a>Mensaje \_ SETFIRSTDAYOFWEEK de MCM

Establece el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetFirstDayOfWeek de MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que representa qué día se va a establecer como primer día de la semana, donde 0 es Lunes, 1 es Martes, y así sucesivamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene dos valores. La palabra alta es un **valor BOOL** distinto de cero si el primer día de la semana anterior no era igual a LOCALE \_ IFIRSTDAYOFWEEK o cero en caso contrario. La palabra baja es un valor INT que representa el primer día de la semana anterior.

## <a name="remarks"></a>Comentarios

Si el primer día de la semana se establece en algo distinto del valor predeterminado (LOCALE IFIRSTDAYOFWEEK), el control no actualizará automáticamente los cambios del primer día de la semana en función de los cambios de configuración \_ regional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





