---
title: TCN_SELCHANGE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente ha cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166166"
---
# <a name="tcn_selchange-notification-code"></a>Código de notificación DE TCN \_ SELCHANGE

Notifica a la ventana primaria de un control de pestaña que la pestaña seleccionada actualmente ha cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para determinar la pestaña seleccionada actualmente, use la [**macro TabCtrl \_ GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TCN \_ SELCHANGING](tcn-selchanging.md)
</dt> </dl>

 

 





