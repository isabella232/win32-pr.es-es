---
description: El mensaje de PRINTCLIENT de WM \_ se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Mensaje de WM_PRINTCLIENT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985799"
---
# <a name="wm_printclient-message"></a>Mensaje de PRINTCLIENT de WM \_

El mensaje de **\_ PRINTCLIENT de WM** se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.

A diferencia de la [**\_ impresión de WM**](wm-print.md), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)no procesa **\_ PRINTCLIENT** . Una ventana debe procesar el mensaje de **\_ PRINTCLIENT de WM** a través de una función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definida por la aplicación para que se use correctamente.


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

Identificador del contexto de dispositivo en el que se va a dibujar.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de dibujo. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Dibuja la ventana solo si está visible.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**\_elementos secundarios PRF**</dt> </dl>             | Dibuja todas las ventanas secundarias visibles.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_cliente PRF**</dt> </dl>                   | Dibuja el área cliente de la ventana.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Borra el fondo antes de dibujar la ventana.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**no \_ cliente PRF**</dt> </dl>          | Dibuja el área no cliente de la ventana.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**propiedad de PRF \_**</dt> </dl>                      | Dibuja todas las ventanas de propiedad.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una ventana puede procesar este mensaje de la misma manera que en [**WM \_ Paint**](./wm-paint.md), salvo que no es necesario llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (se proporciona un contexto de dispositivo) y la ventana debe dibujar todo el área cliente en lugar de simplemente la región no válida.

Las ventanas que se pueden usar en cualquier parte del sistema, como los controles, deben procesar este mensaje. Probablemente merece la pena para otras ventanas procesar este mensaje también porque es relativamente fácil de implementar.

La función [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) requiere que la ventana que se está animando implemente el mensaje de **\_ PRINTCLIENT de WM** .

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

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**pintura de WM \_**](wm-paint.md)
</dt> </dl>

 

 
