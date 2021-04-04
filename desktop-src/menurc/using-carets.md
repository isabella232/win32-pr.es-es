---
title: Usar las intercalaciones
description: En esta sección se proporcionan ejemplos de código que muestran cómo realizar tareas relacionadas con las intercalaciones.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- recursos, insumos
- insumos, crear
- insumos, Mostrar
- insumos, destruir
- Acentos, ocultar
- Acentos, tiempos de intermitencia
- líneas intermitentes
- bloques en parpadeo
- parpadeo de mapas de bits
- crear insumos
- Mostrar insumos
- ocultar las intercalaciones
- destruir insumos
- tiempos de intermitencia
- entrada de usuario, entrada de teclado
- capturar datos proporcionados por el usuario, entrada mediante teclado
- entrada mediante teclado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077644"
---
# <a name="using-carets"></a>Usar las intercalaciones

Esta sección contiene ejemplos de código para las siguientes tareas:

-   [Crear y mostrar un símbolo de intercalación](#creating-and-displaying-a-caret)
-   [Ocultar un símbolo de intercalación](#hiding-a-caret)
-   [Destruir un símbolo de intercalación](#destroying-a-caret)
-   [Ajustar el tiempo de intermitencia](#adjusting-the-blink-time)
-   [Procesar la entrada del teclado](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Crear y mostrar un símbolo de intercalación

Al recibir el foco de teclado, la ventana debe crear y mostrar el símbolo de intercalación. Usar la función [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para crear un símbolo de intercalación en la ventana determinada. Después, puede llamar a [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) para establecer la posición actual del símbolo de intercalación y [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para que el símbolo de intercalación esté visible.

El sistema envía el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) a la ventana que recibe el foco de teclado; por lo tanto, una aplicación debe crear y mostrar el símbolo de intercalación al procesar este mensaje.


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



Para crear un símbolo de intercalación basado en un mapa de bits, debe especificar un identificador de mapa de bits al usar [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret). Puede usar una aplicación de gráficos para crear el mapa de bits y un compilador de recursos para agregar el mapa de bits a los recursos de la aplicación. A continuación, la aplicación puede usar la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para cargar el identificador de mapa de bits. Por ejemplo, podría reemplazar la línea **CreateCaret** en el ejemplo anterior por las líneas siguientes para crear un símbolo de intercalación de mapa de bits.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Como alternativa, puede usar la función [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) o [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) para recuperar el identificador del mapa de bits del símbolo de intercalación. Para obtener más información sobre los mapas de bits, vea [mapas de bits](/windows/desktop/gdi/bitmaps).

Si la aplicación especifica un identificador de mapa de bits, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) omite los parámetros de ancho y alto. El mapa de bits define el tamaño del símbolo de intercalación.

## <a name="hiding-a-caret"></a>Ocultar un símbolo de intercalación

Cada vez que la aplicación vuelve a dibujar una pantalla mientras procesa un mensaje distinto de [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), debe hacer invisible el símbolo de intercalación mediante la función [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Cuando la aplicación termine de dibujar, vuelva a mostrar el símbolo de intercalación mediante la función [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Si la aplicación procesa el mensaje de **\_ dibujo de WM** , no es necesario ocultar y volver a mostrar el símbolo de intercalación, ya que esta función lo hace automáticamente.

En el ejemplo de código siguiente se muestra cómo hacer que la aplicación oculte el símbolo de intercalación mientras dibuja un carácter en la pantalla y mientras procesa el mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) .


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



Si la aplicación llama a la función [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) varias veces sin llamar a [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), el símbolo de intercalación no se mostrará hasta que la aplicación también llame a **ShowCaret** el mismo número de veces.

## <a name="destroying-a-caret"></a>Destruir un símbolo de intercalación

Cuando una ventana pierde el foco de teclado, el sistema envía el mensaje de [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) a la ventana. La aplicación debe destruir el símbolo de intercalación mientras procesa este mensaje mediante la función [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . En el código siguiente se muestra cómo destruir un símbolo de intercalación en una ventana que ya no tiene el foco de teclado.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Ajustar el tiempo de intermitencia

En Windows de 16 bits, una aplicación basada en Windows podía llamar a la función [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) para guardar la hora de parpadeo actual y, después, llamar a la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para ajustar el tiempo de intermitencia durante su procesamiento del mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) . La aplicación restauraría el tiempo de intermitencia guardado para el uso de otras aplicaciones mediante una llamada a **SetCaretBlinkTime** durante su procesamiento del mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) . Sin embargo, esta técnica no funciona en entornos multiproceso. En concreto, la desactivación de una aplicación no está sincronizada con la activación de otra aplicación, de modo que si una aplicación deja de responder, todavía se puede activar otra aplicación.

Las aplicaciones deben respetar el tiempo de intermitencia elegido por el usuario. Solo una aplicación que permite al usuario establecer el tiempo de parpadeo solo debe llamar a la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) .

## <a name="processing-keyboard-input"></a>Procesar la entrada del teclado

En el ejemplo siguiente se muestra cómo usar un símbolo de intercalación en un editor de texto simple. En el ejemplo se actualiza la posición del símbolo de intercalación a medida que el usuario escribe caracteres imprimibles y utiliza varias teclas para desplazarse por el área cliente.


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 