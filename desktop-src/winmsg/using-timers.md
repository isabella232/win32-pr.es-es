---
description: En este tema se muestra cómo crear y destruir temporizadores y cómo usar un temporizador para capturar la entrada del mouse a intervalos especificados.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Uso de temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028313"
---
# <a name="using-timers"></a>Uso de temporizadores

En este tema se muestra cómo crear y destruir temporizadores y cómo usar un temporizador para capturar la entrada del mouse a intervalos especificados.

En este tema se incluyen las siguientes secciones.

-   [Crear un temporizador](#creating-a-timer)
-   [Destruir un temporizador](#destroying-a-timer)
-   [Uso de funciones de temporizador para capturar la entrada del mouse](#using-timer-functions-to-trap-mouse-input)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-timer"></a>Crear un temporizador

En el ejemplo siguiente se usa [**la función SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) para crear dos temporizadores. El primer temporizador se establece para cada 10 segundos y el segundo para cada cinco minutos.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Para procesar los [**mensajes WM \_ TIMER**](wm-timer.md) generados por estos temporizadores, agregue una instrucción de caso **\_ DE TEMPORIZADOR DE WM** al procedimiento de ventana para el parámetro *hwnd.*


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Una aplicación también puede crear un temporizador cuyos mensajes [**WM \_ TIMER**](wm-timer.md) no se procesan mediante el procedimiento de ventana principal, sino por una función de devolución de llamada definida por la aplicación, como en el ejemplo de código siguiente, que crea un temporizador y usa la función de devolución de llamada **MyTimerProc para** procesar los mensajes **WM \_ TIMER** del temporizador.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



La convención de llamada para **MyTimerProc** debe basarse en la función de devolución de llamada [*TimerProc.*](/windows/win32/api/winuser/nc-winuser-timerproc)

Si la aplicación crea un temporizador sin especificar un identificador de ventana, la aplicación debe supervisar la cola de mensajes para los mensajes [**WM \_ TIMER**](wm-timer.md) y enviarlos a la ventana adecuada.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Destruir un temporizador

Las aplicaciones deben usar [**la función KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) para destruir temporizadores que ya no son necesarios. En el ejemplo siguiente se destruyen los temporizadores identificados por las constantes IDT \_ TIMER1, IDT \_ TIMER2 y IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Uso de funciones de temporizador para capturar la entrada del mouse

A veces es necesario evitar más entradas mientras se tiene un puntero del mouse en la pantalla. Una manera de lograrlo es crear una rutina especial que captura la entrada del mouse hasta que se produce un evento específico. Muchos desarrolladores hacen referencia a esta rutina como "creación de una ratón".

En el ejemplo siguiente se usan [**las funciones SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) y [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) para capturar la entrada del mouse. **SetTimer crea** un temporizador que envía un mensaje [**WM \_ TIMER**](wm-timer.md) cada 10 segundos. Cada vez que la aplicación recibe un **mensaje \_ WM TIMER,** registra la ubicación del puntero del mouse. Si la ubicación actual es la misma que la ubicación anterior y se minimiza la ventana principal de la aplicación, la aplicación mueve el puntero del mouse al icono. Cuando se cierra la aplicación, **KillTimer** detiene el temporizador.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Aunque en el ejemplo siguiente también se muestra cómo capturar la entrada del mouse, procesa el mensaje [**\_ WM TIMER**](wm-timer.md) a través de la función de devolución de llamada **MyTimerProc** definida por la aplicación, en lugar de a través de la cola de mensajes de la aplicación.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los temporizadores](about-timers.md)
</dt> </dl>

 

 
