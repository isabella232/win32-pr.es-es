---
title: MCN_GETDAYSTATE de notificación (Commctrl.h)
description: Enviado por un control de calendario mensual para solicitar información sobre cómo se deben mostrar los días individuales. Este código de notificación solo se envía mediante controles de calendario mensuales que usan el estilo DAYSTATE de MCS y se envía en forma de \_ mensaje WM \_ NOTIFY.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE código de notificación Windows controles
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64af64fde86ed91ae41cbd3fed53e9cb27a0be410140bc1d25e0548a64042668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697146"
---
# <a name="mcn_getdaystate-notification-code"></a>Código de notificación \_ GETDAYSTATE de MCN

Enviado por un control de calendario mensual para solicitar información sobre cómo se deben mostrar los días individuales. Este código de notificación solo se envía mediante controles de calendario mensuales que usan el estilo [**\_ DAYSTATE**](month-calendar-control-styles.md) de MCS y se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMDAYSTATE.**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) La estructura contiene información sobre el período de tiempo para el que el control necesita información y recibe la dirección de una matriz que proporciona estos datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El control de este código de notificación permite a la aplicación personalizar su presentación especificando que determinados días se muestren en negrita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





