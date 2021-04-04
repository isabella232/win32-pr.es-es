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
# <a name="using-carets"></a><span data-ttu-id="a5db3-120">Usar las intercalaciones</span><span class="sxs-lookup"><span data-stu-id="a5db3-120">Using Carets</span></span>

<span data-ttu-id="a5db3-121">Esta sección contiene ejemplos de código para las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a5db3-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="a5db3-122">Crear y mostrar un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="a5db3-123">Ocultar un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="a5db3-124">Destruir un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="a5db3-125">Ajustar el tiempo de intermitencia</span><span class="sxs-lookup"><span data-stu-id="a5db3-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="a5db3-126">Procesar la entrada del teclado</span><span class="sxs-lookup"><span data-stu-id="a5db3-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="a5db3-127">Crear y mostrar un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="a5db3-128">Al recibir el foco de teclado, la ventana debe crear y mostrar el símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a5db3-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="a5db3-129">Usar la función [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para crear un símbolo de intercalación en la ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="a5db3-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="a5db3-130">Después, puede llamar a [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) para establecer la posición actual del símbolo de intercalación y [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para que el símbolo de intercalación esté visible.</span><span class="sxs-lookup"><span data-stu-id="a5db3-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="a5db3-131">El sistema envía el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) a la ventana que recibe el foco de teclado; por lo tanto, una aplicación debe crear y mostrar el símbolo de intercalación al procesar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a5db3-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


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



<span data-ttu-id="a5db3-132">Para crear un símbolo de intercalación basado en un mapa de bits, debe especificar un identificador de mapa de bits al usar [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span><span class="sxs-lookup"><span data-stu-id="a5db3-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="a5db3-133">Puede usar una aplicación de gráficos para crear el mapa de bits y un compilador de recursos para agregar el mapa de bits a los recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5db3-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="a5db3-134">A continuación, la aplicación puede usar la función [**loadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para cargar el identificador de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a5db3-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="a5db3-135">Por ejemplo, podría reemplazar la línea **CreateCaret** en el ejemplo anterior por las líneas siguientes para crear un símbolo de intercalación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a5db3-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="a5db3-136">Como alternativa, puede usar la función [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) o [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) para recuperar el identificador del mapa de bits del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a5db3-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="a5db3-137">Para obtener más información sobre los mapas de bits, vea [mapas de bits](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="a5db3-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="a5db3-138">Si la aplicación especifica un identificador de mapa de bits, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) omite los parámetros de ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="a5db3-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="a5db3-139">El mapa de bits define el tamaño del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a5db3-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="a5db3-140">Ocultar un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-140">Hiding a Caret</span></span>

<span data-ttu-id="a5db3-141">Cada vez que la aplicación vuelve a dibujar una pantalla mientras procesa un mensaje distinto de [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), debe hacer invisible el símbolo de intercalación mediante la función [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="a5db3-142">Cuando la aplicación termine de dibujar, vuelva a mostrar el símbolo de intercalación mediante la función [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="a5db3-143">Si la aplicación procesa el mensaje de **\_ dibujo de WM** , no es necesario ocultar y volver a mostrar el símbolo de intercalación, ya que esta función lo hace automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a5db3-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="a5db3-144">En el ejemplo de código siguiente se muestra cómo hacer que la aplicación oculte el símbolo de intercalación mientras dibuja un carácter en la pantalla y mientras procesa el mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


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



<span data-ttu-id="a5db3-145">Si la aplicación llama a la función [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) varias veces sin llamar a [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), el símbolo de intercalación no se mostrará hasta que la aplicación también llame a **ShowCaret** el mismo número de veces.</span><span class="sxs-lookup"><span data-stu-id="a5db3-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="a5db3-146">Destruir un símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a5db3-146">Destroying a Caret</span></span>

<span data-ttu-id="a5db3-147">Cuando una ventana pierde el foco de teclado, el sistema envía el mensaje de [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5db3-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="a5db3-148">La aplicación debe destruir el símbolo de intercalación mientras procesa este mensaje mediante la función [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="a5db3-149">En el código siguiente se muestra cómo destruir un símbolo de intercalación en una ventana que ya no tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="a5db3-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="a5db3-150">Ajustar el tiempo de intermitencia</span><span class="sxs-lookup"><span data-stu-id="a5db3-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="a5db3-151">En Windows de 16 bits, una aplicación basada en Windows podía llamar a la función [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) para guardar la hora de parpadeo actual y, después, llamar a la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para ajustar el tiempo de intermitencia durante su procesamiento del mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="a5db3-152">La aplicación restauraría el tiempo de intermitencia guardado para el uso de otras aplicaciones mediante una llamada a **SetCaretBlinkTime** durante su procesamiento del mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="a5db3-153">Sin embargo, esta técnica no funciona en entornos multiproceso.</span><span class="sxs-lookup"><span data-stu-id="a5db3-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="a5db3-154">En concreto, la desactivación de una aplicación no está sincronizada con la activación de otra aplicación, de modo que si una aplicación deja de responder, todavía se puede activar otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5db3-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="a5db3-155">Las aplicaciones deben respetar el tiempo de intermitencia elegido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a5db3-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="a5db3-156">Solo una aplicación que permite al usuario establecer el tiempo de parpadeo solo debe llamar a la función [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) .</span><span class="sxs-lookup"><span data-stu-id="a5db3-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="a5db3-157">Procesar la entrada del teclado</span><span class="sxs-lookup"><span data-stu-id="a5db3-157">Processing Keyboard Input</span></span>

<span data-ttu-id="a5db3-158">En el ejemplo siguiente se muestra cómo usar un símbolo de intercalación en un editor de texto simple.</span><span class="sxs-lookup"><span data-stu-id="a5db3-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="a5db3-159">En el ejemplo se actualiza la posición del símbolo de intercalación a medida que el usuario escribe caracteres imprimibles y utiliza varias teclas para desplazarse por el área cliente.</span><span class="sxs-lookup"><span data-stu-id="a5db3-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


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



 

 