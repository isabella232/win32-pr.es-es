---
description: En esta sección se incluye código de ejemplo que muestra cómo generar una ruta de acceso de clip que consta de una cadena de caracteres. En el ejemplo se crea una fuente lógica y se usa para dibujar una cadena dentro de un trazado de clip y, a continuación, se rellena la ruta de acceso dibujando líneas horizontales y verticales.
ms.assetid: c71727aa-f4a3-409e-b50f-709eb4dbdaab
title: Usar el recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a81181c09197fd98b5c84fd6f641ba84445000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997897"
---
# <a name="using-clipping"></a><span data-ttu-id="8058e-104">Usar el recorte</span><span class="sxs-lookup"><span data-stu-id="8058e-104">Using Clipping</span></span>

<span data-ttu-id="8058e-105">En esta sección se incluye código de ejemplo que muestra cómo generar una ruta de acceso de clip que consta de una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8058e-105">This section contains example code that shows how to generate a clip path consisting of a character string.</span></span> <span data-ttu-id="8058e-106">En el ejemplo se crea una fuente lógica y se usa para dibujar una cadena dentro de un trazado de clip y, a continuación, se rellena la ruta de acceso dibujando líneas horizontales y verticales.</span><span class="sxs-lookup"><span data-stu-id="8058e-106">The example creates a logical font and uses it to draw a string within a clip path, then fills the path by drawing horizontal and vertical lines.</span></span>


```C++
// DoClipPat - Draws a clip path using the specified string  
// Return value - TRUE if successful; FALSE otherwise  
// lplf - address of a LOGFONT structure that defines the font to  
//        use to draw the clip path  
// lpsz - address of a string to use for the clip path  
 
BOOL DoClipPath(LPLOGFONT lplf, LPSTR lpsz) 
{ 
    LOGFONT lf;           // logical font structure  
    HFONT hfont;          // new logical font handle  
    HFONT hfontOld;       // original logical font handle  
    HDC hdc;              // display DC handle  
    int nXStart, nYStart; // drawing coordinates  
    RECT rc;              // rectangle structure for painting window  
    SIZE sz;              // size structure that receives text extents  
    int nStrLen;          // length of the string  
    int i;                // loop counter  
        HRESULT hr;
        size_t * pcch;
 
    // Retrieve a cached DC for the window.  
 
    hdc = GetDC(hwnd); 
 
    // Erase the current window contents.  
 
    GetClientRect(hwnd, &rc); 
    FillRect(hdc, &rc, GetStockObject(WHITE_BRUSH)); 
 
    // Use the specified font to create a logical font and select it  
    // into the DC.  
 
    hfont = CreateFontIndirect(lplf); 
    if (hfont == NULL) 
        return FALSE; 
    hfontOld = SelectObject(hdc, hfont); 
 
    // Create a clip path.  
 
        hr = StringCchLength(lpsz, STRSAFE_MAX_CCH, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
        nStrLen = *pcch 
    BeginPath(hdc); 
        TextOut(hdc, nXStart, nYStart, lpsz, nStrLen); 
    EndPath(hdc); 
    SelectClipPath(hdc, RGN_DIFF); 
 
    // Retrieve the dimensions of the rectangle surrounding  
    // the text.  
 
    GetTextExtentPoint32(hdc, lpsz, nStrLen, &sz); 
 
    // Draw horizontal lines through the clip path.  
 
    for (i = nYStart + 1; i < (nYStart + sz.cy); i += 3) 
    { 
       MoveToEx(hdc, nXStart, i, (LPPOINT) NULL); 
       LineTo(hdc, (nXStart + sz.cx), i); 
    } 
 
    // Draw vertical lines through the clip path.  
 
    for (i = nXStart + 1; i < (nXStart + sz.cx); i += 3)
    { 
       MoveToEx(hdc, i, nYStart, (LPPOINT) NULL); 
       LineTo(hdc, i, (nYStart + sz.cy)); 
    } 
 
    // Select the original font into the DC and release the DC.  
 
    SelectObject(hdc, hfontOld); 
    DeleteObject(hfont); 
    ReleaseDC(hwnd, hdc); 
 
    return TRUE; 
} 
```



<span data-ttu-id="8058e-107">Para ver un ejemplo que muestra cómo una aplicación crea una región de recorte rectangular, consulte [regiones](regions.md).</span><span class="sxs-lookup"><span data-stu-id="8058e-107">For an example that demonstrates how an application creates a rectangular clipping region, see [Regions](regions.md).</span></span>

 

 



