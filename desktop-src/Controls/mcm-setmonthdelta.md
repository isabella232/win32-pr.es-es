---
title: MCM_SETMONTHDELTA mensaje (Commctrl.h)
description: Establece la velocidad de desplazamiento de un control de calendario mensual. La velocidad de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a148bac8ee28d4e3ebeb370d9fcacb678730bc77baac0b42f3f14b8f65a57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005386"
---
# <a name="mcm_setmonthdelta-message"></a>Mensaje \_ SETMONTHDELTA de MCM

Establece la velocidad de desplazamiento de un control de calendario mensual. La velocidad de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetMonthDelta.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa el número de meses que se establecerán como velocidad de desplazamiento del control. Si este valor es cero, la diferencia de mes se restablece al valor predeterminado, que es el número de meses que se muestran en el control .

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa la velocidad de desplazamiento anterior. Si no se estableció previamente la velocidad de desplazamiento, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Las claves PAGE UP y PAGE DOWN, VK PRIOR y VK NEXT, cambian el mes seleccionado por uno, independientemente del número de meses mostrados o del valor establecido por \_ \_ **MCM \_ SETMONTHDELTA.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





