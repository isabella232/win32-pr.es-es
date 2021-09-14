---
title: TVN_ITEMEXPANDING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING código de notificación Windows controles
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
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165542"
---
# <a name="tvn_itemexpanding-notification-code"></a>Código de notificación \_ DE TVN ITEMEXPANDING

Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) El **miembro itemNew** es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento primario en los **miembros hItem**, **state** y **lParam.** El **miembro** de acción indica si la lista se va a expandir o contraer. Para obtener una lista de los valores posibles, vea la descripción del [**mensaje \_ TVM EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que la lista se expanda o se contrae.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) y **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ELEMENTO DE \_ TVNEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





