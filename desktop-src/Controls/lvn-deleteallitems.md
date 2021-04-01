---
title: Código de notificación de LVN_DELETEALLITEMS (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997188"
---
# <a name="lvn_deleteallitems-notification-code"></a>Código de notificación de DELETEALLITEMS de LVN \_

Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . El miembro **iItem** es-1 y los demás miembros son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para suprimir los códigos de notificación [LVN \_ DELETEITEM](lvn-deleteitem.md) posteriores, devuelva **true**.

Para recibir los códigos de notificación de [LVN \_ DELETEITEM](lvn-deleteitem.md) posteriores, devuelva **false**.

## <a name="remarks"></a>Observaciones

Un control de vista de lista envía el código de notificación del [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) cuando se destruye o cuando recibe el mensaje **\_ DELETEALLITEMS de LVM** . Si **el \_ DELETEALLITEMS LVM** no devuelve **true**, el control también enviará un código de notificación [LVN \_ DELETEITEM](lvn-deleteitem.md) a medida que se elimine cada elemento.

Si el controlador de mensajes [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) está en un procedimiento de cuadro de diálogo, devuelva **true** en el procedimiento de cuadro de diálogo y use la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT para establecer el valor devuelto del mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

