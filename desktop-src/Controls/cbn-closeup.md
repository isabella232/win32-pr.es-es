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
ms.openlocfilehash: 79ff96f30a13705028a18199780da69948633c0c3381d87896f1c7137ae06041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085775"
---
# <a name="cbn_closeup-notification-code"></a>Código de notificación \_ de CLOSEUP de CBN

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

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del cuadro combinado. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el usuario cambió la selección actual, el cuadro combinado también envía el código de notificación [ \_ CBN SELCHANGE](cbn-selchange.md) cuando se cierra la lista desplegable. En general, no se puede predecir el orden en el que se enviarán los códigos de notificación. En concreto, un código de notificación CBN SELCHANGE puede producirse antes o después de un código de notificación \_ \_ CLOSEUP de CBN.

Para ejecutar un proceso específico cada vez que el usuario selecciona un elemento de lista, puede controlar el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) o CBN \_ CLOSEUP. Normalmente, esperaría el código de notificación DE \_ CBN CLOSEUP antes de procesar un cambio en la selección actual. Esto puede ser especialmente importante si se requiere una cantidad significativa de procesamiento.

Este código de notificación no se envía a un cuadro combinado que tenga el estilo [**\_ SIMPLE de CBS.**](combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

