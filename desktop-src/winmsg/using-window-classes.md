---
description: En este tema se incluye un ejemplo de código que muestra cómo registrar una ventana local y usarla para crear una ventana principal.
ms.assetid: ea9e36c9-b10d-441e-b1b5-1ab93e009e1d
title: Usar clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d23f49e431aa6f980d16fc7a9df5c4f98951498
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667493"
---
# <a name="using-window-classes"></a><span data-ttu-id="b9b8e-103">Usar clases de ventana</span><span class="sxs-lookup"><span data-stu-id="b9b8e-103">Using Window Classes</span></span>

<span data-ttu-id="b9b8e-104">En este tema se incluye un ejemplo de código que muestra cómo registrar una ventana local y usarla para crear una ventana principal.</span><span class="sxs-lookup"><span data-stu-id="b9b8e-104">This topic has a code example that shows how to register a local window and use it to create a main window.</span></span>

<span data-ttu-id="b9b8e-105">Cada proceso debe registrar sus propias clases de ventana.</span><span class="sxs-lookup"><span data-stu-id="b9b8e-105">Each process must register its own window classes.</span></span> <span data-ttu-id="b9b8e-106">Para registrar una clase local de aplicación, use la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) .</span><span class="sxs-lookup"><span data-stu-id="b9b8e-106">To register an application local class, use the [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) function.</span></span> <span data-ttu-id="b9b8e-107">Debe definir el procedimiento de ventana, rellenar los miembros de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) y, a continuación, pasar un puntero a la estructura a la función **RegisterClassEx** .</span><span class="sxs-lookup"><span data-stu-id="b9b8e-107">You must define the window procedure, fill the members of the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure, and then pass a pointer to the structure to the **RegisterClassEx** function.</span></span>

<span data-ttu-id="b9b8e-108">En el ejemplo siguiente se muestra cómo registrar una clase de ventana local y utilizarla para crear una ventana principal.</span><span class="sxs-lookup"><span data-stu-id="b9b8e-108">The following example shows how to register a local window class and use it to create a main window.</span></span>


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



<span data-ttu-id="b9b8e-109">El registro de una clase global de aplicación es similar al registro de una clase local de la aplicación, salvo que el miembro de **estilo** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) debe especificar el estilo **CS \_ GLOBALCLASS** .</span><span class="sxs-lookup"><span data-stu-id="b9b8e-109">Registering an application global class is similar to registering an application local class, except that the **style** member of the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure must specify the **CS\_GLOBALCLASS** style.</span></span>

 

 
