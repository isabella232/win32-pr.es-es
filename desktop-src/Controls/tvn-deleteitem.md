---
title: Código de notificación de TVN_DELETEITEM (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490840"
---
# <a name="tvn_deleteitem-notification-code"></a>Código de notificación de TVN \_ DELETEITEM

Notifica a la ventana primaria de un control de vista de árbol que se está eliminando un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . El miembro **itemOld** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **hItem** e **lParam** contienen información válida sobre el elemento que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Si el miembro **lParam** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) apunta a la memoria asignada por la aplicación, puede liberarla cuando reciba el código de \_ notificación TVN DELETEITEM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) y **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





