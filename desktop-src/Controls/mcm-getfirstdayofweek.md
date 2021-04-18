---
title: Mensaje de MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Recupera el primer día de la semana de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK controles de mensajes de Windows
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
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658237"
---
# <a name="mcm_getfirstdayofweek-message"></a>Mensaje de MCM \_ GETFIRSTDAYOFWEEK

Recupera el primer día de la semana de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene dos valores. La palabra alta es un valor **booleano** que es distinto de cero si el primer día de la semana se establece en un valor distinto de IFIRSTDAYOFWEEK de configuración regional \_ , o bien cero en caso contrario. La palabra baja es un valor INT que representa el primer día de la semana, donde 0 es el lunes, 1 es el martes, etc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





