---
description: Puede dibujar a intervalos de tiempo mediante la creación de un temporizador con la función SetTimer.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Dibujar a intervalos de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544502"
---
# <a name="drawing-at-timed-intervals"></a>Dibujar a intervalos de tiempo

Puede dibujar a intervalos de tiempo mediante la creación de un temporizador con la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Mediante el uso de un temporizador para enviar mensajes del [**\_ temporizador de WM**](../winmsg/wm-timer.md) al procedimiento de ventana a intervalos regulares, una aplicación puede llevar a cabo una animación simple en el área de cliente mientras otras aplicaciones continúan en ejecución.

En el ejemplo siguiente, la aplicación rebota una estrella de lado a lado en el área de cliente. Cada vez que el procedimiento de ventana recibe un mensaje [**\_ del temporizador de WM**](../winmsg/wm-timer.md) , el procedimiento borra la estrella en la posición actual, calcula una nueva posición y dibuja la estrella dentro de la nueva posición. El procedimiento inicia el temporizador llamando a [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) mientras procesa el mensaje de [**\_ creación de WM**](../winmsg/wm-create.md) .


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



Esta aplicación utiliza un contexto de dispositivo privado para minimizar el tiempo necesario para preparar el contexto de dispositivo para el dibujo. El procedimiento de ventana recupera e inicializa el contexto de dispositivo privado al procesar el mensaje de [**\_ creación de WM**](../winmsg/wm-create.md) , estableciendo el modo de operación de rasterización binaria para permitir que la estrella se borre y dibuje usando la misma llamada a la función [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) . El procedimiento de ventana también establece el origen de la ventanilla para permitir que la estrella se dibuje usando el mismo conjunto de puntos, independientemente de la posición de la estrella en el área de cliente.

La aplicación utiliza el mensaje de [**\_ dibujo de WM**](wm-paint.md) para dibujar la estrella cada vez que se debe actualizar la ventana. El procedimiento de ventana sólo dibuja la estrella si no está visible; es decir, solo si se ha borrado mediante el mensaje [**de \_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) . El procedimiento de ventana intercepta el mensaje de **\_ ERASEBKGND de WM** para establecer la variable *fVisible* , pero pasa el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que el sistema pueda dibujar el fondo de la ventana.

La aplicación utiliza el mensaje de [**\_ tamaño de WM**](../winmsg/wm-size.md) para detener el temporizador cuando la ventana está minimizada y reiniciar el temporizador cuando se restaura la ventana minimizada. El procedimiento de ventana también usa el mensaje para actualizar la posición actual de la estrella si se ha reducido el tamaño de la ventana, de modo que la estrella ya no esté en el área de cliente. La aplicación realiza un seguimiento de la posición actual de la estrella mediante la estructura especificada por rcCurrent, que define el rectángulo delimitador para la estrella. Mantener todas las esquinas del rectángulo en el área de cliente mantiene la estrella en el área. El procedimiento de ventana centra inicialmente la estrella en el área de cliente al procesar el mensaje de [**\_ creación de WM**](../winmsg/wm-create.md) .

 

 
