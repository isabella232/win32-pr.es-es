---
description: Este tema tiene un ejemplo de código que muestra cómo registrar una ventana local y usarla para crear una ventana principal.
ms.assetid: ea9e36c9-b10d-441e-b1b5-1ab93e009e1d
title: Usar clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d23f49e431aa6f980d16fc7a9df5c4f98951498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262236"
---
# <a name="using-window-classes"></a>Usar clases de ventana

Este tema tiene un ejemplo de código que muestra cómo registrar una ventana local y usarla para crear una ventana principal.

Cada proceso debe registrar sus propias clases de ventana. Para registrar una clase local de aplicación, use [**la función RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Debe definir el procedimiento de ventana, rellenar los miembros de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) y, a continuación, pasar un puntero a la estructura a la **función RegisterClassEx.**

En el ejemplo siguiente se muestra cómo registrar una clase de ventana local y usarla para crear una ventana principal.


```
#include <windows.h> 
 
// Global variable 
 
HINSTANCE hinst; 
 
// Function prototypes. 
 
int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int); 
InitApplication(HINSTANCE); 
InitInstance(HINSTANCE, int); 
LRESULT CALLBACK MainWndProc(HWND, UINT, WPARAM, LPARAM); 
 
// Application entry point. 
 
int WINAPI WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, 
    LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg; 
 
    if (!InitApplication(hinstance)) 
        return FALSE; 
 
    if (!InitInstance(hinstance, nCmdShow)) 
        return FALSE; 
 
    BOOL fGotMessage;
    while ((fGotMessage = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0 && fGotMessage != -1) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(lpCmdLine); 
} 
 
BOOL InitApplication(HINSTANCE hinstance) 
{ 
    WNDCLASSEX wcx; 
 
    // Fill in the window class structure with parameters 
    // that describe the main window. 
 
    wcx.cbSize = sizeof(wcx);          // size of structure 
    wcx.style = CS_HREDRAW | 
        CS_VREDRAW;                    // redraw if size changes 
    wcx.lpfnWndProc = MainWndProc;     // points to window procedure 
    wcx.cbClsExtra = 0;                // no extra class memory 
    wcx.cbWndExtra = 0;                // no extra window memory 
    wcx.hInstance = hinstance;         // handle to instance 
    wcx.hIcon = LoadIcon(NULL, 
        IDI_APPLICATION);              // predefined app. icon 
    wcx.hCursor = LoadCursor(NULL, 
        IDC_ARROW);                    // predefined arrow 
    wcx.hbrBackground = GetStockObject( 
        WHITE_BRUSH);                  // white background brush 
    wcx.lpszMenuName =  "MainMenu";    // name of menu resource 
    wcx.lpszClassName = "MainWClass";  // name of window class 
    wcx.hIconSm = LoadImage(hinstance, // small class icon 
        MAKEINTRESOURCE(5),
        IMAGE_ICON, 
        GetSystemMetrics(SM_CXSMICON), 
        GetSystemMetrics(SM_CYSMICON), 
        LR_DEFAULTCOLOR); 
 
    // Register the window class. 
 
    return RegisterClassEx(&wcx); 
} 
 
BOOL InitInstance(HINSTANCE hinstance, int nCmdShow) 
{ 
    HWND hwnd; 
 
    // Save the application-instance handle. 
 
    hinst = hinstance; 
 
    // Create the main window. 
 
    hwnd = CreateWindow( 
        "MainWClass",        // name of window class 
        "Sample",            // title-bar string 
        WS_OVERLAPPEDWINDOW, // top-level window 
        CW_USEDEFAULT,       // default horizontal position 
        CW_USEDEFAULT,       // default vertical position 
        CW_USEDEFAULT,       // default width 
        CW_USEDEFAULT,       // default height 
        (HWND) NULL,         // no owner window 
        (HMENU) NULL,        // use class menu 
        hinstance,           // handle to application instance 
        (LPVOID) NULL);      // no window-creation data 
 
    if (!hwnd) 
        return FALSE; 
 
    // Show the window and send a WM_PAINT message to the window 
    // procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
    return TRUE; 
 
} 
```



El registro de una clase global de aplicación es similar  al registro de una clase local de aplicación, salvo que el miembro de estilo de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) debe especificar el estilo **\_ GLOBALCLASS de CS.**

 

 
