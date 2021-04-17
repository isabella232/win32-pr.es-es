---
title: Mensaje de WM_NCXBUTTONDOWN (Winuser. h)
description: Se envía cuando el usuario presiona el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCXBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd615b1e30e013f23097cdc7a8ca7c22c338684a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714585"
---
# <a name="wm_ncxbuttondown-message"></a>Mensaje de NCXBUTTONDOWN de WM \_

Se envía cuando el usuario presiona el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje *no* se publica.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior especifica el valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) . Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**. La palabra de orden superior indica el botón que se presionó. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                     | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | Se presionó el primer botón X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Se presionó el segundo botón X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor. Las coordenadas son relativas a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true**. Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Use el código siguiente para obtener la información del parámetro *wParam* .


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



También puede usar el código siguiente para obtener las coordenadas x e y de *lParam*:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para obtener la posición del cursor y realiza la acción adecuada. Si es necesario, envía el mensaje de [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.

A diferencia de los mensajes [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)y [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md) , una aplicación debe devolver **true** desde este mensaje si lo procesa. Esto permitirá que el software que simula este mensaje en sistemas Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir windowsx. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**NCHITTEST de WM \_**](wm-nchittest.md)
</dt> <dt>

[**NCXBUTTONDBLCLK de WM \_**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**NCXBUTTONUP de WM \_**](wm-ncxbuttonup.md)
</dt> <dt>

[**SYSCOMMAND de WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**CIMA**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

