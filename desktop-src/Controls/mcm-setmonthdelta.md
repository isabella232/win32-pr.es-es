---
title: Mensaje de MCM_SETMONTHDELTA (commctrl. h)
description: Establece la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA controles de mensajes de Windows
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
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658373"
---
# <a name="mcm_setmonthdelta-message"></a>Mensaje de MCM \_ SETMONTHDELTA

Establece la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa el número de meses que se va a establecer como la tasa de desplazamiento del control. Si este valor es cero, la diferencia de mes se restablece en el valor predeterminado, que es el número de meses que se muestran en el control.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa la tasa de desplazamiento anterior. Si la tasa de desplazamiento no se estableció previamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Las teclas Re Pág y Av Pág, VK \_ anterior y VK \_ Next, cambian el mes seleccionado en uno, independientemente del número de meses que se muestren o del valor establecido por **MCM \_ SETMONTHDELTA**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





