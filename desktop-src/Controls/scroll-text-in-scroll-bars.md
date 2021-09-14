---
title: Cómo desplazar texto
description: En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir que un usuario desplácese por el texto.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167038"
---
# <a name="how-to-scroll-text"></a>Cómo desplazar texto

En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir que un usuario desplácese por el texto. El ejemplo de esta sección crea y muestra una matriz de cadenas de texto y procesa mensajes de barra de desplazamiento de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) para que el usuario pueda desplazar texto vertical y horizontalmente.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones

### <a name="processing-the-wm_create-message"></a>Procesamiento del mensaje CREATE de WM \_

Normalmente, las unidades de desplazamiento se establecen al procesar el [**\_ mensaje WM CREATE.**](/windows/desktop/winmsg/wm-create) Es conveniente basar las unidades de desplazamiento en las dimensiones de la fuente asociadas al contexto de dispositivo (DC) de la ventana. Para recuperar las dimensiones de fuente de un controlador de dominio específico, use la [**función GetTextMetrics.**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics)

En el ejemplo de esta sección, una unidad de desplazamiento vertical es equivalente al alto de una celda de caracteres, más el inicial externo. Una unidad de desplazamiento horizontal es equivalente al ancho medio de una celda de caracteres. Por lo tanto, las posiciones de desplazamiento horizontal no corresponden a los caracteres reales, a menos que la fuente de la pantalla sea de ancho fijo.

### <a name="processing-the-wm_size-message"></a>Procesamiento del mensaje \_ WM SIZE

Al procesar el [**mensaje WM \_ SIZE,**](/windows/desktop/winmsg/wm-size) es conveniente ajustar el intervalo de desplazamiento y la posición de desplazamiento para reflejar las dimensiones del área de cliente, así como el número de líneas de texto que se mostrarán.

La [**función SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) establece los valores de posición mínima y máxima, el tamaño de página y la posición de desplazamiento de una barra de desplazamiento.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Procesamiento de los mensajes \_ WM HSCROLL y WM \_ VSCROLL

La barra de desplazamiento envía [**mensajes WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) al procedimiento de ventana cada vez que el usuario hace clic en la barra de desplazamiento o arrastra el cuadro de desplazamiento. Las palabras de orden bajo de **WM \_ VSCROLL** y **WM \_ HSCROLL** contienen cada una un código de solicitud que indica la dirección y magnitud de la acción de desplazamiento.

Cuando se [**procesan los mensajes WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL,**](wm-vscroll.md) se examina el código de solicitud de la barra de desplazamiento y se calcula el incremento de desplazamiento. Después de aplicar el incremento a la posición de desplazamiento actual, la ventana se desplaza a la nueva posición mediante la función [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) y la posición del cuadro de desplazamiento se ajusta mediante la [**función SetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)

Una vez que se desplaza una ventana, parte de su área de cliente no es válida. Para asegurarse de que se actualiza la región no válida, se usa [**la función UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) para generar un [**mensaje WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)

### <a name="processing-the-wm_paint-message"></a>Procesamiento del mensaje \_ WM PAINT

Al procesar el [**mensaje \_ WM PAINT,**](/windows/desktop/gdi/wm-paint) es conveniente dibujar las líneas de texto que desea que aparezcan en la parte no válida de la ventana. En el ejemplo siguiente se usa la posición de desplazamiento actual y las dimensiones de la región no válida para determinar el intervalo de líneas dentro de la región no válida para mostrarlas.

## <a name="example-of-scrolling-text"></a>Ejemplo de desplazamiento de texto

El ejemplo siguiente es un procedimiento de ventana para una ventana que muestra texto en su área cliente. En el ejemplo se muestra cómo desplazar el texto en respuesta a la entrada de las barras de desplazamiento horizontal y vertical.


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
TEXTMETRIC tm; 
SCROLLINFO si; 
 
// These variables are required to display text. 
static int xClient;     // width of client area 
static int yClient;     // height of client area 
static int xClientMax;  // maximum width of client area 
 
static int xChar;       // horizontal scrolling unit 
static int yChar;       // vertical scrolling unit 
static int xUpper;      // average width of uppercase letters 
 
static int xPos;        // current horizontal scrolling position 
static int yPos;        // current vertical scrolling position 
 
int i;                  // loop counter 
int x, y;               // horizontal and vertical coordinates
 
int FirstLine;          // first line in the invalidated area 
int LastLine;           // last line in the invalidated area 
HRESULT hr;
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar barras de desplazamiento](using-scroll-bars.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 