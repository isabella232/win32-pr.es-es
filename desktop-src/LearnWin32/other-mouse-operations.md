---
title: Varias operaciones del mouse
description: En las secciones anteriores se han analizado los clics del mouse y el movimiento del mouse. Estas son algunas otras operaciones que se pueden realizar con el mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159951"
---
# <a name="miscellaneous-mouse-operations"></a>Varias operaciones del mouse

En las secciones anteriores se han analizado los clics del mouse y el movimiento del mouse. Estas son algunas otras operaciones que se pueden realizar con el mouse.

## <a name="dragging-ui-elements"></a>Arrastrar elementos de la interfaz de usuario

Si la interfaz de usuario admite el arrastre de elementos de la interfaz de usuario, hay otra función a la que debe llamar en el controlador de mensajes del mouse: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). La **función DragDetect** devuelve **TRUE si** el usuario inicia un gesto del mouse que se debe interpretar como arrastre. En el código siguiente se muestra cómo usar esta función.


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



Esta es la idea: cuando un programa admite arrastrar y colocar, no quiere que cada clic del mouse se interprete como un arrastre. De lo contrario, el usuario podría arrastrar accidentalmente algo cuando simplemente quería hacer clic en él (por ejemplo, para seleccionarlo). Pero si un mouse es especialmente sensible, puede ser difícil mantener el mouse perfectamente inquiete al hacer clic. Por lo tanto, Windows define un umbral de arrastre de unos pocos píxeles. Cuando el usuario presiona el botón del mouse, no se considera un arrastre a menos que el mouse cruce este umbral. La [**función DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) comprueba si se alcanza este umbral. Si la función devuelve **TRUE**, puede interpretar el clic del mouse como un arrastre. De lo contrario, no lo haga.

> [!Note]  
> Si [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) devuelve **FALSE,** Windows el mensaje [**\_ LBUTTONUP de WM**](/windows/desktop/inputdev/wm-lbuttonup) cuando el usuario suelta el botón del mouse. Por lo tanto, no llame a **DragDetect** a menos que el programa esté actualmente en un modo que admita arrastrar. (Por ejemplo, si ya se ha seleccionado un elemento de interfaz de usuario arrastrable). Al final de este módulo, veremos un ejemplo de código más largo que usa la **función DragDetect.**

 

## <a name="confining-the-cursor"></a>Confining the Cursor

