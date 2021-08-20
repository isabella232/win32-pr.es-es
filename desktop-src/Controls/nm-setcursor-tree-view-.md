---
title: NM_SETCURSOR de notificación (vista de árbol) (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un mensaje \_ SETCURSOR de WM. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- NM_SETCURSOR (vista de árbol) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7791ff62fa9ed097052ebd38dae0000d7165519133527044e9716bb7e39c655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410462"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>Código de notificación de NM \_ SETCURSOR (vista de árbol)

Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un [**mensaje \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) de WM. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que el control establezca el cursor o distinto de cero para evitar que el control establezca el cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

