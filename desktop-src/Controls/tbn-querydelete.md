---
title: TBN_QUERYDELETE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas si un botón se puede eliminar de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166326"
---
# <a name="tbn_querydelete-notification-code"></a>Código de notificación QUERYDELETE de TBN \_

Notifica a la ventana primaria de la barra de herramientas si un botón se puede eliminar de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) El miembro **iItem** contiene el índice basado en cero del botón que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para permitir que se elimine el botón o **FALSE** para evitar que se elimine el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





