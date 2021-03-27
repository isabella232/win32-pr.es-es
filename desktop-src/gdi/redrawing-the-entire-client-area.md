---
description: Puede hacer que la aplicación vuelva a dibujar todo el contenido del área cliente cada vez que cambie el tamaño de la ventana mediante el establecimiento de los \_ estilos CS HREDRAW y CS \_ VREDRAW para la clase Window.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Volver a dibujar todo el área cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67640d1b464173755029bef1d0feb91f215cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997305"
---
# <a name="redrawing-the-entire-client-area"></a>Volver a dibujar todo el área cliente

Puede hacer que la aplicación vuelva a dibujar todo el contenido del área cliente cada vez que cambie el tamaño de la ventana mediante el establecimiento de los \_ estilos CS HREDRAW y CS \_ VREDRAW para la clase Window. Las aplicaciones que ajustan el tamaño del dibujo en función del tamaño de la ventana usan estos estilos para asegurarse de que se inician con un área cliente completamente vacía al dibujar.

En el ejemplo siguiente, el procedimiento de ventana dibuja una estrella de cinco puntas que encaja perfectamente en el área de cliente. Utiliza un contexto de dispositivo común y debe establecer el modo de asignación, así como las extensiones de ventana y ventanilla, cada vez que se procesa el mensaje de [**\_ pintura de WM**](wm-paint.md) .


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



