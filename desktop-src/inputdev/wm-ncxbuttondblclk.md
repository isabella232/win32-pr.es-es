---
title: WM_NCXBUTTONDBLCLK mensaje (Winuser.h)
description: Se publica cuando el usuario hace doble clic en el primer o segundo botón X mientras el cursor está en el área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- WM_NCXBUTTONDBLCLK entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b5b0deb3efb84af2bdd862377411d86328ee7ef72242a6e27759b819cdab2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482645"
---
# <a name="wm_ncxbuttondblclk-message"></a>Mensaje \_ WM NCXBUTTONDBLCLK

Se publica cuando el usuario hace doble clic en el primer o segundo botón X mientras el cursor está en el área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica el valor de la prueba de acceso devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) al procesar el [**mensaje WM \_ NCHITTEST.**](wm-nchittest.md) Para obtener una lista de valores de prueba de acceso, vea **WM \_ NCHITTEST**.

La palabra de orden superior indica en qué botón se hizo doble clic. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                     | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | Se hizo doble clic en el primer botón X.<br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Se hizo doble clic en el segundo botón X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINTS**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor. Las coordenadas son relativas a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**. Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.

## <a name="remarks"></a>Comentarios

Use el código siguiente para obtener la información en el *parámetro wParam.*


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
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y- de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

De forma predeterminada, la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para obtener la posición del cursor y realiza la acción adecuada. Si procede, envía el mensaje [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.

Una ventana no necesita tener el estilo **\_ DBLCLKS** de CS para recibir mensajes **WM \_ NCXBUTTONDBLCLK.** El sistema genera un mensaje **\_ WM NCXBUTTONDBLCLK** cuando el usuario presiona, suelta y vuelve a presionar un botón X dentro del límite de tiempo de doble clic del sistema. Al hacer doble clic en uno de estos botones, se generan cuatro mensajes: [**WM \_ NCXBUTTONDOWN,**](wm-ncxbuttondown.md) [**WM \_ NCXBUTTONUP,**](wm-ncxbuttonup.md) **WM \_ NCXBUTTONDBLCLK** y **WM \_ NCXBUTTONUP** de nuevo.

A diferencia de los mensajes [**\_ WM NCLBUTTONDBLCLK,**](wm-nclbuttondblclk.md) [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)y [**WM \_ NCRBUTTONDBLCLK,**](wm-ncrbuttondblclk.md) una aplicación debe devolver **TRUE** desde este mensaje si lo procesa. Esto permitirá que el software que simula este mensaje en sistemas de Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Puntos**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

