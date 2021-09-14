---
title: WM_XBUTTONDOWN mensaje (Winuser.h)
description: Se publica cuando el usuario presiona el primer o segundo botón X mientras el cursor está en el área cliente de una ventana.
ms.assetid: 4d972841-1513-4925-9d59-2557233561a2
keywords:
- WM_XBUTTONDOWN entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_XBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976a5f3d7282853b5267b0b1640a7a95120efbef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241551"
---
# <a name="wm_xbuttondown-message"></a>Mensaje \_ XBUTTONDOWN de WM

Se publica cuando el usuario presiona el primer o segundo botón X mientras el cursor está en el área cliente de una ventana. Si no se captura el mouse, el mensaje se publica en la ventana debajo del cursor. De lo contrario, el mensaje se publica en la ventana que ha capturado el mouse.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_XBUTTONDOWN                  0x020B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo indica si varias claves virtuales están abajo. Puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Control**</dt> <dt>0x0008</dt> </dl>    | La tecla CTRL está presionada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | El botón izquierdo del mouse está apagado.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | El botón central del mouse está apagado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | El botón derecho del mouse está apagado.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ Mayús**</dt> <dt>0x0004</dt> </dl>          | La tecla MAYÚS está abajo.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | El primer botón X está apagado.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | El segundo botón X está apagado.<br/>     |



 

La palabra de orden superior indica qué botón se hizo clic. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                     | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | Se hizo clic en el primer botón X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Se hizo clic en el segundo botón X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica la coordenada x del cursor. La coordenada es relativa a la esquina superior izquierda del área cliente.

La palabra de orden superior especifica la coordenada y del cursor. La coordenada es relativa a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**. Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Use el código siguiente para obtener la información en el *parámetro wParam:*


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam);
```



Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Como se indicó anteriormente, la coordenada x está en el orden bajo **corto** del valor devuelto; la coordenada y está en el  orden corto de orden superior **(ambos** representan valores con signo porque pueden tomar valores negativos en sistemas con varios monitores). Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**POINTS**](/previous-versions//dd162808(v=vs.85)) del valor devuelto. También puede usar la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.

> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y- de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

A diferencia de los mensajes [**WM \_ LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)y [**WM \_ RBUTTONDOWN,**](wm-rbuttondown.md) una aplicación debe devolver **TRUE** a partir de este mensaje si lo procesa. Esto permite que el software que simula este mensaje en sistemas de Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ XBUTTON \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTOS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

