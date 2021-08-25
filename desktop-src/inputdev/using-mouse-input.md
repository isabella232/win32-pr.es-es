---
title: Uso de la entrada del mouse
description: En esta sección se tratan las tareas asociadas a la entrada del mouse.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- entrada de usuario, entrada del mouse
- capturar la entrada del usuario, la entrada del mouse
- entrada del mouse
- cursores, entrada del mouse
- cursor del mouse
- Procesamiento de mensajes con doble clic
- rueda del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829975"
---
# <a name="using-mouse-input"></a>Uso de la entrada del mouse

En esta sección se tratan las tareas asociadas a la entrada del mouse.

-   [Seguimiento del cursor del mouse](#tracking-the-mouse-cursor)
-   [Dibujar líneas con el mouse](#drawing-lines-with-the-mouse)
-   [Procesamiento de un mensaje de doble clic](#processing-a-double-click-message)
-   [Selección de una línea de texto](#selecting-a-line-of-text)
-   [Usar una rueda del mouse en un documento con objetos incrustados](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Recuperar el número de líneas de desplazamiento de la rueda del mouse](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Seguimiento del cursor del mouse

A menudo, las aplicaciones realizan tareas que implican el seguimiento de la posición del cursor del mouse. Por ejemplo, la mayoría de las aplicaciones de dibujo realiza un seguimiento de la posición del cursor del mouse durante las operaciones de dibujo, lo que permite al usuario dibujar en el área cliente de una ventana arrastrando el mouse. Las aplicaciones de procesamiento de palabras también realiza un seguimiento del cursor, lo que permite al usuario seleccionar una palabra o un bloque de texto haciendo clic y arrastrando el mouse.

Normalmente, el seguimiento del cursor implica el procesamiento de los mensajes [**WM \_ LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)y [**WM \_ LBUTTONUP.**](wm-lbuttonup.md) Una ventana determina cuándo empezar a realizar el seguimiento del cursor comprobando la posición del cursor proporcionada en el parámetro *lParam* del **mensaje WM \_ LBUTTONDOWN.** Por ejemplo, una aplicación de procesamiento de palabras comenzaría a realizar el seguimiento del cursor solo si el mensaje **\_ WM LBUTTONDOWN** se produjo mientras el cursor estaba en una línea de texto, pero no si estaba más allá del final del documento.

Una ventana realiza un seguimiento de la posición del cursor procesando la secuencia de [**mensajes \_ WM MOUSEMOVE**](wm-mousemove.md) publicados en la ventana a medida que se mueve el mouse. El procesamiento **del mensaje \_ MOUSEMOVE** de WM normalmente implica una operación repetitiva de dibujo o dibujo en el área cliente. Por ejemplo, una aplicación de dibujo podría volver a dibujar una línea repetidamente a medida que se mueve el mouse. Una ventana usa el [**mensaje \_ WM LBUTTONUP**](wm-lbuttonup.md) como señal para detener el seguimiento del cursor.

Además, una aplicación puede llamar a la [**función TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que el sistema envíe otros mensajes que sean útiles para realizar el seguimiento del cursor. El sistema envía el [**mensaje \_ WM MOUSEHOVER**](wm-mousehover.md) cuando el cursor mantiene el puntero sobre el área de cliente durante un período de tiempo determinado. Envía el mensaje [**WM \_ MOUSELEAVE**](wm-mouseleave.md) cuando el cursor sale del área de cliente. Los [**mensajes \_ WM NCMOUSEHOVER**](wm-ncmousehover.md) y [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md) son los mensajes correspondientes para las áreas no cliente.

## <a name="drawing-lines-with-the-mouse"></a>Dibujar líneas con el mouse

En el ejemplo de esta sección se muestra cómo realizar un seguimiento del cursor del mouse. Contiene partes de un procedimiento de ventana que permite al usuario dibujar líneas en el área cliente de una ventana arrastrando el mouse.

Cuando el procedimiento de ventana recibe un mensaje [**\_ WM LBUTTONDOWN,**](wm-lbuttondown.md) captura el mouse y guarda las coordenadas del cursor, usando las coordenadas como punto inicial de la línea. También usa la [**función ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) para limitar el cursor al área de cliente durante la operación de dibujo de línea.

Durante el primer [**mensaje \_ MOUSEMOVE**](wm-mousemove.md) de WM, el procedimiento de ventana dibuja una línea desde el punto inicial hasta la posición actual del cursor. Durante los **mensajes \_ WM MOUSEMOVE** posteriores, el procedimiento de ventana borra la línea anterior dibujando sobre ella con un color de lápiz invertido. A continuación, dibuja una nueva línea desde el punto inicial hasta la nueva posición del cursor.

El [**mensaje \_ LBUTTONUP**](wm-lbuttonup.md) de WM indica el final de la operación de dibujo. El procedimiento de ventana libera la captura del mouse y libera el mouse del área de cliente.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>Procesamiento de un mensaje de doble clic

Para recibir mensajes de doble clic, una ventana debe pertenecer a una clase de ventana que tenga el estilo de clase [**\_ DBLCLKS de CS.**](/windows/desktop/winmsg/about-window-classes) Este estilo se establece al registrar la clase de ventana, como se muestra en el ejemplo siguiente.


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



Un mensaje de doble clic siempre va precedido de un mensaje de botón hacia abajo. Por esta razón, las aplicaciones suelen usar un mensaje de doble clic para extender una tarea que comenzó durante un mensaje de botón.

## <a name="selecting-a-line-of-text"></a>Selección de una línea de texto

El ejemplo de esta sección se toma de una aplicación de procesamiento de palabras simple. Incluye código que permite al usuario establecer la posición del elemento de subrayado haciendo clic en cualquier lugar de una línea de texto y seleccionando (resalte) una línea de texto haciendo doble clic en cualquier lugar de la línea.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
    size_t * pcch;
    HRESULT hResult;
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Usar una rueda del mouse en un documento con objetos incrustados

En este ejemplo se presupone un Microsoft Word con varios objetos incrustados:

-   Una hoja Microsoft Excel de cálculo
-   Control de cuadro de lista incrustado que se desplaza en respuesta a la rueda
-   Control de cuadro de texto incrustado que no responde a la rueda

El [mensaje \_ MSH MOUSEWHEEL](about-mouse-input.md) siempre se envía a la ventana principal de Microsoft Word. Esto es así incluso si la hoja de cálculo insertada está activa. En la tabla siguiente se explica cómo se controla el mensaje \_ MSH MOUSEWHEEL según el foco.



| El foco está en                | El control es el siguiente:                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documento de Word              | Word desplaza la ventana del documento.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Hoja de cálculo Excel incrustada | Word publica el mensaje en Excel. Debe decidir si la aplicación incrustada debe responder al mensaje o no.                                                                                                                                                                                                                                                                                                                                                            |
| Control incrustado           | La aplicación debe enviar el mensaje a un control incrustado que tenga el foco y comprobar el código de retorno para ver si el control lo controló. Si el control no lo controló, la aplicación debe desplazarse por la ventana del documento. Por ejemplo, si el usuario hizo clic en un cuadro de lista y luego rodó la rueda, ese control se desplazaría en respuesta a una rotación de rueda. Si el usuario hizo clic en un cuadro de texto y luego giraba la rueda, todo el documento se desplazaría. |



 

En este ejemplo se muestra cómo una aplicación puede controlar los mensajes de las dos ruedas.


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Recuperar el número de líneas de desplazamiento de la rueda del mouse

El código siguiente permite a una aplicación recuperar el número de líneas de desplazamiento mediante la [**función SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 