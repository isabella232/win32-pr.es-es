---
description: Una aplicación envía el mensaje de SETREDRAW de WM \_ a una ventana para permitir que se vuelvan a dibujar los cambios en esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensaje de WM_SETREDRAW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277845"
---
# <a name="wm_setredraw-message"></a>Mensaje de SETREDRAW de WM \_

Una aplicación envía el mensaje de **\_ SETREDRAW de WM** a una ventana para permitir que se vuelvan a dibujar los cambios en esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.

Para enviar este mensaje, llame a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estado de redibujo. Si este parámetro es **true**, el contenido se puede volver a dibujar después de un cambio. Si este parámetro es **false**, no se puede volver a dibujar el contenido después de un cambio.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación devuelve cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje puede ser útil si una aplicación debe agregar varios elementos a un cuadro de lista. La aplicación puede llamar a este mensaje con *wParam* establecido en **false**, agregar los elementos y, a continuación, volver a llamar al mensaje con *wParam* establecido en **true**. Por último, la aplicación puede llamar a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **null**, **null**, RDW \_ Erase \| RDW \_ Frame \| RDW \_ Invalidate \| RDW \_ ALLCHILDREN) para hacer que el cuadro de lista se vuelva a dibujar.

> [!Note]  
> [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con las marcas especificadas se usa en lugar de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) porque el primero es necesario para algunos controles que tienen un área no cliente por su cuenta, o tienen estilos de ventana que provocan que se les proporcione un área no cliente (como **WS \_ THICKFRAME**, **WS \_ Border** o **WS \_ ex \_ CLIENTEDGE**). Si el control no tiene un área de cliente, **RedrawWindow** con estas marcas solo realizará la misma invalidación que **InvalidateRect** .

 

Si la aplicación envía el mensaje de **\_ SETREDRAW de WM** a una ventana oculta, la ventana se vuelve visible (es decir, el sistema operativo agrega el estilo **\_ visible de WS** a la ventana).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre pintura y dibujo](painting-and-drawing.md)
</dt> <dt>

[Pintar y dibujar mensajes](painting-and-drawing-messages.md)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
