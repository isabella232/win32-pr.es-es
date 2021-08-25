---
title: WM_MOUSEWHEEL mensaje (Winuser.h)
description: Se envía a la ventana de enfoque cuando se gira la rueda del mouse.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL entrada de teclado y mouse
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
ms.openlocfilehash: ae3e750a8544c050e735671b7fd2df6980d53b1200e2f67493b46ad7a2e0b017
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888735"
---
# <a name="wm_mousewheel-message"></a>Mensaje \_ WM MOUSEWHEEL

Se envía a la ventana de enfoque cuando se gira la rueda del mouse. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga el mensaje al elemento primario de la ventana. No debería haber ningún reenvío interno del mensaje, ya que **DefWindowProc** lo propaga hacia arriba en la cadena primaria hasta que encuentra una ventana que lo procesa.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden superior indica la distancia a la que gira la rueda, expresada en múltiplos o divisiones de **WHEEL \_ DELTA,** que es 120. Un valor positivo indica que la rueda se ha girado hacia delante, lejos del usuario. Un valor negativo indica que la rueda se ha girado hacia atrás, hacia el usuario.

La palabra de orden bajo indica si varias claves virtuales están abajo. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Control**</dt> <dt>0x0008</dt> </dl>    | La tecla CTRL está presionada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | El botón izquierdo del mouse está apagado.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | El botón central del mouse está apagado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | El botón derecho del mouse está apagado.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ Mayús**</dt> <dt>0x0004</dt> </dl>          | La tecla MAYÚS está abajo.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | El primer botón X está apagado.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | El segundo botón X está apagado.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la coordenada x del puntero, en relación con la esquina superior izquierda de la pantalla.

La palabra de orden superior especifica la coordenada y del puntero, en relación con la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Use el código siguiente para obtener la información en el *parámetro wParam:*


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Como se indicó anteriormente, la coordenada x está en el orden bajo **corto** del valor devuelto; la coordenada y está en el  orden corto de orden superior **(ambos** representan valores con signo porque pueden tomar valores negativos en sistemas con varios monitores). Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**POINTS**](/previous-versions//dd162808(v=vs.85)) del valor devuelto. También puede usar la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.

> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

La rotación de la rueda será un **múltiplo de WHEEL \_ DELTA,** que se establece en 120. Este es el umbral para la acción que se va a realizar y debe producirse una acción de este tipo (por ejemplo, desplazarse un incremento) para cada delta.

La diferencia se estableció en 120 para permitir que Microsoft u otros proveedores crearan ruedas de resolución más fina (una rueda de rotación libre sin notchas) para enviar más mensajes por rotación, pero con un valor más pequeño en cada mensaje. Para usar esta característica, puede agregar los valores delta entrantes hasta que se alcance **WHEEL \_ DELTA** (por lo que para una rotación diferencial obtiene la misma respuesta) o desplazar líneas parciales en respuesta a los mensajes más frecuentes. También puede elegir la granularidad de desplazamiento y acumular deltas hasta que se alcance.

Tenga en cuenta que no hay *fwKeys para* **MSH \_ MOUSEWHEEL**. De lo contrario, los parámetros son exactamente iguales que para **WM \_ MOUSEWHEEL**.

Es la aplicación la que reenvía **MSH \_ MOUSEWHEEL** a cualquier control o objeto incrustado. La aplicación es necesaria para enviar el mensaje a una aplicación OLE insertadas activa. Es opcional que la aplicación la envíe a un control habilitado para rueda con el foco. Si la aplicación envía el mensaje a un control, puede comprobar el valor devuelto para ver si se procesó el mensaje. Los controles deben devolver un valor **true** si procesan el mensaje.

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

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GET \_ WHEEL \_ DELTA \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**evento \_ mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Puntos**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

