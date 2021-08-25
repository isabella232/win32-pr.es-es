---
title: BN_HILITE de notificación (Winuser.h)
description: Se envía cuando el usuario selecciona un botón.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE código de notificación Windows controles
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e864fff01fcce9c7856ab040f66d12e08524c731b43d343a2e878e15e41e801f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827625"
---
# <a name="bn_hilite-notification-code"></a>Código de notificación hilite de BN \_

Se envía cuando el usuario selecciona un botón.

> [!Note]  
> Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows versiones anteriores a la versión 3.0. Las aplicaciones deben usar el [**estilo de botón \_ BS OWNERDRAW**](button-styles.md) y la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para esta tarea.

 

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_HILITE

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

Controle el botón.

</dd> </dl>

## <a name="remarks"></a>Comentarios

BN \_ HILITE es igual que el código de notificación [ \_ PUSHED de BN.](bn-pushed.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

