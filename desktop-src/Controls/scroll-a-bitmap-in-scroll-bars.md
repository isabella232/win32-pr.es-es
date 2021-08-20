---
title: Desplazamiento de un mapa de bits
description: En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir al usuario desplazarse por un mapa de bits.
ms.assetid: FA6FEA49-25EB-4C18-AD07-74BD77501906
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d8fff259326c4eb73838f1f6e2b650aab40d54882633a76e2fbf120a1ae89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005288"
---
# <a name="how-to-scroll-a-bitmap"></a>Desplazamiento de un mapa de bits

En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir al usuario desplazarse por un mapa de bits.

El ejemplo incluye un elemento de menú que copia el contenido de la pantalla en un mapa de bits y muestra el mapa de bits en el área de cliente. El ejemplo también procesa los mensajes [**\_ WM HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) generados por las barras de desplazamiento para que el usuario pueda desplazar el mapa de bits horizontal y verticalmente. A diferencia del ejemplo de texto de desplazamiento, el ejemplo de mapa de bits emplea la [**función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para dibujar la parte no válida del área de cliente.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="processing-the-wm_create-message"></a>Procesamiento del mensaje \_ WM CREATE

Cuando se procesa el mensaje [**\_ WM CREATE,**](/windows/desktop/winmsg/wm-create) se inicializan las variables necesarias para el desplazamiento. Use la [**función CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) para crear un contexto de dispositivo (DC) compatible, la función [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para crear un mapa de bits y la función [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para seleccionar el mapa de bits del controlador de dominio. Tenga en cuenta que un controlador de dominio compatible también se conoce como controlador de dominio de memoria.

Se recupera la información específica del dispositivo sobre el dispositivo de visualización. Si se crea un controlador de dominio compatible para la pantalla, como en el ejemplo, use la [**función GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obtener esta información. La información incluye el número de bits de color adyacentes por píxel, el número de planos de color y el alto y ancho del controlador de dominio.

### <a name="processing-the-wm_size-message"></a>Procesamiento del mensaje WM \_ SIZE

El procesamiento del [**mensaje WM \_ SIZE**](/windows/desktop/winmsg/wm-size) requiere ajustar el intervalo de desplazamiento y la posición, para que refleje las dimensiones del área de cliente y el mapa de bits que se mostrarán.

La [**función SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) establece los valores de posición mínima y máxima, el tamaño de página y la posición de desplazamiento de una barra de desplazamiento.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Procesamiento de los mensajes \_ WM HSCROLL y WM \_ VSCROLL

Cuando se procesan los mensajes [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL,**](wm-vscroll.md) se examina el código de solicitud de la barra de desplazamiento y la posición de desplazamiento se establece en un nuevo valor que refleja la acción de desplazamiento del usuario. Si la posición de desplazamiento está dentro del intervalo de desplazamiento, la ventana se desplaza a la nueva posición mediante la [**función ScrollWindow.**](/windows/desktop/api/Winuser/nf-winuser-scrollwindow) A continuación, la posición del cuadro de desplazamiento se ajusta mediante la [**función SetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)

Una vez que se desplaza una ventana, parte de su área de cliente no es válida. Para asegurarse de que la región no válida se actualiza, use la [**función UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) para generar un [**mensaje WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Al procesar el **mensaje \_ WM PAINT,** una aplicación debe volver a dibujar la región no válida en la parte inferior del área de cliente. Al desplazar o cambiar el tamaño del área de cliente, en el ejemplo se usa la función [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para copiar la parte adecuada del mapa de bits en la parte no válida del área de cliente.

## <a name="example-of-scrolling-a-bitmap"></a>Ejemplo de desplazamiento de un mapa de bits

En el ejemplo siguiente se permite al usuario capturar el contenido de la pantalla en un mapa de bits y desplazar el mapa de bits en el área de cliente. El contenido de la pantalla se captura cuando el usuario hace clic con el botón derecho en el área de cliente.


```C++
LRESULT CALLBACK MyBitmapWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc; 
    PAINTSTRUCT ps; 
    SCROLLINFO si; 
 
    // These variables are required by BitBlt. 
    static HDC hdcWin;           // window DC 
    static HDC hdcScreen;        // DC for entire screen 
    static HDC hdcScreenCompat;  // memory DC for screen 
    static HBITMAP hbmpCompat;   // bitmap handle to old DC 
    static BITMAP bmp;           // bitmap data structure 
    static BOOL fBlt;            // TRUE if BitBlt occurred 
    static BOOL fScroll;         // TRUE if scrolling occurred 
    static BOOL fSize;           // TRUE if fBlt & WM_SIZE 
 
    // These variables are required for horizontal scrolling. 
    static int xMinScroll;       // minimum horizontal scroll value 
    static int xCurrentScroll;   // current horizontal scroll value 
    static int xMaxScroll;       // maximum horizontal scroll value 
 
    // These variables are required for vertical scrolling. 
    static int yMinScroll;       // minimum vertical scroll value 
    static int yCurrentScroll;   // current vertical scroll value 
    static int yMaxScroll;       // maximum vertical scroll value 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create a normal DC and a memory DC for the entire 
            // screen. The normal DC provides a snapshot of the 
            // screen contents. The memory DC keeps a copy of this 
            // snapshot in the associated bitmap. 
            hdcScreen = CreateDC(L"DISPLAY", (PCTSTR) NULL, 
                (PCTSTR) NULL, (CONST DEVMODE *) NULL); 
            hdcScreenCompat = CreateCompatibleDC(hdcScreen); 
 
            // Retrieve the metrics for the bitmap associated with the 
            // regular device context. 
            bmp.bmBitsPixel = 
                (BYTE) GetDeviceCaps(hdcScreen, BITSPIXEL); 
            bmp.bmPlanes = (BYTE) GetDeviceCaps(hdcScreen, PLANES); 
            bmp.bmWidth = GetDeviceCaps(hdcScreen, HORZRES); 
            bmp.bmHeight = GetDeviceCaps(hdcScreen, VERTRES); 
 
            // The width must be byte-aligned. 
            bmp.bmWidthBytes = ((bmp.bmWidth + 15) &~15)/8; 
 
            // Create a bitmap for the compatible DC. 
            hbmpCompat = CreateBitmap(bmp.bmWidth, bmp.bmHeight, 
                bmp.bmPlanes, bmp.bmBitsPixel, (CONST VOID *) NULL); 
 
            // Select the bitmap for the compatible DC. 
            SelectObject(hdcScreenCompat, hbmpCompat); 
 
            // Initialize the flags. 
            fBlt = FALSE; 
            fScroll = FALSE; 
            fSize = FALSE; 
 
            // Initialize the horizontal scrolling variables. 
            xMinScroll = 0; 
            xCurrentScroll = 0; 
            xMaxScroll = 0; 
 
            // Initialize the vertical scrolling variables. 
            yMinScroll = 0; 
            yCurrentScroll = 0; 
            yMaxScroll = 0; 
 
            break; 
 
        case WM_SIZE: 
        { 
            int xNewSize; 
            int yNewSize; 
 
            xNewSize = LOWORD(lParam); 
            yNewSize = HIWORD(lParam); 
 
            if (fBlt) 
                fSize = TRUE; 
     
            // The horizontal scrolling range is defined by 
            // (bitmap_width) - (client_width). The current horizontal 
            // scroll value remains within the horizontal scrolling range. 
            xMaxScroll = max(bmp.bmWidth-xNewSize, 0); 
            xCurrentScroll = min(xCurrentScroll, xMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = xMinScroll; 
            si.nMax   = bmp.bmWidth; 
            si.nPage  = xNewSize; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            // The vertical scrolling range is defined by 
            // (bitmap_height) - (client_height). The current vertical 
            // scroll value remains within the vertical scrolling range. 
            yMaxScroll = max(bmp.bmHeight - yNewSize, 0); 
            yCurrentScroll = min(yCurrentScroll, yMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = yMinScroll; 
            si.nMax   = bmp.bmHeight; 
            si.nPage  = yNewSize; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 
 
        case WM_PAINT: 
        { 
            PRECT prect; 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            // If the window has been resized and the user has 
            // captured the screen, use the following call to 
            // BitBlt to paint the window's client area. 
            if (fSize) 
            { 
                BitBlt(ps.hdc, 
                    0, 0, 
                    bmp.bmWidth, bmp.bmHeight, 
                    hdcScreenCompat, 
                    xCurrentScroll, yCurrentScroll, 
                    SRCCOPY); 
 
                fSize = FALSE; 
            } 
 
            // If scrolling has occurred, use the following call to 
            // BitBlt to paint the invalid rectangle. 
            // 
            // The coordinates of this rectangle are specified in the 
            // RECT structure to which prect points. 
            // 
            // Note that it is necessary to increment the seventh 
            // argument (prect->left) by xCurrentScroll and the 
            // eighth argument (prect->top) by yCurrentScroll in 
            // order to map the correct pixels from the source bitmap. 
             if (fScroll) 
            { 
                prect = &ps.rcPaint; 
 
                BitBlt(ps.hdc, 
                    prect->left, prect->top, 
                    (prect->right - prect->left), 
                    (prect->bottom - prect->top), 
                    hdcScreenCompat, 
                    prect->left + xCurrentScroll, 
                    prect->top + yCurrentScroll, 
                    SRCCOPY); 
 
                fScroll = FALSE; 
            } 
 
            EndPaint(hwnd, &ps); 

            break; 
        } 

        case WM_HSCROLL: 
        { 
            int xDelta;     // xDelta = new_pos - current_pos  
            int xNewPos;    // new position 
            int yDelta = 0; 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft left of the scroll box. 
                case SB_PAGEUP: 
                    xNewPos = xCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft right of the scroll box. 
                case SB_PAGEDOWN: 
                    xNewPos = xCurrentScroll + 50; 
                    break; 
 
                // User clicked the left arrow. 
                case SB_LINEUP: 
                    xNewPos = xCurrentScroll - 5; 
                    break; 
 
                // User clicked the right arrow. 
                case SB_LINEDOWN: 
                    xNewPos = xCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    xNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    xNewPos = xCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen width. 
            xNewPos = max(0, xNewPos); 
            xNewPos = min(xMaxScroll, xNewPos); 
 
            // If the current position does not change, do not scroll.
            if (xNewPos == xCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            xDelta = xNewPos - xCurrentScroll; 
 
            // Reset the current scroll position. 
            xCurrentScroll = xNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            break; 
        } 
        
        case WM_VSCROLL: 
        { 
            int xDelta = 0; 
            int yDelta;     // yDelta = new_pos - current_pos 
            int yNewPos;    // new position 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft above the scroll box. 
                case SB_PAGEUP: 
                    yNewPos = yCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft below the scroll box. 
                case SB_PAGEDOWN: 
                    yNewPos = yCurrentScroll + 50; 
                    break; 
 
                // User clicked the top arrow. 
                case SB_LINEUP: 
                    yNewPos = yCurrentScroll - 5; 
                    break; 
 
                // User clicked the bottom arrow. 
                case SB_LINEDOWN: 
                    yNewPos = yCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    yNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    yNewPos = yCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen height. 
            yNewPos = max(0, yNewPos); 
            yNewPos = min(yMaxScroll, yNewPos); 
 
            // If the current position does not change, do not scroll.
            if (yNewPos == yCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            yDelta = yNewPos - yCurrentScroll; 
 
            // Reset the current scroll position. 
            yCurrentScroll = yNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 

        case WM_RBUTTONDOWN:
        {
            // Get the compatible DC of the client area. 
            hdcWin = GetDC(hwnd); 

            // Fill the client area to remove any existing contents. 
            RECT rect;
            GetClientRect(hwnd, &rect);
            FillRect(hdcWin, &rect, (HBRUSH)(COLOR_WINDOW+1));
 
            // Copy the contents of the current screen 
            // into the compatible DC. 
            BitBlt(hdcScreenCompat, 0, 0, bmp.bmWidth, 
                bmp.bmHeight, hdcScreen, 0, 0, SRCCOPY); 
 
            // Copy the compatible DC to the client area.
            BitBlt(hdcWin, 0, 0, bmp.bmWidth, bmp.bmHeight, 
                hdcScreenCompat, 0, 0, SRCCOPY); 
 
            ReleaseDC(hwnd, hdcWin); 
            fBlt = TRUE; 
            break; 
        }

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

 

 