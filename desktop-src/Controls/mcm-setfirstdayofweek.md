---
title: Mensaje de MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Establece el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK controles de mensajes de Windows
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
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658374"
---
# <a name="mcm_setfirstdayofweek-message"></a>Mensaje de MCM \_ SETFIRSTDAYOFWEEK

Establece el primer día de la semana para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que representa el día que se va a establecer como primer día de la semana, donde 0 es el lunes, 1 es el martes, etc.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene dos valores. La palabra alta es un valor **booleano** que es distinto de cero si el primer día de la semana anterior no era igual a la configuración regional \_ IFIRSTDAYOFWEEK, o bien, cero en caso contrario. La palabra baja es un valor INT que representa el primer día de la semana anterior.

## <a name="remarks"></a>Observaciones

Si el primer día de la semana se establece en un valor distinto del predeterminado (configuración regional \_ IFIRSTDAYOFWEEK), el control no actualizará automáticamente los cambios del primer día de la semana en función de los cambios de la configuración regional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





