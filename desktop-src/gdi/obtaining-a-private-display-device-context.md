---
description: Una aplicación que realiza numerosas operaciones de dibujo en el área cliente de su ventana debe usar un controlador de dominio de pantalla privado.
ms.assetid: 9c4ed127-a88f-4946-9d7c-f77899152c31
title: Obtención de un contexto de dispositivo de presentación privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab21ced9c9c3beb1c4133d78271d24389b40f144156c60b1085679e922256ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469155"
---
# <a name="obtaining-a-private-display-device-context"></a>Obtención de un contexto de dispositivo de presentación privado

Una aplicación que realiza numerosas operaciones de dibujo en el área cliente de su ventana debe usar un controlador de dominio de pantalla privado. Para crear este tipo de controlador de dominio, la aplicación debe especificar la constante **\_ OWNDC** de CS para el miembro de estilo de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase window. Después de registrar la clase window, la aplicación obtiene un identificador que identifica un controlador de dominio de pantalla privado mediante una llamada a la [**función GetDC.**](/windows/desktop/api/Winuser/nf-winuser-getdc)

En el ejemplo siguiente se muestra cómo crear un controlador de dominio de pantalla privado.


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



 

 
