---
title: CBN_EDITUPDATE de notificación (Winuser.h)
description: Se envía cuando la parte del control de edición de un cuadro combinado está a punto de mostrar texto modificado.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeaf787fd241d9dd87457273bd76c07eebe12fa99f2635643b4a4eaa8eaf4952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314735"
---
# <a name="cbn_editupdate-notification-code"></a>Código de notificación EDITUPDATE de CBN \_

Se envía cuando la parte del control de edición de un cuadro combinado está a punto de mostrar texto modificado. Este código de notificación se envía después de que el control haya dado formato al texto, pero antes de mostrar el texto. La ventana primaria del cuadro combinado recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del cuadro combinado. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el cuadro combinado tiene el estilo [**\_ DROPDOWNLIST de CBS,**](combo-box-styles.md) no se envía este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[CBN \_ EDITCHANGE](cbn-editchange.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

