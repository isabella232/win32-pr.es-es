---
title: Mensaje WM_POINTERUP
description: Se publica cuando un puntero que hizo contacto sobre el área de cliente de una ventana interrumpe el contacto.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5bf811501d189abef127e2b191e159518654650bf569cd2abdad42d7471eb1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756803"
---
# <a name="wm_pointerup-message"></a>Mensaje WM_POINTERUP

Se publica cuando un puntero que hizo contacto sobre el área de cliente de una ventana interrumpe el contacto. Este mensaje de entrada tiene como destino la ventana sobre la que el puntero realiza contacto y el puntero se captura implícitamente en la ventana para que la ventana siga recibiendo mensajes de entrada, incluida la notificación WM_POINTERUP del puntero **hasta** que se interrumpe el contacto.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene información sobre el puntero. Use las macros siguientes para recuperar información del parámetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador del puntero.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si un puntero generó este mensaje durante su vigencia. Esta marca no se establece en los mensajes que indican que el puntero tiene un intervalo de detección izquierdo.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje lo generó un puntero que está en contacto con la superficie de la ventana. Esta marca no se establece en los mensajes que indican un puntero que mantiene el puntero.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.
    -   Esto es análogo a un botón izquierdo del mouse hacia abajo.
    -   Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.
    -   Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin botones presionados.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.
    -   Esto es análogo a un botón derecho del mouse hacia abajo.
    -   Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de lápiz presionado.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): una marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; Las aplicaciones que desean responder a acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan. Por ejemplo, una aplicación puede determinar los estados de los botones de un lápiz llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado realizó la cuarta acción. Las aplicaciones que deseen responder a cuartas acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el primer botón extendido del mouse (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado realizó la quinta acción. Las aplicaciones que deseen responder a la quinta acción deben recuperar información específica del tipo de puntero para determinar si se presiona el segundo botón extendido del mouse (XButton2).

    Consulte [**Marcas de puntero para**](pointer-flags-contants.md) obtener más detalles.

    > [!Note]  
    > Un puntero que mantiene el puntero no tiene establecida ninguna de las marcas de botón. Esto es análogo a un movimiento del mouse sin botones del mouse hacia abajo. Una aplicación puede determinar los estados de botones de un lápiz que mantiene el puntero, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación de punto del puntero.

> [!Note]  
> Dado que el puntero puede hacer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información completa del área de puntero en lugar de la ubicación del punto.

 

Use las macros siguientes para recuperar las coordenadas de pantalla física del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada x (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordenada y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentarios

> \[! Importante\]  
> Cuando una ventana pierde la captura de [](wm-pointercapturechanged.md) un puntero y recibe la notificación WM_POINTERCAPTURECHANGED, normalmente no recibirá ninguna notificación adicional. Por esta razón, es importante que no realice ninguna [](wm-pointerdown.md)suposición basada en notificaciones de WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER /  [](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) emparejadas uniformemente.

 

Cada puntero tiene un identificador de puntero único durante su duración. La duración de un puntero comienza cuando se detecta por primera vez.

Se [**WM_POINTERENTER**](wm-pointerenter.md) mensaje de confirmación si se detecta un puntero que mantiene el puntero. Si [**se detecta WM_POINTERDOWN**](wm-pointerdown.md) puntero que no mantiene el puntero, se **genera** un mensaje de WM_POINTERENTER seguido de un mensaje de confirmación.

Durante su vigencia, un puntero puede generar una serie de mensajes [**WM_POINTERUPDATE**](wm-pointerupdate.md) mientras mantiene el puntero o está en contacto.

La duración de un puntero finaliza cuando ya no se detecta. Esto genera un mensaje [**WM_POINTERLEAVE**](wm-pointerleave.md) mensaje.

Cuando se anula un puntero, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) se establece.

También [**WM_POINTERLEAVE**](wm-pointerleave.md) mensaje de error cuando un puntero no capturado se mueve fuera de los límites de una ventana.

Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:

Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



La [**macro MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) también se puede usar para convertir el parámetro lParam en una [**estructura POINTS.**](/previous-versions//dd162808(v=vs.85))

La [**función GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) se puede usar para determinar los estados de tecla modificadora de teclado asociados a este mensaje. Por ejemplo, para detectar que se presionó la tecla ALT, compruebe si **GetKeyState**(VK_MENU) &lt; 0.

Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md)si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto. Si no se reconoce un gesto, **DefWindowProc puede** generar la entrada del mouse.

Si una aplicación consume selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.

Use la [**función GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar más información relacionada con este mensaje.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recuperar la posición x e y del puntero asociado a este mensaje.


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



En el ejemplo de código siguiente se muestra cómo obtener el identificador de puntero asociado a este mensaje.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



En el ejemplo de código siguiente se muestra cómo controlar los distintos tipos de puntero asociados a este mensaje.


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**Marcas de puntero**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>
