---
description: Use las funciones BeginPaint y EndPaint para preparar y completar el dibujo en el área cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Dibujo en el área cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832025"
---
# <a name="drawing-in-the-client-area"></a>Dibujo en el área cliente

Use las [**funciones BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para preparar y completar el dibujo en el área cliente. **BeginPaint** devuelve un identificador al contexto del dispositivo de presentación que se usa para dibujar en el área cliente; **EndPaint** finaliza la solicitud de pintura y libera el contexto del dispositivo.

En el ejemplo siguiente, el procedimiento de ventana escribe el mensaje "Hello, Windows!" en el área cliente. Para asegurarse de que la cadena está visible cuando se crea la ventana por primera vez, la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) llama a [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) inmediatamente después de crear y mostrar la ventana. Esto hace que [**un mensaje \_ WM PAINT**](wm-paint.md) se envíe inmediatamente al procedimiento de ventana.


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
