---
title: NM_SETCURSOR (ComboBoxEx) (Commctrl.h)
description: Notifica a la ventana primaria de un control ComboBoxEx que el control establece el cursor en respuesta a un mensaje \_ SETCURSOR de WM. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx) notification code Windows Controls
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
ms.openlocfilehash: aa0f7c7ffc8459ae1da279b6e53329f894662dd6ae6f30888fd9bdbdf631fa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798995"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>Código de notificación DE NM \_ SETCURSOR (ComboBoxEx)

Notifica a la ventana primaria de un control ComboBoxEx que el control establece el cursor en respuesta a un [**mensaje \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) de WM. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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



 

