---
description: En el ejemplo siguiente se muestra cómo una aplicación puede cambiar el color del lápiz dc mediante las funciones GetStockObject o SetDCPenColor y SetDCBrushColor.
ms.assetid: d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc
title: Establecer el lápiz o el color del pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 087d4ca2bcd19457c66dddb8471c9ee2cda99294
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072448"
---
# <a name="setting-the-pen-or-brush-color"></a>Establecer el lápiz o el color del pincel

En el ejemplo siguiente se muestra cómo una aplicación puede cambiar el color del lápiz dc mediante las funciones [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) o [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) y [**SetDCBrushColor.**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)


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



 

 



