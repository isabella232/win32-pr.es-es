---
title: NM_SETCURSOR de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el control está estableciendo el cursor en respuesta a un mensaje \_ SETCURSOR de WM. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- NM_SETCURSOR código de notificación Windows controles
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
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167846"
---
# <a name="nm_setcursor-notification-code"></a>Código de notificación DE NM \_ SETCURSOR

Notifica a la ventana primaria de un control que el control está estableciendo el cursor en respuesta a un [**mensaje \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) de WM. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

