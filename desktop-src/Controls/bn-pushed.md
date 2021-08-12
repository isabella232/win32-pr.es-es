---
title: BN_PUSHED de notificación (Winuser.h)
description: Se envía cuando el estado de inserción de un botón se establece en pushed.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED código de notificación Windows controles
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d95210ebe5abaddabcc33b908baf1cb2c1498af7446f32d7ebcfa9500ebd329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674139"
---
# <a name="bn_pushed-notification-code"></a>Código de notificación PUSHED de BN \_

Se envía cuando el estado de inserción de un botón se establece en pushed.

> [!Note]  
> Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows versiones anteriores a la versión 3.0. Las aplicaciones deben usar el [**estilo de botón \_ BS OWNERDRAW**](button-styles.md) y la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.

 

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del botón.

</dd> </dl>

## <a name="remarks"></a>Observaciones

BN \_ PUSHED es el mismo que el código de notificación de [ \_ HILITE de BN.](bn-hilite.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BN \_ UNPUSHED**](bn-unpushed.md)
</dt> </dl>

 

