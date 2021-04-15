---
title: Mensaje de WM_MOUSEWHEEL (Winuser. h)
description: Se envía a la ventana de foco cuando se gira la rueda del mouse.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEWHEEL
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695899"
---
# <a name="wm_mousewheel-message"></a>Mensaje de WM \_ MOUSEWHEEL

Se envía a la ventana de foco cuando se gira la rueda del mouse. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga el mensaje al elemento primario de la ventana. No debe haber un reenvío interno del mensaje, ya que **DefWindowProc** lo propaga hacia arriba en la cadena primaria hasta que encuentra una ventana que la procesa.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden superior indica la distancia a la que gira la rueda, expresada en múltiplos o divisiones de la **\_ diferencia** de la rueda, que es 120. Un valor positivo indica que la rueda se giró hacia delante, alejándose del usuario; un valor negativo indica que la rueda se giró hacia atrás, hacia el usuario.

La palabra de orden inferior indica si varias claves virtuales están inactivas. Este parámetro puede ser uno o varios de los valores siguientes.



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

La palabra de orden inferior especifica la coordenada x del puntero, relativa a la esquina superior izquierda de la pantalla.

La palabra de orden superior especifica la coordenada y del puntero, con respecto a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Use el código siguiente para obtener la información del parámetro *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores). Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto. También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.

> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

La rotación de la rueda será un múltiplo de la **\_ diferencia** de la rueda, que se establece en 120. Este es el umbral de acción que se va a realizar y una acción de este tipo (por ejemplo, desplazarse un incremento) debe producirse para cada diferencia.

El delta se estableció en 120 para que Microsoft u otros proveedores puedan crear ruedas de resolución más precisa (una rueda de rotación gratuita sin muescas) para enviar más mensajes por rotación, pero con un valor menor en cada mensaje. Para usar esta característica, puede Agregar los valores Delta entrantes hasta que se alcance la **\_ diferencia** de la rueda (por lo que para una rotación Delta obtiene la misma respuesta) o desplazarse por las líneas parciales en respuesta a los mensajes con más frecuencia. También puede elegir la granularidad de desplazamiento y acumular las diferencias hasta que se alcance.

Tenga en cuenta que no hay *fwKeys* para **MSH \_ MOUSEWHEEL**. De lo contrario, los parámetros son exactamente iguales que para **WM \_ MOUSEWHEEL**.

Depende de la aplicación reenviar **MSH \_ MOUSEWHEEL** a cualquier objeto o control incrustado. La aplicación es necesaria para enviar el mensaje a una aplicación OLE integrada activa. Es opcional que la aplicación la envíe a un control habilitado para rueda con el foco. Si la aplicación envía el mensaje a un control, puede comprobar el valor devuelto para ver si se procesó el mensaje. Los controles son necesarios para devolver el valor **true** si procesan el mensaje.

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

[**OBTENER \_ KEYSTATE \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GET \_ wheel \_ Delta \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**evento del mouse \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**CIMA**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

