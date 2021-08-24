---
title: Marco de ventana personalizado mediante DWM
description: En este tema se muestra cómo usar las API Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Administrador de ventanas de escritorio (DWM), marcos de ventana personalizados
- DWM (Administrador de ventanas de escritorio), marcos de ventana personalizados
- marcos de ventana personalizados
- quitar fotogramas estándar
- ampliación de marcos de cliente
- Administrador de ventanas de escritorio (DWM), ampliar marcos de cliente
- DWM (Administrador de ventanas de escritorio), ampliación de marcos de cliente
- Administrador de ventanas de escritorio (DWM), quitar fotogramas estándar
- DWM (Administrador de ventanas de escritorio), quitar fotogramas estándar
- Administrador de ventanas de escritorio (DWM), dibujar en marcos extendidos
- DWM (Administrador de ventanas de escritorio), dibujar en marcos extendidos
- dibujar en marcos extendidos
- comprobación de visitas
- Administrador de ventanas de escritorio (DWM), pruebas de impacto
- DWM (Administrador de ventanas de escritorio), pruebas de impacto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b440f475dfacc610354ce151ab0be42dbbe3069390b1efa211195252f7a3914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741478"
---
# <a name="custom-window-frame-using-dwm"></a>Marco de ventana personalizado mediante DWM

En este tema se muestra cómo usar las API Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.

