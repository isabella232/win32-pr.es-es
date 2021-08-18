---
title: MCM_GETTODAY mensaje (Commctrl.h)
description: Recupera la información de fecha de la fecha especificada como \ 0034; hoy \ 0034; para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6925ff24a2d3e042a4f2c752d87642f74345116fc5cc7f94e00e811d453be4fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019033"
---
# <a name="mcm_gettoday-message"></a>Mensaje \_ GETTODAY de MCM

Recupera la información de fecha de la fecha especificada como "today" para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetToday.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

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

 

