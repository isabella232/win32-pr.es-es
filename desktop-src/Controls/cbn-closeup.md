---
title: Código de notificación de CBN_CLOSEUP (Winuser. h)
description: Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151207"
---
# <a name="cbn_closeup-notification-code"></a>Código de notificación de primer plano de CBN \_

Se envía cuando se ha cerrado el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el usuario ha cambiado la selección actual, el cuadro combinado también enviará el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) cuando se cierre la lista desplegable. En general, no puede predecir el orden en el que se enviarán los códigos de notificación. En concreto, un código de notificación de CBN \_ SELCHANGE puede producirse antes o después de un código de notificación de CBN \_ primer plano.

Para ejecutar un proceso específico cada vez que el usuario selecciona un elemento de lista, puede controlar el código de notificación [CBN \_ SELCHANGE](cbn-selchange.md) o CBN \_ primer plano. Normalmente, se espera el \_ código de notificación primer plano de CBN antes de procesar un cambio en la selección actual. Esto puede ser especialmente importante si se requiere una cantidad significativa de procesamiento.

Este código de notificación no se envía a un cuadro combinado que tenga el estilo [**\_ simple CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[\_lista desplegable CBN](cbn-dropdown.md)
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

