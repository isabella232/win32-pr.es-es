---
title: WM_NCMBUTTONDOWN mensaje (Winuser.h)
description: Se publica cuando el usuario presiona el botón central del mouse mientras el cursor está dentro del área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 0aa86fc6-43e9-4356-a4c1-e3f687dc2884
keywords:
- WM_NCMBUTTONDOWN entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0b99b530deb808337246af984b24848454cbe78ec4bbe2b09e969caa8154a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602655"
---
# <a name="wm_ncmbuttondown-message"></a>Mensaje \_ wm NCMBUTTONDOWN

Se publica cuando el usuario presiona el botón central del mouse mientras el cursor está dentro del área no cliente de una ventana. Este mensaje se publica en la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMBUTTONDOWN                0x00A7
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de la prueba de acceso devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado del procesamiento del [**mensaje WM \_ NCHITTEST.**](wm-nchittest.md) Para obtener una lista de valores de prueba de acceso, vea **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**POINTS**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor. Las coordenadas son relativas a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

También puede usar las macros [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y- de *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

Si es adecuado hacerlo, el sistema envía el mensaje [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)
</dt> <dt>

[**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)
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

 

