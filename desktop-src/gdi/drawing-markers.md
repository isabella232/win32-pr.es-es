---
description: Puede usar las funciones de línea para dibujar marcadores.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Marcadores de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811972"
---
# <a name="drawing-markers"></a><span data-ttu-id="4a892-103">Marcadores de dibujo</span><span class="sxs-lookup"><span data-stu-id="4a892-103">Drawing Markers</span></span>

<span data-ttu-id="4a892-104">Puede usar las funciones de línea para dibujar marcadores.</span><span class="sxs-lookup"><span data-stu-id="4a892-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="4a892-105">Un marcador es un símbolo que se centra en un punto.</span><span class="sxs-lookup"><span data-stu-id="4a892-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="4a892-106">Las aplicaciones de dibujo usan marcadores para designar puntos de inicio, puntos finales y puntos de control.</span><span class="sxs-lookup"><span data-stu-id="4a892-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="4a892-107">Las aplicaciones de hojas de cálculo usan marcadores para designar puntos de interés en un gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a892-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="4a892-108">En el ejemplo de código siguiente, la función de marcador definida por la aplicación crea un marcador mediante las funciones [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) y [**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) .</span><span class="sxs-lookup"><span data-stu-id="4a892-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="4a892-109">Estas funciones dibujan dos líneas de intersección, 20 píxeles de longitud, centradas en las coordenadas del cursor.</span><span class="sxs-lookup"><span data-stu-id="4a892-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



<span data-ttu-id="4a892-110">El sistema almacena las coordenadas del cursor en el parámetro *lParam* del mensaje de [**\_ LBUTTONDOWN de WM**](../inputdev/wm-lbuttondown.md) cuando el usuario presiona el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="4a892-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="4a892-111">En el código siguiente se muestra cómo una aplicación obtiene estas coordenadas, determina si se encuentran dentro de su área cliente y las pasa a la función de marcador para dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="4a892-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
