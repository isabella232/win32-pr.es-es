---
title: Mensaje WM_POINTERUPDATE
description: Se publica para proporcionar una actualización en un puntero que se puso en contacto con el área de cliente de una ventana o en un puntero no capturado al mantener el mouse sobre el área cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERUPDATE
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
ms.openlocfilehash: 215874f4dc1b3438ae3d69b22758ced09a050f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151163"
---
# <a name="wm_pointerupdate-message"></a>Mensaje WM_POINTERUPDATE

Se publica para proporcionar una actualización en un puntero que se puso en contacto con el área de cliente de una ventana o en un puntero no capturado al mantener el mouse sobre el área cliente de una ventana. Mientras se mantiene el puntero, el mensaje se dirige a la ventana en la que se encuentra el puntero. Mientras el puntero se encuentra en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero se pone en contacto y la ventana continúa recibiendo entradas para el puntero hasta que interrumpe el contacto.

> \[! Aún\]  
> Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene información sobre el puntero. Use las siguientes macros para recuperar información del parámetro wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): el identificador de puntero.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero durante su duración. Esta marca no se establece en mensajes que indican que el puntero tiene el intervalo de detección izquierdo
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero que está en contacto con la superficie de la ventana. Esta marca no se establece en los mensajes que indican un puntero de desplazamiento.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.
    -   Es análogo a un botón primario del mouse hacia abajo.
    -   Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.
    -   Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin presionar ningún botón.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.
    -   Es análogo a un botón secundario del mouse hacia abajo.
    -   Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; las aplicaciones que desean responder a las acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan. Por ejemplo, una aplicación puede determinar los Estados de los botones de un lápiz mediante una llamada a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y el examen de las marcas que especifican los Estados de los botones.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado tardó la cuarta acción. Las aplicaciones que deseen responder a las cuarta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón del primer Mouse extendido (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado tardó la quinta acción. Las aplicaciones que deseen responder a las Quinta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón secundario del mouse (XButton2).

    Consulte [**marcadores de puntero**](pointer-flags-contants.md) para obtener más detalles.

    > [!Note]  
    > Un puntero que mantiene el mouse no tiene ninguna de las marcas de botón establecidas. Esto es análogo a un movimiento del mouse sin presionar los botones del mouse. Una aplicación puede determinar los Estados de los botones de un lápiz que mantiene el mouse, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los Estados de los botones.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la ubicación del punto del puntero.

> [!Note]  
> Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja. Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.

 

Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Cada puntero tiene un identificador de puntero único durante su duración. La duración de un puntero comienza cuando se detecta por primera vez.

Si se detecta un puntero de desplazamiento, se genera un mensaje de [**WM_POINTERENTER**](wm-pointerenter.md) . Se genera un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) seguido de un mensaje de **WM_POINTERENTER** si se detecta un puntero que no tiene el desplazamiento.

Durante su duración, un puntero puede generar una serie de mensajes de **WM_POINTERUPDATE** mientras se mantiene el mouse o el contacto.

La duración de un puntero finaliza cuando ya no se detecta. Esto genera un mensaje de [**WM_POINTERLEAVE**](wm-pointerleave.md) .

Cuando se anula un puntero, se establece [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .

También se puede generar un mensaje [**WM_POINTERLEAVE**](wm-pointerleave.md) cuando un puntero no capturado se mueve fuera de los límites de una ventana.

Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



La macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) también se puede usar para convertir el parámetro lParam en una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) .

La función [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) se puede usar para determinar los Estados de tecla modificador de teclado asociados a este mensaje. Por ejemplo, para detectar que se presionó la tecla ALT, compruebe si **GetKeyState** (VK_MENU) &lt; 0.

Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto. Si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.

Si una aplicación usa selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.

Utilice la función [**GetPointerInfo**](/previous-versions/windows/desktop/api) para recuperar más información relacionada con este mensaje.

Si la aplicación no procesa estos mensajes tan rápido como se generan, se pueden fusionar algunos movimientos. El historial de entradas que se fusionaron en este mensaje se puede recuperar mediante la función [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) .

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)y [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) para recuperar información relevante de los parámetros wParam e lParam del mensaje **WM_POINTERUPDATE** .


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



En el ejemplo de código siguiente se muestra cómo usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar el identificador de puntero del parámetro wParam del mensaje de **WM_POINTERUPDATE** .


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



En el ejemplo de código siguiente se muestra cómo administrar distintos tipos de puntero.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

