---
title: TVN_SELCHANGING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que la selección está a punto de cambiar de un elemento a otro. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165538"
---
# <a name="tvn_selchanging-notification-code"></a>Código de notificación \_ DE TVN SELCHANGING

Notifica a la ventana primaria de un control de vista de árbol que la selección está a punto de cambiar de un elemento a otro. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Los **miembros itemOld** y **itemNew** contienen información válida sobre el elemento seleccionado actualmente y el elemento recién seleccionado. El **miembro** de acción indica si una acción del mouse o del teclado está provocando que cambie la selección. Para obtener una lista de los valores posibles, vea la descripción del código de [notificación \_ DE TVN SELCHANGED.](tvn-selchanged.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que la selección cambie.

## <a name="remarks"></a>Observaciones

Al responder a este código de notificación, las aplicaciones no deben eliminar los elementos que ganan o pierden la selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ SELCHANGINGW** (Unicode) y **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





