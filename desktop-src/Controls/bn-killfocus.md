---
title: BN_KILLFOCUS de notificación (Winuser.h)
description: Se envía cuando un botón pierde el foco del teclado. El botón debe tener el estilo BS \_ NOTIFY para enviar este código de notificación. La ventana primaria del botón recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS código de notificación Windows controles
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062234"
---
# <a name="bn_killfocus-notification-code"></a>Código de notificación KILLFOCUS de BN \_

Se envía cuando un botón pierde el foco del teclado. El botón debe tener el estilo [**BS \_ NOTIFY**](button-styles.md) para enviar este código de notificación.

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del botón.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[BN \_ SETFOCUS](bn-setfocus.md)
</dt> </dl>

 

