---
title: MCM_GETMONTHDELTA mensaje (Commctrl.h)
description: Recupera la velocidad de desplazamiento de un control de calendario mensual. La velocidad de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro \_ GetMonthDelta de MonthCal.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA controles de Windows mensaje
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
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319615"
---
# <a name="mcm_getmonthdelta-message"></a>Mensaje \_ GETMONTHDELTA de MCM

Recupera la velocidad de desplazamiento de un control de calendario mensual. La velocidad de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetMonthDelta de MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la diferencia del mes se estableció previamente mediante el mensaje [**\_ SETMONTHDELTA de MCM,**](mcm-setmonthdelta.md) devuelve un valor INT que representa la velocidad de desplazamiento actual del calendario mensual. Si la diferencia del mes no se estableció previamente mediante el mensaje **\_ SETMONTHDELTA** de MCM o la diferencia de mes se restablecía al valor predeterminado, devuelve un valor INT que representa el número actual de meses visibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





