---
title: Uso de la entrada de teclado
description: En esta sección se tratan las tareas asociadas a la entrada de teclado.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- entrada de usuario, entrada de teclado
- captura de la entrada del usuario, entrada de teclado
- entrada mediante teclado
- mensajes de pulsación de tecla
- mensajes de caracteres
- carets,keyboard input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567600"
---
# <a name="using-keyboard-input"></a>Uso de la entrada de teclado

Una ventana recibe la entrada del teclado en forma de mensajes de pulsación de teclas y mensajes de caracteres. El bucle de mensajes asociado a la ventana debe incluir código para traducir los mensajes de pulsación de tecla en los mensajes de caracteres correspondientes. Si la ventana muestra la entrada de teclado en su área de cliente, debe crear y mostrar un carácter de diálogo para indicar la posición donde se especificará el carácter siguiente. En las secciones siguientes se describe el código implicado en la recepción, el procesamiento y la visualización de la entrada de teclado:

-   [Procesamiento de mensajes de pulsación de teclas](#processing-keystroke-messages)
-   [Traducción de mensajes de caracteres](#translating-character-messages)
-   [Procesar mensajes de caracteres](#processing-character-messages)
-   [Uso del caret](#using-the-caret)
-   [Mostrar la entrada de teclado](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Procesamiento de mensajes de pulsación de teclas

El procedimiento de ventana de la ventana que tiene el foco de teclado recibe mensajes de pulsación de tecla cuando el usuario tipos en el teclado. Los mensajes de pulsación de tecla son [**WM \_ KEYDOWN,**](wm-keydown.md) [**WM \_ KEYUP,**](wm-keyup.md) [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)y [**WM \_ SYSKEYUP.**](wm-syskeyup.md) Un procedimiento de ventana típico omite todos los mensajes de pulsación de tecla excepto **WM \_ KEYDOWN**. El sistema envía el **mensaje WM \_ KEYDOWN** cuando el usuario presiona una tecla.

Cuando el procedimiento de ventana recibe el mensaje [**\_ WM KEYDOWN,**](wm-keydown.md) debe examinar el código de clave virtual que acompaña al mensaje para determinar cómo procesar la pulsación de tecla. El código de clave virtual está en el parámetro *wParam del* mensaje. Normalmente, una aplicación procesa solo las pulsaciones de teclas generadas por claves que no son de caracteres, incluidas las claves de función, las claves de movimiento del cursor y las claves de propósito especial, como INS, DEL, HOME y END.

En el ejemplo siguiente se muestra el marco de procedimientos de ventana que usa una aplicación típica para recibir y procesar mensajes de pulsación de tecla.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Traducción de mensajes de caracteres

Cualquier subproceso que reciba la entrada de caracteres del usuario debe incluir [**la función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) en su bucle de mensajes. Esta función examina el código de clave virtual de un mensaje de pulsación de tecla y, si el código corresponde a un carácter, coloca un mensaje de carácter en la cola de mensajes. El mensaje de carácter se quita y se envía en la siguiente iteración del bucle de mensajes; El *parámetro wParam* del mensaje contiene el código de carácter.

En general, el bucle de mensajes de un subproceso debe usar la [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para traducir todos los mensajes, no solo los mensajes de clave virtual. Aunque **TranslateMessage** no tiene ningún efecto en otros tipos de mensajes, garantiza que la entrada del teclado se traduce correctamente. En el ejemplo siguiente se muestra cómo incluir la **función TranslateMessage** en un bucle de mensajes de subproceso típico.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Procesar mensajes de caracteres

Un procedimiento de ventana recibe un mensaje de carácter cuando [**la función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un código de clave virtual correspondiente a una clave de carácter. Los mensajes de caracteres [**son WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)y [**WM \_ SYSDEADCHAR.**](wm-sysdeadchar.md) Un procedimiento de ventana típico omite todos los mensajes de caracteres excepto **WM \_ CHAR.** La **función TranslateMessage** genera un **mensaje CHAR \_ de WM** cuando el usuario presiona cualquiera de las siguientes teclas:

-   Cualquier clave de carácter
-   RETROCESO
-   ENTER (retorno de carro)
-   ESC
-   MAYÚS+ENTRAR (linefeed)
-   TAB

Cuando un procedimiento de ventana recibe el [**mensaje \_ CHAR de WM,**](wm-char.md) debe examinar el código de caracteres que acompaña al mensaje para determinar cómo procesar el carácter. El código de carácter está en el parámetro *wParam del* mensaje.

En el ejemplo siguiente se muestra el marco de procedimientos de ventana que una aplicación típica usa para recibir y procesar mensajes de caracteres.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Uso del caret

Una ventana que recibe la entrada de teclado normalmente muestra los caracteres que el usuario tipos en el área de cliente de la ventana. Una ventana debe usar un carácter de diálogo para indicar la posición en el área de cliente donde aparecerá el carácter siguiente. La ventana también debe crear y mostrar el centro de diálogo cuando recibe el foco del teclado, y ocultar y destruir el centro de atención cuando pierde el foco. Una ventana puede realizar estas operaciones en el procesamiento de los mensajes [**\_ WM SETFOCUS**](wm-setfocus.md) y [**WM \_ KILLFOCUS.**](wm-killfocus.md) Para obtener más información sobre los carets, vea [Carets](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Mostrar la entrada de teclado

En el ejemplo de esta sección se muestra cómo una aplicación puede recibir caracteres del teclado, mostrarlos en el área de cliente de una ventana y actualizar la posición del carácter de subrayado con cada carácter con tipo. También muestra cómo mover el símbolo de cursor en respuesta a las pulsaciones de tecla FLECHA IZQUIERDA, FLECHA DERECHA, INICIO y FIN, y muestra cómo resaltar el texto seleccionado en respuesta a la combinación de teclas MAYÚS+FLECHA DERECHA.

Durante el procesamiento del [**mensaje \_ WM CREATE,**](/windows/desktop/winmsg/wm-create) el procedimiento de ventana que se muestra en el ejemplo asigna un búfer de 64 K para almacenar la entrada del teclado. También recupera las métricas de la fuente cargada actualmente, guardando el alto y el ancho medio de los caracteres en la fuente. El alto y el ancho se usan en el procesamiento del mensaje [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para calcular la longitud de línea y el número máximo de líneas, en función del tamaño del área de cliente.

El procedimiento de ventana crea y muestra el caret al procesar el [**\_ mensaje SETFOCUS de WM.**](wm-setfocus.md) Oculta y elimina el centro de atención al procesar el [**mensaje \_ KILLFOCUS de WM.**](wm-killfocus.md)

Al procesar el [**mensaje \_ WM CHAR,**](wm-char.md) el procedimiento de ventana muestra caracteres, los almacena en el búfer de entrada y actualiza la posición del carácter de cursor. El procedimiento de ventana también convierte los caracteres de tabulación en cuatro caracteres de espacio consecutivos. El retroceso, el linefeed y los caracteres de escape generan un pitido, pero no se procesan de otro modo.

El procedimiento de ventana realiza los movimientos de la parte izquierda, derecha, final e inicio al procesar el [**mensaje \_ KEYDOWN de WM.**](wm-keydown.md) Al procesar la acción de la tecla FLECHA DERECHA, el procedimiento de ventana comprueba el estado de la tecla MAYÚS y, si está fuera de servicio, selecciona el carácter a la derecha del carácter de cursor mientras se mueve el carácter de cursor.

Tenga en cuenta que el código siguiente está escrito para que se pueda compilar como Unicode o como ANSI. Si el código fuente define UNICODE, las cadenas se controlan como caracteres Unicode; De lo contrario, se controlan como caracteres ANSI.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
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
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 