---
description: Se envía a una ventana secundaria cuando el usuario hace clic en la barra de título de la ventana o cuando la ventana se activa, se mueve o se dimensiona.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: WM_CHILDACTIVATE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ff2e2e3e7c96880c38f63e5ff9975d44c37fcf21ce2bf2bd79bfc0b3ae9636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031013"
---
# <a name="wm_childactivate-message"></a>Mensaje \_ CHILDACTIVATE de WM

Se envía a una ventana secundaria cuando el usuario hace clic en la barra de título de la ventana o cuando la ventana se activa, se mueve o se dimensiona.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
