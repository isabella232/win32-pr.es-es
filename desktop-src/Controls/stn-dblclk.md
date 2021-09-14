---
title: STN_DBLCLK de notificación (Winuser.h)
description: El código de notificación DBLCLK de STN se envía cuando el usuario hace doble clic en un control estático que tiene el \_ estilo NOTIFY de \_ SS. La ventana primaria del control recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK código de notificación Windows controles
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166989"
---
# <a name="stn_dblclk-notification-code"></a>Código de notificación \_ DBLCLK de STN

El código de notificación DBLCLK de STN se envía cuando el usuario hace doble clic en un control estático que tiene el \_ [**estilo NOTIFY \_ de SS.**](static-control-styles.md) La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_DBLCLK

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

[STN \_ CLICKED](stn-clicked.md)
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

 

