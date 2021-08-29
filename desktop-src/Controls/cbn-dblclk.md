---
title: CBN_DBLCLK de notificación (Winuser.h)
description: Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb37150aee923b63faf4eda54c66807d16b02f0e7a66183a2e5e55a29378307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770424"
---
# <a name="cbn_dblclk-notification-code"></a>Código de notificación \_ DBLCLK de CBN

Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_DBLCLK

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

Este código de notificación solo se produce para un cuadro combinado con el [**estilo \_ SIMPLE de CBS.**](combo-box-styles.md) En un cuadro combinado con el estilo DROPDOWN o [**\_ CBS DROPDOWNLIST**](combo-box-styles.md) de [**CBS, \_**](combo-box-styles.md) no se puede hacer doble clic porque un solo clic cierra el cuadro de lista.

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

 

