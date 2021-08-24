---
description: El mensaje PRINTCLIENT de WM se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto \_ de dispositivo de impresora.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: WM_PRINTCLIENT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717665"
---
# <a name="wm_printclient-message"></a>Mensaje \_ PRINTCLIENT de WM

El **mensaje \_ PRINTCLIENT de WM** se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.

A [**diferencia de WM \_ PRINT,**](wm-print.md) [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)no procesa **WM \_ PRINTCLIENT.** Una ventana debe procesar el **mensaje \_ PRINTCLIENT de WM** a través de una función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definida por la aplicación para que se utilice correctamente.


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

Identificador del contexto del dispositivo en el que se dibujará.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de dibujo. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Dibuja la ventana solo si está visible.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Dibuja todas las ventanas de los secundarios visibles.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**CLIENTE DE \_ PRF**</dt> </dl>                   | Dibuja el área de cliente de la ventana.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEB PREPND**</dt> </dl>       | Borra el fondo antes de dibujar la ventana.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Dibuja el área no cliente de la ventana.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PROPIEDAD \_ DE PRF**</dt> </dl>                      | Dibuja todas las ventanas de propiedad.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una ventana puede procesar este mensaje de la misma manera que [**WM \_ PAINT,**](./wm-paint.md)salvo que no es necesario llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (se proporciona un contexto de dispositivo) y la ventana debe dibujar toda su área de cliente en lugar de solo la región no válida.

Windows que se puede usar en cualquier parte del sistema, como los controles, debe procesar este mensaje. Probablemente merece la pena que otras ventanas también procesen este mensaje porque es relativamente fácil de implementar.

La [función AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) requiere que la ventana que se anima implemente el **mensaje \_ PRINTCLIENT de WM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre dibujo y dibujo](painting-and-drawing.md)
</dt> <dt>

[Pintar y dibujar mensajes](painting-and-drawing-messages.md)
</dt> <dt>

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
