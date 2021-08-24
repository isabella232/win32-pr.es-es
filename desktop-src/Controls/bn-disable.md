---
title: BN_DISABLE de notificación (Winuser.h)
description: Se envía cuando se deshabilita un botón.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- BN_DISABLE código de notificación Windows controles
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305515d7735da4528f91a961005ce50e9e1bb63459489947cb2ba5afd4d119e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439155"
---
# <a name="bn_disable-notification-code"></a>Código de notificación DISABLE de BN \_

Se envía cuando se deshabilita un botón.

> [!Note]  
> Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows anteriores a la versión 3.0. Las aplicaciones deben usar el [**estilo de botón \_ BS OWNERDRAW**](button-styles.md) y la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.

 

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_DISABLE

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

Controle el botón.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

