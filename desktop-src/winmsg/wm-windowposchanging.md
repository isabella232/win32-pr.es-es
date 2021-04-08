---
description: Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z está a punto de cambiar como resultado de una llamada a la función SetWindowPos u otra función de administración de ventanas.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Mensaje de WM_WINDOWPOSCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816307"
---
# <a name="wm_windowposchanging-message"></a>Mensaje de WINDOWPOSCHANGING de WM \_

Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z está a punto de cambiar como resultado de una llamada a la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) u otra función de administración de ventanas.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) que contiene información sobre el nuevo tamaño y la posición de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

En el caso de una ventana con el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ THICKFRAME** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía el mensaje de [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) a la ventana. Esto se hace para validar el nuevo tamaño y la posición de la ventana y aplicar los estilos [CS \_ BYTEALIGNCLIENT](about-window-classes.md) y CS \_ BYTEALIGNWINDOW Client. Al no pasar el mensaje de **\_ WINDOWPOSCHANGING de WM** a la función **DefWindowProc** , una aplicación puede invalidar estos valores predeterminados.

Mientras se está procesando este mensaje, la modificación de los valores de [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) afecta al nuevo tamaño, posición o lugar en el orden Z. Una aplicación puede evitar cambios en la ventana estableciendo o borrando los bits adecuados en el miembro **Flags** de **windowpos (**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS (**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**GETMINMAXINFO de WM \_**](wm-getminmaxinfo.md)
</dt> <dt>

[**movimiento de WM \_**](wm-move.md)
</dt> <dt>

[**tamaño de WM \_**](wm-size.md)
</dt> <dt>

[**WINDOWPOSCHANGED de WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
