---
title: WM_POINTERUPDATE mensaje
description: Se publica para proporcionar una actualización en un puntero que hizo contacto sobre el área cliente de una ventana o en un puntero no capturado al mantener el puntero sobre el área cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- WM_POINTERUPDATE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 40c1decbf3c209a381356c58c901c4cab992fadd28eb9566e55e46b1cf87e3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829515"
---
# <a name="wm_pointerupdate-message"></a>WM_POINTERUPDATE mensaje

Se publica para proporcionar una actualización en un puntero que hizo contacto sobre el área cliente de una ventana o en un puntero no capturado al mantener el puntero sobre el área cliente de una ventana. Mientras el puntero mantiene el puntero, el mensaje tiene como destino la ventana sobre la que se encuentra el puntero. Mientras el puntero está en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero hizo contacto y esa ventana continúa recibiendo la entrada del puntero hasta que se interrumpe el contacto.

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no es compatible con PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no son compatibles con PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene información sobre el puntero. Use las macros siguientes para recuperar información del parámetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador del puntero.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si un puntero generó este mensaje durante su vigencia. Esta marca no se establece en los mensajes que indican que el puntero tiene un intervalo de detección izquierdo
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje lo generó un puntero que está en contacto con la superficie de la ventana. Esta marca no se establece en los mensajes que indican un puntero que mantiene el puntero.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.
    -   Esto es análogo a un botón izquierdo del mouse hacia abajo.
    -   Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.
    -   Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin botones presionados.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.
    -   Esto es análogo a un botón derecho del mouse hacia abajo.
    -   Un puntero de lápiz tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de botones del lápiz presionado.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; Las aplicaciones que deseen responder a acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan. Por ejemplo, una aplicación puede determinar los estados de los botones de un lápiz llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado realizó la cuarta acción. Las aplicaciones que deseen responder a la cuarta acción deben recuperar información específica del tipo de puntero para determinar si se presiona el primer botón extendido del mouse (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado realizó la quinta acción. Las aplicaciones que deseen responder a la quinta acción deben recuperar información específica del tipo de puntero para determinar si se presiona el segundo botón extendido del mouse (XButton2).

    Vea [**Marcas de puntero para**](pointer-flags-contants.md) obtener más detalles.

    > [!Note]  
    > Un puntero que mantiene el puntero no tiene establecida ninguna de las marcas de botón. Esto es análogo a un movimiento del mouse sin botones del mouse hacia abajo. Una aplicación puede determinar los estados de los botones de un lápiz, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los estados de los botones.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación de punto del puntero.

> [!Note]  
> Dado que el puntero puede hacer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información completa del área de puntero en lugar de la ubicación de punto.

 

Use las macros siguientes para recuperar las coordenadas de pantalla física del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada x (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordenada y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentarios

Cada puntero tiene un identificador de puntero único durante su vigencia. La duración de un puntero comienza cuando se detecta por primera vez.

Se [**WM_POINTERENTER**](wm-pointerenter.md) mensaje de confirmación si se detecta un puntero que mantiene el puntero. Si [**se detecta un puntero**](wm-pointerdown.md) que no mantiene el **puntero, se WM_POINTERDOWN** un mensaje de WM_POINTERENTER seguido de un mensaje de confirmación.

Durante su vigencia, un puntero puede generar una serie de mensajes **WM_POINTERUPDATE** mientras mantiene el puntero o está en contacto.

La duración de un puntero finaliza cuando ya no se detecta. Esto genera un [**mensaje WM_POINTERLEAVE**](wm-pointerleave.md) mensaje.

Cuando se anula un puntero, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) se establece.

También [**WM_POINTERLEAVE**](wm-pointerleave.md) mensaje de error cuando un puntero no capturado se mueve fuera de los límites de una ventana.

Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



La [**macro MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) también se puede usar para convertir el parámetro lParam en una [**estructura POINTS.**](/previous-versions//dd162808(v=vs.85))

La [**función GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) se puede usar para determinar los estados de tecla modificadora de teclado asociados a este mensaje. Por ejemplo, para detectar que se ha presionado la tecla ALT, compruebe si **GetKeyState** (VK_MENU) &lt; 0.

Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto. Si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.

Si una aplicación consume selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.

Use la [**función GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar más información relacionada con este mensaje.

Si la aplicación no procesa estos mensajes tan rápido como se generan, es posible que algunos movimientos se acomenten. El historial de entradas que se han convertido en este mensaje se puede recuperar mediante la función [**GetPointerInfoHistory.**](/previous-versions/windows/desktop/api)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)y [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) para recuperar información pertinente de los parámetros wParam y lParam **del WM_POINTERUPDATE** mensaje.


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with right button down
}
```



En el ejemplo de código siguiente se muestra [**cómo GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar el identificador de puntero del parámetro wParam **del WM_POINTERUPDATE** mensaje.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



En el ejemplo de código siguiente se muestra cómo controlar distintos tipos de puntero.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_INPUT_TYPE pointerType = PT_POINTER;

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
        fHandled = HandleGenericPointerInfo(&pointerInfo);
    }
    break;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

