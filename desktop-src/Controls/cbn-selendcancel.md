---
title: CBN_SELENDCANCEL de notificación (Winuser.h)
description: Se envía cuando el usuario selecciona un elemento, pero luego selecciona otro control o cierra el cuadro de diálogo. Indica que se omitirá la selección inicial del usuario. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173866"
---
# <a name="cbn_selendcancel-notification-code"></a>Código de notificación \_ DE CBN SELENDCANCEL

Se envía cuando el usuario selecciona un elemento, pero luego selecciona otro control o cierra el cuadro de diálogo. Indica que se omitirá la selección inicial del usuario. La ventana primaria del cuadro combinado recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del cuadro combinado. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En un cuadro combinado con el estilo SIMPLE de [**CBS, \_**](combo-box-styles.md) no se envía el código de notificación \_ DE CBN SELENDCANCEL. El [código de notificación DE \_ CBN SELENDOK](cbn-selendok.md) se envía inmediatamente antes de cada [código de notificación DE \_ CBN SELCHANGE.](cbn-selchange.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDOK](cbn-selendok.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

