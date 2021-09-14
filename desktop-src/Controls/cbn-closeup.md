---
title: CBN_CLOSEUP de notificación (Winuser.h)
description: Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173897"
---
# <a name="cbn_closeup-notification-code"></a>Código de notificación \_ DE CBN CLOSEUP

Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_CLOSEUP

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

## <a name="remarks"></a>Observaciones

Si el usuario cambió la selección actual, el cuadro combinado también envía el código de notificación [ \_ CBN SELCHANGE](cbn-selchange.md) cuando se cierra la lista desplegable. En general, no puede predecir el orden en el que se enviarán los códigos de notificación. En concreto, un código de notificación CBN SELCHANGE puede producirse antes o después de un código de \_ notificación \_ CLOSEUP de CBN.

Para ejecutar un proceso específico cada vez que el usuario selecciona un elemento de lista, puede controlar el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) o CBN \_ CLOSEUP. Normalmente, esperaría el código de notificación CLOSEUP de CBN antes \_ de procesar un cambio en la selección actual. Esto puede ser especialmente importante si se requiere una cantidad significativa de procesamiento.

Este código de notificación no se envía a un cuadro combinado que tenga el estilo [**\_ SIMPLE de CBS.**](combo-box-styles.md)

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

[LISTA DESPLEGABLE DE CBN \_](cbn-dropdown.md)
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