-   [Introducción](#introduction)
-   [Extensión del marco de cliente](#extending-the-client-frame)
-   [Quitar el marco estándar](#removing-the-standard-frame)
-   [Dibujo en la ventana marco extendido](#drawing-in-the-extended-frame-window)
-   [Habilitación de las pruebas de acceso para el marco personalizado](#enabling-hit-testing-for-the-custom-frame)
-   [Apéndice A: Procedimiento de ventana de ejemplo](#appendix-a-sample-window-procedure)
-   [Apéndice B: Pintar el título del título](#appendix-b-painting-the-caption-title)
-   [Apéndice C: Función HitTestNCA](#appendix-c-hittestnca-function)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En Windows Vista y versiones posteriores, el DWM controla la apariencia de las áreas que no son cliente de las ventanas de la aplicación (la barra de título, el icono, el borde de la ventana y los botones de título). Con las API de DWM, puede cambiar la forma en que DWM representa el marco de una ventana.

Una característica de las API de DWM es la capacidad de ampliar el marco de aplicación en el área cliente. Esto le permite integrar un elemento de interfaz de usuario de cliente,como una barra de herramientas, en el marco, lo que proporciona a los controles de interfaz de usuario un lugar más destacado en la interfaz de usuario de la aplicación. Por ejemplo, Windows Internet Explorer 7 en Windows Vista integra la barra de navegación en el marco de ventana extendiendo la parte superior del marco, como se muestra en la siguiente captura de pantalla.

![barra de navegación integrada en el marco de ventana.](images/ie7-extendedborder-boxed.png)

La capacidad de ampliar el marco de ventana también le permite crear fotogramas personalizados mientras mantiene la apariencia de la ventana. Por ejemplo, Microsoft Office Word 2007 dibuja el botón Office y la barra de herramientas acceso rápido dentro del marco personalizado, al tiempo que proporciona los botones estándar Minimizar, Maximizar y Cerrar título, como se muestra en la siguiente captura de pantalla.

![Botón office y barra de herramientas de acceso rápido en word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Extensión del marco de cliente

La función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) expone la funcionalidad para ampliar el marco en el área de cliente. Para extender el marco, pase el identificador de la ventana de destino junto con los valores del conjunto de márgenes a **DwmExtendFrameIntoClientArea**. Los valores del conjunto de márgenes determinan hasta qué punto extender el marco en los cuatro lados de la ventana.

En el código siguiente se muestra el uso [**de DwmExtendFrameIntoClientArea para**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) ampliar el marco.


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



Tenga en cuenta que la extensión de marco se realiza dentro del [**mensaje WM \_ ACTIVATE**](/windows/desktop/inputdev/wm-activate) en lugar del [**mensaje WM \_ CREATE.**](/windows/desktop/winmsg/wm-create) Esto garantiza que la extensión de marco se controla correctamente cuando la ventana tiene su tamaño predeterminado y cuando está maximizada.

En la imagen siguiente se muestra un marco de ventana estándar (a la izquierda) y el mismo marco de ventana extendido (a la derecha). El marco se extiende con el ejemplo de código anterior y el Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) (COLOR \_ WINDOW +1).

![captura de pantalla de un marco estándar (izquierda) y extendido (derecha) con fondo blanco](images/white-sidebyside.png)

La diferencia visual entre estas dos ventanas es muy sutil. La única diferencia entre los dos es que falta el borde fino de la línea negra de la región del cliente en la ventana de la izquierda en la ventana de la derecha. El motivo de que falte este borde es que se incorpora en el marco extendido, pero el resto del área cliente no lo está. Para que los fotogramas extendidos sean visibles, las regiones subyacentes a cada uno de los lados del marco extendido deben tener datos de píxeles con un valor alfa de 0. El borde negro alrededor de la región del cliente tiene datos de píxeles en los que todos los valores de color (rojo, verde, azul y alfa) se establecen en 0. El resto del fondo no tiene el valor alfa establecido en 0, por lo que el resto del marco extendido no está visible.

La manera más fácil de asegurarse de que los marcos extendidos son visibles es pintar toda la región de cliente en negro. Para ello, inicialice el *miembro hbrBackground* de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en el identificador del pincel negro \_ de existencias. En la imagen siguiente se muestra el mismo marco estándar (izquierdo) y el marco extendido (derecha) mostrados anteriormente. Esta vez, sin embargo, *hbrBackground* se establece en el identificador BLACK BRUSH obtenido \_ de la función [**GetStockObject.**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject)

![captura de pantalla de un marco estándar (izquierda) y extendido (derecha) con fondo negro](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Quitar el marco estándar

Una vez que haya ampliado el marco de la aplicación y lo haya hecho visible, puede quitar el marco estándar. Quitar el marco estándar le permite controlar el ancho de cada lado del marco en lugar de simplemente extender el marco estándar.

Para quitar el marco de ventana estándar, debe controlar el mensaje [**\_ WM NCCALCSIZE,**](/windows/desktop/winmsg/wm-nccalcsize) específicamente cuando su valor *wParam* es **TRUE** y el valor devuelto es 0. Al hacerlo, la aplicación usa toda la región de ventana como área de cliente, quitando el marco estándar.

Los resultados del control del [**mensaje \_ WM NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) no son visibles hasta que sea necesario cambiar el tamaño de la región del cliente. Hasta ese momento, la vista inicial de la ventana aparece con el marco estándar y los bordes extendidos. Para solucionar este problema, debe cambiar el tamaño de la ventana o realizar una acción que inicie un mensaje **\_ WM NCCALCSIZE** en el momento de la creación de la ventana. Esto se puede lograr mediante la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover la ventana y cambiar su tamaño. El código siguiente muestra una llamada a **SetWindowPos** que fuerza el envío de un mensaje **\_ WM NCCALCSIZE** mediante los atributos de rectángulo de ventana actuales y la marca \_ SWP FRAMECHANGED.


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



En la imagen siguiente se muestra el marco estándar (izquierda) y el marco recién extendido sin el marco estándar (derecha).

![captura de pantalla de un marco estándar (izquierda) y marco personalizado (derecha)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Dibujo en la ventana marco extendido

Al quitar el marco estándar, se pierde el dibujo automático del icono y el título de la aplicación. Para volver a agregarlos a la aplicación, debe dibujarlos usted mismo. Para ello, primero debe ver el cambio que se ha producido en el área cliente.

Con la eliminación del marco estándar, el área de cliente ahora consta de toda la ventana, incluido el marco extendido. Esto incluye la región donde se dibujan los botones de título. En la siguiente comparación en paralelo, el área de cliente para el marco estándar y el marco extendido personalizado se resalta en rojo. El área de cliente de la ventana de marco estándar (izquierda) es la región negra. En la ventana marco extendido (derecha), el área de cliente es toda la ventana.

![captura de pantalla de las áreas de cliente resaltadas de color rojo en el marco estándar y personalizado](images/clientarea-sidebyside.png)

Dado que toda la ventana es el área de cliente, simplemente puede dibujar lo que quiera en el marco extendido. Para agregar un título a la aplicación, basta con dibujar texto en la región adecuada. En la imagen siguiente se muestra el texto con temas dibujado en el marco de título personalizado. El título se dibuja mediante [**la función DrawThemeTextEx.**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) Para ver el código que pinta el título, vea [Apéndice B: Pintar el título del título](#appendix-b-painting-the-caption-title).

![captura de pantalla de un marco personalizado con título](images/custom-caption-title.png)

> [!Note]  
> Al dibujar en el marco personalizado, tenga cuidado al colocar controles de interfaz de usuario. Dado que toda la ventana es la región del cliente, debe ajustar la ubicación del control de interfaz de usuario para cada ancho de marco si no desea que aparezcan en o en el marco extendido.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Habilitación de las pruebas de acceso para el marco personalizado

Un efecto secundario de quitar el marco estándar es la pérdida del comportamiento de cambio de tamaño y movimiento predeterminado. Para que la aplicación emule correctamente el comportamiento de la ventana estándar, deberá implementar lógica para controlar las pruebas de posición del botón de título y cambiar el tamaño o el movimiento del marco.

Para las pruebas de pulsación del botón de título, DWM [**proporciona la función DwmDefWindowProc.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) Para probar correctamente los botones de título en escenarios de fotogramas personalizados, primero se deben pasar mensajes a **DwmDefWindowProc** para su control. **DwmDefWindowProc devuelve** **TRUE si** se controla un mensaje y **FALSE** si no lo está. Si **DwmDefWindowProc** no controla el mensaje, la aplicación debe controlar el propio mensaje o pasarlo [**a DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Para cambiar el tamaño y el movimiento de fotogramas, la aplicación debe proporcionar la lógica de prueba de impacto y controlar los mensajes de prueba de impacto del marco. Los mensajes de prueba de acceso de marco se envían a través del mensaje [**\_ WM NCHITTEST,**](/windows/desktop/inputdev/wm-nchittest) incluso si la aplicación crea un marco personalizado sin el marco estándar. El código siguiente muestra cómo controlar el **mensaje \_ WM NCHITTEST** [**cuando DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no lo controla. Para ver el código de la función `HitTestNCA` llamada, vea [Apéndice C: HitTestNCA Function](#appendix-c-hittestnca-function).


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



## <a name="appendix-a-sample-window-procedure"></a>Apéndice A: Procedimiento de ventana de ejemplo

En el ejemplo de código siguiente se muestra un procedimiento de ventana y sus funciones de trabajo compatibles que se usan para crear una aplicación de marco personalizado.


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



## <a name="appendix-b-painting-the-caption-title"></a>Apéndice B: Pintar el título del título

En el código siguiente se muestra cómo pintar un título de título en el marco extendido. Se debe llamar a esta función desde dentro de [**las llamadas BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) [**y EndPaint.**](/windows/desktop/api/winuser/nf-winuser-endpaint)


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



## <a name="appendix-c-hittestnca-function"></a>Apéndice C: Función HitTestNCA

En el código siguiente se muestra `HitTestNCA` la función utilizada en Habilitar las [pruebas de acceso para el marco personalizado.](#enabling-hit-testing-for-the-custom-frame) Esta función controla la lógica de prueba de acceso para [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) cuando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no controla el mensaje.


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

 

 