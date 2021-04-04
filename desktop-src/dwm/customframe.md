---
title: Marco de ventana personalizado mediante DWM
description: En este tema se muestra cómo usar las API de Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Administrador de ventanas de escritorio (DWM), marcos de ventana personalizados
- DWM (Administrador de ventanas de escritorio), marcos de ventana personalizados
- marcos de ventana personalizados
- quitar fotogramas estándar
- extender fotogramas de cliente
- Administrador de ventanas de escritorio (DWM), extender fotogramas de cliente
- DWM (Administrador de ventanas de escritorio), extender fotogramas de cliente
- Administrador de ventanas de escritorio (DWM), quitar fotogramas estándar
- DWM (Administrador de ventanas de escritorio), quitar fotogramas estándar
- Administrador de ventanas de escritorio (DWM), dibujar en marcos extendidos
- DWM (Administrador de ventanas de escritorio), dibujar en marcos extendidos
- dibujar en marcos extendidos
- comprobación de visitas
- Administrador de ventanas de escritorio (DWM), prueba de posicionamiento
- DWM (Administrador de ventanas de escritorio), prueba de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078337"
---
# <a name="custom-window-frame-using-dwm"></a>Marco de ventana personalizado mediante DWM

En este tema se muestra cómo usar las API de Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.

-   [Introducción](#introduction)
-   [Extender el marco de cliente](#extending-the-client-frame)
-   [Quitar el fotograma estándar](#removing-the-standard-frame)
-   [Dibujar en la ventana de marco extendido](#drawing-in-the-extended-frame-window)
-   [Habilitar la prueba de posicionamiento para el marco personalizado](#enabling-hit-testing-for-the-custom-frame)
-   [Apéndice A: procedimiento de ventana de ejemplo](#appendix-a-sample-window-procedure)
-   [Apéndice B: pintar el título del título](#appendix-b-painting-the-caption-title)
-   [Apéndice C: función HitTestNCA](#appendix-c-hittestnca-function)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En Windows Vista y versiones posteriores, el DWM controla la apariencia de las áreas no cliente de las ventanas de la aplicación (la barra de título, el icono, el borde de la ventana y los botones de título). Con las API de DWM, puede cambiar la forma en que DWM representa el marco de una ventana.

Una característica de las API de DWM es la capacidad de extender el marco de aplicación en el área de cliente. Esto le permite integrar un elemento de la interfaz de usuario de cliente (por ejemplo, una barra de herramientas) en el marco, de forma que la interfaz de usuario controla un lugar más destacado en la interfaz de usuario de la aplicación. Por ejemplo, Windows Internet Explorer 7 en Windows Vista integra la barra de navegación en el marco de la ventana extendiendo la parte superior del marco, tal como se muestra en la siguiente captura de pantalla.

![barra de navegación integrada en el marco de la ventana.](images/ie7-extendedborder-boxed.png)

La capacidad de extender el marco de ventana también le permite crear fotogramas personalizados mientras mantiene la apariencia y el funcionamiento de la ventana. Por ejemplo, Microsoft Office Word 2007 dibuja el botón de Office y la barra de herramientas de acceso rápido dentro del marco personalizado, a la vez que proporciona los botones estándar minimizar, maximizar y cerrar título, como se muestra en la siguiente captura de pantalla.

![botón de Office y barra de herramientas de acceso rápido en Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Extender el marco de cliente

La función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) expone la funcionalidad para extender el marco en el área cliente. Para extender el marco, pase el identificador de la ventana de destino junto con los valores de margen de margen a **DwmExtendFrameIntoClientArea**. Los valores de bajorrelieve del margen determinan hasta qué punto se extiende el marco en los cuatro lados de la ventana.

En el código siguiente se muestra el uso de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) para extender el marco.


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



Tenga en cuenta que la extensión de marco se realiza dentro del mensaje de [**\_ activación de WM**](/windows/desktop/inputdev/wm-activate) en lugar del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) . Esto garantiza que la extensión de marco se administra correctamente cuando la ventana tiene el tamaño predeterminado y cuando está maximizada.

La siguiente imagen muestra un marco de ventana estándar (a la izquierda) y el mismo marco de ventana extendido (a la derecha). El marco se extiende mediante el ejemplo de código anterior y el predeterminado Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (color \_ window + 1).

![captura de pantalla de un fotograma estándar (izquierda) y marco extendido (derecha) con fondo blanco](images/white-sidebyside.png)

La diferencia visual entre estas dos ventanas es muy sutil. La única diferencia entre los dos es que en la ventana de la derecha falta el borde de línea negra fina de la región cliente en la ventana de la izquierda. El motivo de este borde que falta es que se incorpora en el marco extendido, pero el resto del área cliente no lo está. Para que los fotogramas extendidos sean visibles, las regiones subyacentes de cada uno de los lados del marco extendido deben tener datos de píxeles con un valor alfa de 0. El borde negro alrededor de la región del cliente tiene datos de píxeles en los que todos los valores de color (rojo, verde, azul y alfa) se establecen en 0. El resto del fondo no tiene el valor alfa establecido en 0, por lo que el resto del marco extendido no es visible.

La manera más sencilla de asegurarse de que los fotogramas extendidos están visibles es pintar todo el color de la región cliente. Para ello, inicialice el miembro *hbrBackground* de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en el identificador del pincel negro de acciones \_ . La siguiente imagen muestra el mismo marco estándar (izquierda) y el marco extendido (derecha) mostrados anteriormente. Sin embargo, esta vez *hbrBackground* se establece en el \_ controlador de pincel negro Obtenido de la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .

![captura de pantalla de un fotograma estándar (izquierda) y marco extendido (derecha) con fondo negro](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Quitar el fotograma estándar

Después de extender el marco de la aplicación y hacer que esté visible, puede quitar el fotograma estándar. Quitar el fotograma estándar permite controlar el ancho de cada lado del marco en lugar de simplemente extender el fotograma estándar.

Para quitar el marco de ventana estándar, debe controlar el mensaje de [**\_ NCCALCSIZE de WM**](/windows/desktop/winmsg/wm-nccalcsize) , en concreto cuando el valor de *wParam* es **true** y el valor devuelto es 0. Al hacerlo, la aplicación usa toda la región de la ventana como el área cliente, quitando el fotograma estándar.

Los resultados del control del mensaje de [**\_ NCCALCSIZE de WM**](/windows/desktop/winmsg/wm-nccalcsize) no estarán visibles hasta que sea necesario cambiar el tamaño de la región del cliente. Hasta ese momento, la vista inicial de la ventana aparece con el marco estándar y los bordes extendidos. Para solucionar este error, debe cambiar el tamaño de la ventana o realizar una acción que inicie un mensaje de **\_ NCCALCSIZE de WM** en el momento de la creación de la ventana. Esto puede realizarse mediante el uso de la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para desplace la ventana y cambiar su tamaño. En el código siguiente se muestra una llamada a **SetWindowPos** que fuerza el envío de un mensaje de **WM \_ NCCALCSIZE** con los atributos de rectángulo de la ventana actual y la \_ marca FRAMECHANGED de SWP.


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



En la imagen siguiente se muestra el marco estándar (izquierda) y el fotograma recién extendido sin el marco estándar (derecha).

![captura de pantalla de un fotograma estándar (izquierda) y un fotograma personalizado (derecha)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Dibujar en la ventana de marco extendido

Al quitar el fotograma estándar, pierde el dibujo automático del icono de la aplicación y del título. Para volver a agregarlos a la aplicación, debe dibujarlos usted mismo. Para ello, primero examine el cambio que se ha producido en el área de cliente.

Con la eliminación del fotograma estándar, el área de cliente ahora se compone de toda la ventana, incluido el marco extendido. Esto incluye la región donde se dibujan los botones de título. En la siguiente comparación en paralelo, el área cliente para el fotograma estándar y el marco extendido personalizado se resaltan en rojo. El área cliente de la ventana de marco estándar (izquierda) es la región negra. En la ventana marco extendido (derecha), el área cliente es toda la ventana.

![captura de pantalla de las áreas de cliente destacadas en rojo en el marco estándar y personalizado](images/clientarea-sidebyside.png)

Dado que toda la ventana es el área de cliente, puede dibujar simplemente lo que desea en el marco extendido. Para agregar un título a la aplicación, solo tiene que dibujar texto en la región adecuada. En la imagen siguiente se muestra el texto con los que se dibuja en el marco de título personalizado. El título se dibuja con la función [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) . Para ver el código que pinta el título, vea [el Apéndice B: pintar el título del](#appendix-b-painting-the-caption-title)título.

![captura de pantalla de un marco personalizado con título](images/custom-caption-title.png)

> [!Note]  
> Al dibujar en el marco personalizado, tenga cuidado al colocar controles de interfaz de usuario. Dado que toda la ventana es su región de cliente, debe ajustar la posición del control de interfaz de usuario para cada ancho de marco si no desea que aparezcan en o en el marco extendido.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Habilitar la prueba de posicionamiento para el marco personalizado

Un efecto secundario de quitar el fotograma estándar es la pérdida del cambio de tamaño y el comportamiento de movimiento predeterminados. Para que la aplicación eMule correctamente el comportamiento estándar de las ventanas, debe implementar la lógica para controlar las pruebas de posicionamiento de los botones de título y el cambio de tamaño o movimiento de fotogramas.

En el caso de las pruebas de posicionamiento de los botones de título, DWM proporciona la función [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) . Para realizar correctamente una prueba de posicionamiento de los botones de título en escenarios de fotogramas personalizados, los mensajes se deben pasar primero a **DwmDefWindowProc** para el control. **DwmDefWindowProc** devuelve **true** si se controla un mensaje y **false** en caso contrario. Si **DwmDefWindowProc** no controla el mensaje, la aplicación debe controlar el mensaje en sí o pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Para cambiar el tamaño y mover el marco, la aplicación debe proporcionar la lógica de la prueba de posicionamiento y controlar los mensajes de prueba de posicionamiento del marco. Los mensajes de prueba de posicionamiento de fotogramas se le envían a través del mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) , incluso si la aplicación crea un marco personalizado sin el marco estándar. En el código siguiente se muestra cómo controlar el mensaje de **\_ NCHITTEST de WM** cuando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no lo controla. Para ver el código de la `HitTestNCA` función llamada, vea [Apéndice C: función HitTestNCA](#appendix-c-hittestnca-function).


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a>Apéndice A: procedimiento de ventana de ejemplo

En el ejemplo de código siguiente se muestra un procedimiento de ventana y sus funciones de trabajo auxiliares que se usan para crear una aplicación de marco personalizada.


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
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



## <a name="appendix-b-painting-the-caption-title"></a>Apéndice B: pintar el título del título

En el código siguiente se muestra cómo pintar un título de título en el marco extendido. Se debe llamar a esta función desde las llamadas a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a>Apéndice C: función HitTestNCA

En el código siguiente se muestra la función que se `HitTestNCA` usa [para habilitar la prueba de posicionamiento para el marco personalizado](#enabling-hit-testing-for-the-custom-frame). Esta función controla la lógica de la prueba de posicionamiento para el [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) cuando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no controla el mensaje.


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)
</dt> </dl>

 

 