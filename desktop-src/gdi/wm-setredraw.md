---
description: Envíe el mensaje **WM_SETREDRAW** a una ventana para permitir que se vuelvan a dibujar los cambios de esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593461"
---
# <a name="wm_setredraw-message"></a>WM_SETREDRAW mensaje

El mensaje **WM \_ SETREDRAW** se envía a una ventana para permitir que se vuelvan a dibujar los cambios de esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.

Para enviar este mensaje, llame a la [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a>Parámetros

`wParam`

Estado de volver a dibujar. Si este parámetro es **TRUE,** el contenido se puede volver a dibujar después de un cambio. Si este parámetro es **FALSE,** no se puede volver a dibujar el contenido después de un cambio.

`lParam`

Este parámetro no se usa.

## <a name="return-value"></a>Valor devuelto

La aplicación debe devolver 0 si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje puede ser útil si la aplicación debe agregar varios elementos a un cuadro de lista. La aplicación puede llamar a este mensaje con *wParam* establecido en **FALSE,** agregar los elementos y, a continuación, volver a llamar al mensaje con *wParam* establecido en **TRUE.** Por último, la aplicación puede llamar a [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, \_ RDW ERASE \| RDW \_ FRAME \| RDW \_ INVALIDATE \| RDW \_ ALLCHILDREN) para hacer que se vuelva a dibujar el cuadro de lista.

> [!NOTE] 
> Debe usar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) con las marcas especificadas, en lugar de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), porque la primera es necesaria para algunos controles que tienen su propio área no cliente o tienen estilos de ventana que hacen que se les de un área no cliente (como **WS_THICKFRAME**, **WS_BORDER** o **WS_EX_CLIENTEDGE**). Si el control no tiene un área no cliente, **RedrawWindow** con estas marcas solo hará tanta invalidación como **Lo haría InvalidateRect.**

Al pasar **un WM_SETREDRAW** a la función **DefWindowProc** se quita el estilo **WS_VISIBLE** de la ventana cuando *wParam* está establecido en **FALSE.** Aunque el contenido de la ventana permanece visible en la pantalla, la función [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) devuelve **FALSE** cuando se llama a en una ventana en este estado. 

Al pasar **un WM_SETREDRAW** a la función **DefWindowProc** se agrega el estilo **WS_VISIBLE** a la ventana, si no se establece, cuando *wParam* se establece en **TRUE.** Si la aplicación envía el **mensaje WM_SETREDRAW** con *wParam* establecido en **TRUE** en una ventana oculta, la ventana se vuelve visible. 

**Windows 10 y versiones posteriores; Windows Server 2016 y versiones posteriores.** El sistema establece una propiedad denominada *SysSetRedraw* en una ventana cuyo procedimiento de ventana **pasa** WM_SETREDRAW mensajes a **DefWindowProc**. Puede usar la [**función GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) para obtener el valor de propiedad cuando esté disponible. **GetProp** devuelve un valor distinto de cero cuando se deshabilita volver a dibujar. **GetProp** devolverá cero cuando se habilite volver a dibujar o cuando la propiedad de ventana no exista. 

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional |
| Servidor mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Server |
| Encabezado | <dl><dt>Winuser.h (incluir Windows.h)</dt></dl> |

## <a name="see-also"></a>Vea también

* [Información general sobre dibujo y dibujo](painting-and-drawing.md)
* [Pintar y dibujar mensajes](painting-and-drawing-messages.md)
* [Volver a dibujarWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
