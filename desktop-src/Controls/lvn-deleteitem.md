---
title: LVN_DELETEITEM de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637cf2e8de98c056635cef2e68a7672f52b649c0162920f647384a2ceb4e64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062165"
---
# <a name="lvn_deleteitem-notification-code"></a>Código de notificación DELETEITEM de LVN \_

Notifica a la ventana primaria de un control de vista de lista que un elemento está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El **miembro iItem** identifica el elemento que se va a eliminar. Si el control no tiene el estilo **LVS \_ OWNERDATA,** *lParam* son los datos definidos por la aplicación asociados al elemento. Todos los demás miembros de esta estructura son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

No agregue, elimine ni reorganice elementos en la vista de lista mientras procesa este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





