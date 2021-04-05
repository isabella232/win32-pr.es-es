---
title: Código de notificación de MCN_SELCHANGE (commctrl. h)
description: Se envía por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionado actualmente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079004"
---
# <a name="mcn_selchange-notification-code"></a>Código de notificación de SELCHANGE de MCN \_

Se envía por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionado actualmente. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Por ejemplo, el control envía MCN \_ SELCHANGE cuando el usuario cambia explícitamente la selección en el mes actual o cuando la selección se cambia implícitamente en respuesta a la navegación de mes anterior o siguiente. El sistema también envía este código de notificación a intervalos regulares para que el control pueda responder a los cambios de fecha.

Este código de notificación es similar a [MCN \_ Select](mcn-select.md), pero se envía como respuesta a cualquier cambio de selección. MCN \_ Select solo se envía para una selección de fecha explícita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





