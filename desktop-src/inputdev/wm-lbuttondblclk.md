---
title: Mensaje de WM_LBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra en el área cliente de una ventana.
ms.assetid: 370aa19e-4939-4ac3-9c0b-137a9792e52a
keywords:
- Entrada de mouse y teclado de mensaje de WM_LBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_LBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd91eef026ae027e183b4f304211915e7bbbd95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695906"
---
# <a name="wm_lbuttondblclk-message"></a>Mensaje de LBUTTONDBLCLK de WM \_

Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra en el área cliente de una ventana. Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor. De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_LBUTTONDBLCLK                0x0203
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si varias claves virtuales están inactivas. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de control </dl>    | La tecla CTRL está presionada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | El botón primario del mouse está inactivo.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | El botón central del mouse está presionado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | El botón secundario del mouse está inactivo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | La tecla Mayús está presionada.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | El primer botón X está inactivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | El segundo botón X está inactivo.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la coordenada x del cursor. La coordenada es relativa a la esquina superior izquierda del área cliente.

La palabra de orden superior especifica la coordenada y del cursor. La coordenada es relativa a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores). Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto. También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.

> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

Solo las ventanas que tienen el estilo **CS \_ DBLCLKS** pueden recibir mensajes de **WM \_ LBUTTONDBLCLK** , que el sistema genera cada vez que el usuario presiona, suelta y presiona el botón primario del mouse dentro del límite de tiempo de doble clic del sistema. Al hacer doble clic en el botón primario del mouse, se genera una secuencia de cuatro mensajes: [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), [**WM \_ LBUTTONUP**](wm-lbuttonup.md), **WM \_ LBUTTONDBLCLK** y **WM \_ LBUTTONUP**.

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

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**LBUTTONDOWN de WM \_**](wm-lbuttondown.md)
</dt> <dt>

[**LBUTTONUP de WM \_**](wm-lbuttonup.md)
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

 

