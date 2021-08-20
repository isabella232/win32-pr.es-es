---
title: TVN_ITEMEXPANDING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f4403b41682590d305b527d6445c208011b368b2d2474d66720ed32d29c80ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957794"
---
# <a name="tvn_itemexpanding-notification-code"></a>Código de notificación \_ ITEMEXPANDING de TVN

Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) El **miembro itemNew** es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento primario en los **miembros hItem**, **state** y **lParam.** El **miembro** de acción indica si la lista se va a expandir o contraer. Para obtener una lista de los valores posibles, vea la descripción del [**mensaje \_ EXPAND de TVM.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que la lista se expanda o se contrae.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) y **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ELEMENTO DE \_ TVNEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





