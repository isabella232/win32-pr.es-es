---
description: Para dibujar un triángulo sombreado, defina una estructura de trivértices con tres elementos y una única estructura de triángulo de DEGRADAdo \_ .
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: Dibujo de un triángulo sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3200a1ec061d7513cbac56c8c66104154005cef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155637"
---
# <a name="drawing-a-shaded-triangle"></a>Dibujo de un triángulo sombreado

Para dibujar un triángulo sombreado, defina una estructura de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) con tres elementos y una única estructura de [**\_ triángulo de degradado**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) . En el ejemplo de código siguiente se muestra cómo dibujar un triángulo sombreado mediante la función [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) con el modo triángulo de relleno de degradado \_ \_ definido.


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



En la imagen siguiente se muestra el resultado del dibujo del ejemplo de código anterior.

![Ilustración en la que se muestra un triángulo que se rellena desde el naranja en el punto superior hasta el magenta en el borde inferior](images/gradientfilltriangle.png)

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

[**triángulo de DEGRADAdo \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**Trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



