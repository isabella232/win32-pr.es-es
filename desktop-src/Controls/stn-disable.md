---
title: STN_DISABLE de notificación (Winuser.h)
description: El código de notificación DISABLE de STN \_ se envía cuando se deshabilita un control estático.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE código de notificación Windows controles
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166986"
---
# <a name="stn_disable-notification-code"></a>Código de notificación DE STN \_ DISABLE

El código de notificación DISABLE de STN \_ se envía cuando se deshabilita un control estático. El control estático debe tener el [**estilo NOTIFY de SS \_**](static-control-styles.md) para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control estático. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

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

[STN \_ ENABLE](stn-enable.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

