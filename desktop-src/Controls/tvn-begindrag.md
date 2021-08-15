---
title: TVN_BEGINDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que se está iniciando una operación de arrastrar y colocar que implica el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95952ee42dfe8eb8dd1a46c66dcd452f41cbc9723fa175c2a0d1fc75056c31ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957924"
---
# <a name="tvn_begindrag-notification-code"></a>Código de notificación \_ BEGINDRAG de TVN

Notifica a la ventana primaria de un control de vista de árbol que se está iniciando una operación de arrastrar y colocar que implica el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) El **miembro itemNew** es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento que se arrastra en los **miembros hItem**, **state** y **lParam.** El **miembro ptDrag** especifica las coordenadas de pantalla actuales del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Un control de vista de árbol que tenga el estilo [**TVS \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) no envía este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ BEGINDRAGW** (Unicode) y **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





