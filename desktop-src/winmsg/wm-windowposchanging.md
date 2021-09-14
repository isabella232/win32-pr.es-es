---
description: Se envía a una ventana cuyo tamaño, posición o posición en el orden Z está a punto de cambiar como resultado de una llamada a la función SetWindowPos u otra función de administración de ventanas.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: WM_WINDOWPOSCHANGING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251630"
---
# <a name="wm_windowposchanging-message"></a>WM \_ WINDOWPOSCHANGING message

Se envía a una ventana cuyo tamaño, posición o posición en el orden Z está a punto de cambiar como resultado de una llamada a la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) u otra función de administración de ventanas.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Puntero a una [**estructura WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que contiene información sobre el nuevo tamaño y la posición de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Para una ventana con el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ THICKFRAME,** la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía el mensaje [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) a la ventana. Esto se hace para validar el nuevo tamaño y la posición de la ventana y para aplicar los estilos de cliente [ \_ BYTEALIGNCLIENT](about-window-classes.md) y CS \_ BYTEALIGNWINDOW de CS. Al no pasar el **mensaje WM \_ WINDOWPOSCHANGING** a la función **DefWindowProc,** una aplicación puede invalidar estos valores predeterminados.

Mientras se procesa este mensaje, la modificación de cualquiera de los valores de [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) afecta al nuevo tamaño, la posición o la posición de la ventana en el orden Z. Una aplicación puede evitar cambios en la ventana estableciendo o borrando los bits adecuados en el **miembro flags** de **WINDOWPOS.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**TAMAÑO \_ DE WM**](wm-size.md)
</dt> <dt>

[**VENTANA \_ WMPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
