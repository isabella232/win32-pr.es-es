---
title: Mensaje de MCM_GETTODAY (commctrl. h)
description: Recupera la información de fecha de la fecha especificada como \ 0034; hoy \ 0034; para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY controles de mensajes de Windows
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
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996463"
---
# <a name="mcm_gettoday-message"></a>Mensaje de MCM \_ GETTODAY

Recupera la información de fecha de la fecha especificada como "hoy" para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de fecha. Este parámetro debe ser una dirección válida y no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas en el control de calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

