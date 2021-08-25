---
title: BN_PAINT de notificación (Winuser.h)
description: Se envía cuando se debe pintar un botón.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT código de notificación Windows controles
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3a412dac84fb5e65c7feb652588d6f16af0f49a8f61723ba48447dbbb2b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827605"
---
# <a name="bn_paint-notification-code"></a>Código de notificación de BN \_ PAINT

Se envía cuando se debe pintar un botón.

> [!Note]  
> Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows versiones anteriores a la versión 3.0. Las aplicaciones deben usar el [**estilo de botón \_ BS OWNERDRAW**](button-styles.md) y la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.

 

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_PAINT

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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

