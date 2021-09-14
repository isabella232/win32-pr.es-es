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
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166169"
---
# <a name="tcn_selchanging-notification-code"></a>Código de notificación \_ DE TCN SELCHANGING

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

Devuelve **TRUE** para evitar que cambie la selección o **FALSE** para permitir que la selección cambie.

## <a name="remarks"></a>Observaciones

Para determinar la pestaña seleccionada actualmente, use la [**macro \_ TabCtrl GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TCN \_ SELCHANGE](tcn-selchange.md)
</dt> </dl>

 

 





