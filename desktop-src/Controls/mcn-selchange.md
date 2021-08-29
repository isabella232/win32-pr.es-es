---
title: MCN_SELCHANGE de notificación (Commctrl.h)
description: Enviado por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionados actualmente. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE código de notificación Windows controles
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
ms.openlocfilehash: 3aa4c1d1f2d4c99ab9980deae4b64dc25fa7caf0818df31d1f160b2b1645d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915025"
---
# <a name="mcn_selchange-notification-code"></a>Código de notificación \_ DE MCN SELCHANGE

Enviado por un control de calendario mensual cuando cambia la fecha o el intervalo de fechas seleccionados actualmente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Por ejemplo, el control envía MCN SELCHANGE cuando el usuario cambia explícitamente la selección dentro del mes actual o cuando la selección cambia implícitamente en respuesta a la navegación del mes siguiente o \_ anterior. El sistema también envía este código de notificación a intervalos regulares para que el control pueda responder a los cambios de fecha.

Este código de notificación es similar a [MCN \_ SELECT,](mcn-select.md)pero se envía en respuesta a cualquier cambio de selección. MCN \_ SELECT solo se envía para una selección de fecha explícita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





