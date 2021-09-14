---
title: WM_NCLBUTTONDBLCLK mensaje (Winuser.h)
description: Se publica cuando el usuario hace doble clic en el botón izquierdo del mouse mientras el cursor está dentro del área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- WM_NCLBUTTONDBLCLK entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360727"
---
# <a name="wm_nclbuttondblclk-message"></a>Mensaje \_ de WM NCLBUTTONDBLCLK

Se publica cuando el usuario hace doble clic en el botón izquierdo del mouse mientras el cursor está dentro del área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de prueba de acceso devuelto por la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado del procesamiento del [**mensaje WM \_ NCHITTEST.**](wm-nchittest.md) Para obtener una lista de valores de prueba de acceso, vea **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**POINTS**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor. Las coordenadas son relativas a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

También puede usar las macros [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y- de *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y- de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** e **HIWORD** tratan las coordenadas como cantidades sin signo.

 

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para averiguar la ubicación del cursor y realiza la acción adecuada. Si procede, **DefWindowProc** envía el [**mensaje \_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.

Una ventana no necesita tener el estilo **\_ DBLCLKS** de CS para recibir mensajes **WM \_ NCLBUTTONDBLCLK.**

El sistema genera un mensaje **\_ WM NCLBUTTONDBLCLK** cuando el usuario presiona, suelta y vuelve a presionar el botón izquierdo del mouse dentro del límite de tiempo de doble clic del sistema. Al hacer doble clic en el botón izquierdo del mouse, se generan cuatro mensajes: [**WM \_ NCLBUTTONDOWN,**](wm-nclbuttondown.md) [**WM \_ NCLBUTTONUP,**](wm-nclbuttonup.md) **WM \_ NCLBUTTONDBLCLK** y **WM \_ NCLBUTTONUP** de nuevo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md)
</dt> <dt>

[**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md)
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

[**PUNTOS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

