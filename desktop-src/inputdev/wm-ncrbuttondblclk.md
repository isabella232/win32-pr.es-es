---
title: Mensaje de WM_NCRBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic con el botón secundario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCRBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534714"
---
# <a name="wm_ncrbuttondblclk-message"></a>Mensaje de NCRBUTTONDBLCLK de WM \_

Se envía cuando el usuario hace doble clic con el botón secundario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) . Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor. Las coordenadas son relativas a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

No es necesario que una ventana tenga el estilo **CS \_ DBLCLKS** para recibir mensajes de **WM \_ NCRBUTTONDBLCLK** .

El sistema genera un mensaje de **WM \_ NCRBUTTONDBLCLK** cuando el usuario presiona, suelta y presiona el botón secundario del mouse en el límite de tiempo de doble clic del sistema. Al hacer doble clic con el botón secundario del mouse, se generan cuatro mensajes: [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** y **WM \_ NCRBUTTONUP** de nuevo.

También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

Si es adecuado hacerlo, el sistema envía el mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana.

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

[**NCRBUTTONDOWN de WM \_**](wm-ncrbuttondown.md)
</dt> <dt>

[**NCRBUTTONUP de WM \_**](wm-ncrbuttonup.md)
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

 

