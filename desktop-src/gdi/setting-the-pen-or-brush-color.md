---
description: En el ejemplo siguiente se muestra cómo una aplicación puede cambiar el color del lápiz del controlador de dominio mediante la función GetStockObject o las funciones SetDCPenColor y SetDCBrushColor.
ms.assetid: d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc
title: Establecer el color del lápiz o del pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 087d4ca2bcd19457c66dddb8471c9ee2cda99294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985926"
---
# <a name="setting-the-pen-or-brush-color"></a><span data-ttu-id="11519-103">Establecer el color del lápiz o del pincel</span><span class="sxs-lookup"><span data-stu-id="11519-103">Setting the Pen or Brush Color</span></span>

<span data-ttu-id="11519-104">En el ejemplo siguiente se muestra cómo una aplicación puede cambiar el color del lápiz del controlador de dominio mediante la función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) o las funciones [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) y [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) .</span><span class="sxs-lookup"><span data-stu-id="11519-104">The following example shows how an application can change the DC pen color by using the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function or [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) and the [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) functions.</span></span>


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
        
        {    
            hdc = BeginPaint(hWnd, &ps);
        //    Initializing original object
            HGDIOBJ original = NULL;
        
        //    Saving the original object
            original = SelectObject(hdc,GetStockObject(DC_PEN));

        //    Rectangle function is defined as...
        //    BOOL Rectangle(hdc, xLeft, yTop, yRight, yBottom);
    
        //    Drawing a rectangle with just a black pen
        //    The black pen object is selected and sent to the current device context
        //  The default brush is WHITE_BRUSH
            SelectObject(hdc, GetStockObject(BLACK_PEN));
            Rectangle(hdc,0,0,200,200);

        //    Select DC_PEN so you can change the color of the pen with
        //    COLORREF SetDCPenColor(HDC hdc, COLORREF color)
            SelectObject(hdc, GetStockObject(DC_PEN));

        //    Select DC_BRUSH so you can change the brush color from the 
        //    default WHITE_BRUSH to any other color
            SelectObject(hdc, GetStockObject(DC_BRUSH));

        //    Set the DC Brush to Red
        //    The RGB macro is declared in "Windowsx.h"
            SetDCBrushColor(hdc, RGB(255,0,0));

        //    Set the Pen to Blue
            SetDCPenColor(hdc, RGB(0,0,255));
        
        //    Drawing a rectangle with the current Device Context    
            Rectangle(hdc,100,300,200,400);

        //    Changing the color of the brush to Green
            SetDCBrushColor(hdc, RGB(0,255,0));
            Rectangle(hdc,300,150,500,300);

        //    Restoring the original object
            SelectObject(hdc,original);

        // It is not necessary to call DeleteObject to delete stock objects.
        }
        
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



