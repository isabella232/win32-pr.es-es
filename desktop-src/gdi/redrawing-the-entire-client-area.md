---
description: Puede hacer que la aplicación vuelva a dibujar todo el contenido del área de cliente cada vez que la ventana cambie de tamaño estableciendo los estilos \_ HREDRAW y CS DRAW de CS para la clase \_ de ventana.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Volver a dibujar todo el área de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759151"
---
# <a name="redrawing-the-entire-client-area"></a>Volver a dibujar todo el área de cliente

Puede hacer que la aplicación vuelva a dibujar todo el contenido del área de cliente cada vez que la ventana cambie de tamaño estableciendo los estilos \_ HREDRAW y CS DRAW de CS para la clase \_ de ventana. Las aplicaciones que ajustan el tamaño del dibujo en función del tamaño de la ventana usan estos estilos para asegurarse de que comienzan con un área de cliente completamente vacía al dibujar.

En el ejemplo siguiente, el procedimiento de ventana dibuja una estrella de cinco puntas que encaja perfectamente en el área cliente. Usa un contexto de dispositivo común y debe establecer el modo de asignación, así como las extensiones de ventana y ventanilla cada vez que se procesa el mensaje [**\_ WM PAINT.**](wm-paint.md)


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



 

 