En ocasiones, es posible que quiera restringir el cursor al área de cliente o a una parte del área de cliente. La [**función ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe el movimiento del cursor a un rectángulo especificado. Este rectángulo se indica en coordenadas de pantalla, en lugar de coordenadas de cliente, por lo que el punto (0, 0) significa la esquina superior izquierda de la pantalla. Para convertir coordenadas de cliente en coordenadas de pantalla, llame a la [**función ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

El código siguiente limita el cursor al área cliente de la ventana.


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



[**ClipCursor toma**](/windows/desktop/api/winuser/nf-winuser-clipcursor) una [**estructura RECT,**](/previous-versions//dd162897(v=vs.85)) pero [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) toma una [**estructura POINT.**](/previous-versions//dd162805(v=vs.85)) Un rectángulo se define mediante sus puntos superior izquierdo e inferior derecho. Puede limitar el cursor a cualquier área rectangular, incluidas las áreas fuera de la ventana, pero la conexión del cursor al área de cliente es una manera habitual de usar la función. La conexión del cursor a una región completamente fuera de la ventana sería inusual y los usuarios probablemente lo perciben como un error.

Para quitar la restricción, llame [**a ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con el valor **NULL**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventos de seguimiento del mouse: mantener el mouse y salir

Otros dos mensajes del mouse están deshabilitados de forma predeterminada, pero pueden ser útiles para algunas aplicaciones:

-   [**WM \_ MOUSEHOVER:**](/windows/desktop/inputdev/wm-mousehover)el cursor ha sobresalido sobre el área de cliente durante un período de tiempo fijo.
-   [**WM \_ MOUSELEAVE:**](/windows/desktop/inputdev/wm-mouseleave)el cursor ha dejado el área de cliente.

Para habilitar estos mensajes, llame a [**la función TrackMouseEvent.**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent)


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



La [**estructura TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene los parámetros de la función. El **miembro dwFlags** de la estructura contiene marcas de bits que especifican los mensajes de seguimiento que le interesan. Puede optar por obtener [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) y [**WM \_ MOUSELEAVE,**](/windows/desktop/inputdev/wm-mouseleave)como se muestra aquí, o simplemente uno de los dos. El **miembro dwHoverTime** especifica cuánto tiempo debe mantener el mouse sobre el mouse antes de que el sistema genere un mensaje de mantener el puntero. Este valor se da en milisegundos. La constante **HOVER \_ DEFAULT significa** usar el valor predeterminado del sistema.

Después de obtener uno de los mensajes que solicitó, se restablece la función [**TrackMouseEvent.**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) Debe llamarlo de nuevo para obtener otro mensaje de seguimiento. Sin embargo, debe esperar hasta el siguiente mensaje de movimiento del mouse antes de volver **a llamar a TrackMouseEvent.** De lo contrario, la ventana podría desbordarse con mensajes de seguimiento. Por ejemplo, si el mouse mantiene el puntero, el sistema seguiría generando una secuencia de [**mensajes \_ MOUSEHOVER de WM**](/windows/desktop/inputdev/wm-mousehover) mientras el mouse está estacionado. En realidad, no desea otro mensaje **\_ WM MOUSEHOVER** hasta que el mouse se mueve a otro lugar y se mantiene el puntero de nuevo.

Esta es una pequeña clase auxiliar que puede usar para administrar eventos de seguimiento del mouse.


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



En el ejemplo siguiente se muestra cómo usar esta clase en el procedimiento de ventana.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



Los eventos de seguimiento del mouse requieren un procesamiento adicional por parte del sistema, así que déjelos deshabilitados si no los necesita.

Para que sea completa, esta es una función que consulta el sistema para el tiempo de espera predeterminado del puntero.


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a>Rueda del mouse

La siguiente función comprueba si hay una rueda del mouse.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Si el usuario gira la rueda del mouse, la ventana con el foco recibe un [**mensaje WM \_ MOUSEWHEEL.**](/windows/desktop/inputdev/wm-mousewheel) El *parámetro wParam* de este mensaje contiene un valor entero denominado *delta* que mide hasta qué punto se ha girado la rueda. La diferencia usa unidades arbitrarias, donde 120 unidades se definen como la rotación necesaria para realizar una "acción". Por supuesto, la definición de una acción depende del programa. Por ejemplo, si se usa la rueda del mouse para desplazar el texto, cada 120 unidades de rotación se desplazaría por una línea de texto.

El signo de la diferencia indica la dirección de rotación:

-   Positivo: gira hacia delante, lejos del usuario.
-   Negativo: gira hacia atrás, hacia el usuario.

El valor de delta se coloca en *wParam* junto con algunas marcas adicionales. Use la [**macro GET WHEEL DELTA \_ \_ \_ WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obtener el valor de la diferencia.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Si la rueda del mouse tiene una resolución alta, el valor absoluto del delta podría ser menor que 120. En ese caso, si tiene sentido que la acción se produzca en incrementos más pequeños, puede hacerlo. Por ejemplo, el texto podría desplazarse por incrementos de menos de una línea. De lo contrario, acumule el delta total hasta que la rueda gire lo suficiente como para realizar la acción. Almacene la diferencia sin usar en una variable y, cuando se acumulen 120 unidades (positivas o negativas), realice la acción.

## <a name="next"></a>Siguientes

[Entrada de teclado](keyboard-input.md)

 

 