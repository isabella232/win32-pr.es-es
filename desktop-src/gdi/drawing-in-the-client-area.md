---
description: Las funciones BeginPaint y EndPaint se usan para preparar y completar el dibujo en el área cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Dibujo en el área cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908492"
---
# <a name="drawing-in-the-client-area"></a>Dibujo en el área cliente

Las funciones [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) se usan para preparar y completar el dibujo en el área cliente. **BeginPaint** devuelve un identificador para el contexto de dispositivo de pantalla que se usa para dibujar en el área de cliente. **EndPaint** finaliza la solicitud de Paint y libera el contexto del dispositivo.

En el ejemplo siguiente, el procedimiento de ventana escribe el mensaje "Hello, Windows!" en el área cliente. Para asegurarse de que la cadena está visible cuando se crea la ventana por primera vez, la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) llama a [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) inmediatamente después de crear y mostrar la ventana. Esto hace que se envíe un mensaje de [**\_ dibujo de WM**](wm-paint.md) inmediatamente al procedimiento de ventana.


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



 

 
