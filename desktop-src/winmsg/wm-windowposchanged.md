---
description: Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z ha cambiado como resultado de una llamada a la función SetWindowPos u otra función de administración de ventanas.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Mensaje de WM_WINDOWPOSCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154166"
---
# <a name="wm_windowposchanged-message"></a>Mensaje de WINDOWPOSCHANGED de WM \_

Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z ha cambiado como resultado de una llamada a la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) u otra función de administración de ventanas.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGED             0x0047
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

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de [**\_ tamaño de WM**](wm-size.md) y de [**\_ movimiento de WM**](wm-move.md) a la ventana. Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**. Es más eficaz realizar cualquier procesamiento de cambios de movimiento o de tamaño durante el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.

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

[**movimiento de WM \_**](wm-move.md)
</dt> <dt>

[**tamaño de WM \_**](wm-size.md)
</dt> <dt>

[**WINDOWPOSCHANGING de WM \_**](wm-windowposchanging.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
