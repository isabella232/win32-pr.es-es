---
title: TCN_SELCHANGING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente está a punto de cambiar. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING código de notificación Windows controles
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75fbf92139a43b19d41fce0fd607932531fef7e23556330b9bda376945a21080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104675"
---
# <a name="tcn_selchanging-notification-code"></a>Código de notificación DE TCN \_ SELCHANGING

Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente está a punto de cambiar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que cambie la selección o **FALSE** para permitir que cambie la selección.

## <a name="remarks"></a>Comentarios

Para determinar la pestaña seleccionada actualmente, use la [**macro TabCtrl \_ GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TCN \_ SELCHANGE](tcn-selchange.md)
</dt> </dl>

 

 





