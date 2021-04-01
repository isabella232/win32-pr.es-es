---
title: Mensaje de MCM_GETMONTHDELTA (commctrl. h)
description: Recupera la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151279"
---
# <a name="mcm_getmonthdelta-message"></a>Mensaje de MCM \_ GETMONTHDELTA

Recupera la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la diferencia de mes se estableció previamente mediante el mensaje de [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , devuelve un valor int que representa la tasa de desplazamiento actual del calendario mensual. Si la diferencia de mes no se estableció previamente con el mensaje de **MCM \_ SETMONTHDELTA** o si la diferencia de mes se restableció al valor predeterminado, devuelve un valor int que representa el número actual de meses visibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





