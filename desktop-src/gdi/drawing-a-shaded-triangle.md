---
description: Para dibujar un triángulo sombreado, defina una estructura TRIVERTEX con tres elementos y una sola estructura GRADIENT \_ TRIANGLE.
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: Dibujar un triángulo sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b6742f8ff6a3e2d543592e86cac87489048ca4d9748dc4e111cd4613b2f207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062415"
---
# <a name="drawing-a-shaded-triangle"></a>Dibujar un triángulo sombreado

Para dibujar un triángulo sombreado, defina una [**estructura TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) con tres elementos y una sola [**estructura GRADIENT \_ TRIANGLE.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) En el ejemplo de código siguiente se muestra cómo dibujar un triángulo sombreado mediante la [**función GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) con el modo GRADIENT \_ FILL TRIANGLE \_ definido.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        {hdc = BeginPaint(hWnd, &ps);
// Create an array of TRIVERTEX structures that describe
// positional and color values for each vertex.
TRIVERTEX vertex[3];
vertex[0].x     = 150;
vertex[0].y     = 0;
vertex[0].Red   = 0xff00;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x0000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 0;
vertex[1].y     = 150;
vertex[1].Red   = 0x9000;
vertex[1].Green = 0x0000;
vertex[1].Blue  = 0x9000;
vertex[1].Alpha = 0x0000;

vertex[2].x     = 300;
vertex[2].y     = 150; 
vertex[2].Red   = 0x9000;
vertex[2].Green = 0x0000;
vertex[2].Blue  = 0x9000;
vertex[2].Alpha = 0x0000;

// Create a GRADIENT_TRIANGLE structure that
// references the TRIVERTEX vertices.
GRADIENT_TRIANGLE gTriangle;
gTriangle.Vertex1 = 0;
gTriangle.Vertex2 = 1;
gTriangle.Vertex3 = 2;

// Draw a shaded triangle.
GradientFill(hdc, vertex, 3, &gTriangle, 1, GRADIENT_FILL_TRIANGLE);
        EndPaint(hWnd, &ps);
        break;}
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



En la imagen siguiente se muestra la salida de dibujo del ejemplo de código anterior.

![ilustración en la que se muestra un triángulo que se rellena de color naranja en el punto superior al triángulo en el borde inferior](images/gradientfilltriangle.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre mapas de bits](bitmaps.md)
</dt> <dt>

[Funciones de mapa de bits](bitmap-functions.md)
</dt> <dt>

[Dibujar un rectángulo sombreado](drawing-a-shaded-rectangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**TRIÁNGULO DE \_ DEGRADADO**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



