---
title: TVN_DELETEITEM de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165573"
---
# <a name="tvn_deleteitem-notification-code"></a>Código de notificación DELETEITEM de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) El **miembro itemOld** es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos **miembros hItem** y **lParam** contienen información válida sobre el elemento que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Si el **miembro lParam** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) apunta a la memoria asignada por la aplicación, puede liberarla cuando reciba el código de notificación \_ DELETEITEM de TVN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) y **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





