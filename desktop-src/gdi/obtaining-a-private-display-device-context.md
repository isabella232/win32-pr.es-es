---
description: Una aplicación que realiza numerosas operaciones de dibujo en el área cliente de su ventana debe usar un controlador de dominio de visualización privado.
ms.assetid: 9c4ed127-a88f-4946-9d7c-f77899152c31
title: Obtener un contexto de dispositivo de pantalla privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed679ecadd694cd8781d0de8b4409fde15d22b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811923"
---
# <a name="obtaining-a-private-display-device-context"></a><span data-ttu-id="0c5ef-103">Obtener un contexto de dispositivo de pantalla privado</span><span class="sxs-lookup"><span data-stu-id="0c5ef-103">Obtaining a Private Display Device Context</span></span>

<span data-ttu-id="0c5ef-104">Una aplicación que realiza numerosas operaciones de dibujo en el área cliente de su ventana debe usar un controlador de dominio de visualización privado.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-104">An application performing numerous drawing operations in the client area of its window must use a private display DC.</span></span> <span data-ttu-id="0c5ef-105">Para crear este tipo de controlador de dominio, la aplicación debe especificar la constante **\_ OWNDC de CS** para el miembro de estilo de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-105">To create this type of DC, the application must specify the **CS\_OWNDC** constant for the style member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when registering the window class.</span></span> <span data-ttu-id="0c5ef-106">Después de registrar la clase de ventana, la aplicación obtiene un identificador que identifica un controlador de dominio de visualización privado mediante una llamada a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="0c5ef-106">After registering the window class, the application obtains a handle identifying a private display DC by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="0c5ef-107">En el ejemplo siguiente se muestra cómo crear un controlador de dominio de visualización privado.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-107">The following example shows how to create a private display DC.</span></span>


```C++
#include <windows.h>    // required for all Windows-based applications  
#include <stdio.h>      // C run-time header for i/o 
#include <string.h>     // C run-time header for strtok_s  
#include "dc.h"         // specific to this program  
 
// Function prototypes. 
 
BOOL InitApplication(HINSTANCE); 
long FAR PASCAL MainWndProc(HWND, UINT, UINT, LONG); 
 
// Global variables  
 
HINSTANCE hinst;       // handle to current instance  
HDC hdc;               // display device context handle  
 
BOOL InitApplication(HINSTANCE hinstance) 
{ 
    WNDCLASS  wc; 
 
    // Fill in the window class structure with parameters  
    // describing the main window.  
 
    wc.style = CS_OWNDC;         // Private-DC constant  
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
 
    wc.hIcon = LoadIcon((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDI_APPLICATION)); 
 
    wc.hCursor = LoadCursor((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDC_ARROW)); 
 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "GenericMenu"; 
    wc.lpszClassName = "GenericWClass"; 
 
    // Register the window class and return the resulting code.  
 
    return RegisterClass(&wc); 
} 
 
LRESULT APIENTRY MainWndProc( 
        HWND hwnd,           // window handle  
        UINT message,        // type of message  
        WPARAM wParam,       // additional information  
        LPARAM lParam)       // additional information  
{ 
 
    PAINTSTRUCT ps;              // paint structure  
 
    // Retrieve a handle identifying the private DC.  
 
    hdc = GetDC(hwnd); 
 
    switch (message) 
    { 
        case WM_PAINT: 
              hdc = BeginPaint(hwnd, &ps); 
 
        // Draw and paint using private DC. 
        
                 EndPaint(hwnd, &ps);
              
        case WM_DESTROY:
                     PostQuitMessage(0);
                     break;
        default:
                return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 
