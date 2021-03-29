---
title: Operaciones de mouse misceláneas
description: En las secciones anteriores se han explicado los clics del mouse y el movimiento del mouse. A continuación se indican algunas operaciones que se pueden realizar con el mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358951"
---
# <a name="miscellaneous-mouse-operations"></a>Operaciones de mouse misceláneas

En las secciones anteriores se han explicado los clics del mouse y el movimiento del mouse. A continuación se indican algunas operaciones que se pueden realizar con el mouse.

## <a name="dragging-ui-elements"></a>Arrastrar elementos de la interfaz de usuario

Si la interfaz de usuario admite arrastrar elementos de la interfaz de usuario, hay otra función a la que se debe llamar en el controlador de mensajes de mouse: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect). La función **DragDetect** devuelve **true** si el usuario inicia un gesto del mouse que debe interpretarse como un arrastre. En el código siguiente se muestra cómo usar esta función.


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



Esta es la idea: cuando un programa admite arrastrar y colocar, no desea que todos los clics del mouse se interpreten como un arrastre. De lo contrario, es posible que el usuario arrastre accidentalmente algo cuando simplemente destinaría hacer clic en él (por ejemplo, para seleccionarlo). Pero si un mouse es especialmente sensible, puede ser difícil mantener el mouse perfectamente al hacer clic. Por lo tanto, Windows define un umbral de arrastre de unos pocos píxeles. Cuando el usuario presiona el botón del mouse, no se considera un arrastre a menos que el mouse cruce este umbral. La función [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) comprueba si se alcanza este umbral. Si la función devuelve **true**, puede interpretar el clic del mouse como un arrastre. En caso contrario, no.

> [!Note]  
> Si [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) devuelve **false**, Windows suprime el mensaje de [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) cuando el usuario suelta el botón del mouse. Por lo tanto, no llame a **DragDetect** a menos que el programa esté actualmente en un modo que admita arrastrar. (Por ejemplo, si ya se ha seleccionado un elemento de la interfaz de usuario arrastrable). Al final de este módulo, veremos un ejemplo de código más largo en el que se usa la función **DragDetect** .

 

## <a name="confining-the-cursor"></a>Restringir el cursor

En ocasiones, es posible que desee restringir el cursor al área cliente o a una parte del área cliente. La función [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) restringe el movimiento del cursor a un rectángulo especificado. Este rectángulo se proporciona en coordenadas de pantalla, en lugar de coordenadas de cliente, por lo que el punto (0,0) significa la esquina superior izquierda de la pantalla. Para convertir las coordenadas de cliente en coordenadas de pantalla, llame a la función [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).

El siguiente código refina el cursor en el área cliente de la ventana.


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) toma una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) , pero [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) toma una estructura [**Point**](/previous-versions//dd162805(v=vs.85)) . Un rectángulo se define por sus puntos superior izquierdo e inferior derecho. Puede limitar el cursor a cualquier área rectangular, incluidas las áreas fuera de la ventana, pero restringir el cursor al área cliente es una forma habitual de usar la función. Restringir el cursor a una región totalmente fuera de la ventana sería inusual y los usuarios probablemente lo percibirían como un error.

Para quitar la restricción, llame a [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con el valor **null**.


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>Eventos de seguimiento del mouse: mantener el mouse y salir

Otros dos mensajes del mouse están deshabilitados de forma predeterminada, pero pueden ser útiles para algunas aplicaciones:

-   [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): el cursor se ha desplazado sobre el área de cliente durante un período de tiempo fijo.
-   [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): el cursor ha dejado el área cliente.

Para habilitar estos mensajes, llame a la función [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



La estructura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene los parámetros de la función. El miembro **dwFlags** de la estructura contiene marcas de bits que especifican los mensajes de seguimiento que le interesan. Puede optar por obtener [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) y [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), como se muestra aquí, o solo uno de los dos. El miembro **dwHoverTime** especifica cuánto tiempo debe desplazarse el mouse antes de que el sistema genere un mensaje de desplazamiento. Este valor se expresa en milisegundos. El **\_ valor predeterminado de mantener el puntero** constante significa usar el valor predeterminado del sistema.

Después de obtener uno de los mensajes solicitados, se restablece la función [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) . Debe llamarlo de nuevo para obtener otro mensaje de seguimiento. Sin embargo, debe esperar hasta el siguiente mensaje de movimiento del mouse antes de volver a llamar a **TrackMouseEvent** . De lo contrario, es posible que la ventana esté desbordada por mensajes de seguimiento. Por ejemplo, si se mantiene el mouse, el sistema continuará generando un flujo de mensajes [**\_ MOUSEHOVER de WM**](/windows/desktop/inputdev/wm-mousehover) mientras el mouse sea estacionario. En realidad, no desea otro mensaje de **\_ MOUSEHOVER de WM** hasta que el mouse se desplace a otro lugar y mantenga el puntero de nuevo.

Esta es una pequeña clase auxiliar que puede usar para administrar los eventos de seguimiento del mouse.


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



En el ejemplo siguiente se muestra cómo utilizar esta clase en el procedimiento de ventana.


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



Los eventos de seguimiento del mouse requieren un procesamiento adicional por parte del sistema, por lo que debe dejarlos deshabilitados si no los necesita.

Por integridad, esta es una función que consulta el sistema para el tiempo de espera predeterminado de mantener el mouse.


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

La función siguiente comprueba si hay una rueda del mouse.


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



Si el usuario gira la rueda del mouse, la ventana que tiene el foco recibe un mensaje de [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) . El parámetro *wParam* de este mensaje contiene un valor entero denominado *Delta* que mide hasta qué punto se ha girado la rueda. La diferencia usa unidades arbitrarias, donde se definen 120 unidades como la rotación necesaria para realizar una "acción". Por supuesto, la definición de una acción depende del programa. Por ejemplo, si se usa la rueda del mouse para desplazar el texto, cada 120 unidades de giro se desplazarían una línea de texto.

El signo de la diferencia indica la dirección de la rotación:

-   Positivo: girar hacia delante, fuera del usuario.
-   Negativo: gira hacia atrás, hacia el usuario.

El valor del delta se coloca en *wParam* junto con algunas marcas adicionales. Use la macro [**Get \_ wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) para obtener el valor de la diferencia.


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Si la rueda del mouse tiene una resolución alta, el valor absoluto de la diferencia puede ser menor que 120. En ese caso, si tiene sentido que la acción se produzca en incrementos más pequeños, puede hacerlo. Por ejemplo, el texto podría desplazarse por incrementos de menos de una línea. De lo contrario, acumule la diferencia total hasta que la rueda gire lo suficiente para realizar la acción. Almacene el Delta sin usar en una variable y, cuando se acumulen 120 unidades (positivo o negativo), realice la acción.

## <a name="next"></a>Siguientes

[Entrada de teclado](keyboard-input.md)

 

 