---
description: El mensaje de SYNCPAINT de WM \_ se usa para sincronizar el dibujo y evitar la vinculación de subprocesos GUI independientes.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Mensaje de WM_SYNCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997641"
---
# <a name="wm_syncpaint-message"></a>Mensaje de SYNCPAINT de WM \_

El mensaje de **\_ SYNCPAINT de WM** se usa para sincronizar el dibujo y evitar la vinculación de subprocesos GUI independientes.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
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

Una aplicación devuelve cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Cuando se oculta, se muestra, se mueve o se cambia el tamaño de una ventana, el sistema puede determinar que es necesario enviar un mensaje de **WM \_ SYNCPAINT** a las ventanas de nivel superior de otros subprocesos. Las aplicaciones deben pasar **WM \_ SYNCPAINT** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para su procesamiento. La función **DefWindowProc** enviará un mensaje de [**WM \_ NCPAINT**](wm-ncpaint.md) al procedimiento de ventana si se debe pintar el marco de ventana y enviar un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si se debe borrar el fondo de la ventana.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**pintura de WM \_**](wm-paint.md)
</dt> </dl>

 

 
