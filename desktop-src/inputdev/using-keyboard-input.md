---
title: Usar la entrada del teclado
description: En esta sección se describen las tareas que están asociadas a la entrada de teclado.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- entrada de usuario, entrada de teclado
- capturar datos proporcionados por el usuario, entrada mediante teclado
- entrada mediante teclado
- mensajes de pulsación de teclas
- mensajes de caracteres
- insumos, entrada de teclado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714375"
---
# <a name="using-keyboard-input"></a><span data-ttu-id="a1715-109">Usar la entrada del teclado</span><span class="sxs-lookup"><span data-stu-id="a1715-109">Using Keyboard Input</span></span>

<span data-ttu-id="a1715-110">Una ventana recibe la entrada del teclado en forma de mensajes de pulsación de teclas y mensajes de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1715-110">A window receives keyboard input in the form of keystroke messages and character messages.</span></span> <span data-ttu-id="a1715-111">El bucle de mensajes asociado a la ventana debe incluir código para traducir los mensajes de pulsación de tecla en los mensajes de caracteres correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a1715-111">The message loop attached to the window must include code to translate keystroke messages into the corresponding character messages.</span></span> <span data-ttu-id="a1715-112">Si la ventana muestra la entrada de teclado en su área de cliente, debe crear y mostrar un símbolo de intercalación para indicar la posición en la que se escribirá el siguiente carácter.</span><span class="sxs-lookup"><span data-stu-id="a1715-112">If the window displays keyboard input in its client area, it should create and display a caret to indicate the position where the next character will be entered.</span></span> <span data-ttu-id="a1715-113">En las secciones siguientes se describe el código implicado en la recepción, el procesamiento y la visualización de la entrada del teclado:</span><span class="sxs-lookup"><span data-stu-id="a1715-113">The following sections describe the code involved in receiving, processing, and displaying keyboard input:</span></span>

-   [<span data-ttu-id="a1715-114">Procesar mensajes de pulsación de tecla</span><span class="sxs-lookup"><span data-stu-id="a1715-114">Processing Keystroke Messages</span></span>](#processing-keystroke-messages)
-   [<span data-ttu-id="a1715-115">Traducir mensajes de caracteres</span><span class="sxs-lookup"><span data-stu-id="a1715-115">Translating Character Messages</span></span>](#translating-character-messages)
-   [<span data-ttu-id="a1715-116">Procesamiento de mensajes de caracteres</span><span class="sxs-lookup"><span data-stu-id="a1715-116">Processing Character Messages</span></span>](#processing-character-messages)
-   [<span data-ttu-id="a1715-117">Usar el símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a1715-117">Using the Caret</span></span>](#using-the-caret)
-   [<span data-ttu-id="a1715-118">Mostrar la entrada del teclado</span><span class="sxs-lookup"><span data-stu-id="a1715-118">Displaying Keyboard Input</span></span>](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a><span data-ttu-id="a1715-119">Procesar mensajes de pulsación de tecla</span><span class="sxs-lookup"><span data-stu-id="a1715-119">Processing Keystroke Messages</span></span>

<span data-ttu-id="a1715-120">El procedimiento de ventana de la ventana que tiene el foco de teclado recibe mensajes de pulsación de tecla cuando el usuario escribe en el teclado.</span><span class="sxs-lookup"><span data-stu-id="a1715-120">The window procedure of the window that has the keyboard focus receives keystroke messages when the user types at the keyboard.</span></span> <span data-ttu-id="a1715-121">Los mensajes de pulsación de tecla son [**WM \_ KEYDOWN**](wm-keydown.md), [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)y [**WM \_ SYSKEYUP**](wm-syskeyup.md).</span><span class="sxs-lookup"><span data-stu-id="a1715-121">The keystroke messages are [**WM\_KEYDOWN**](wm-keydown.md), [**WM\_KEYUP**](wm-keyup.md), [**WM\_SYSKEYDOWN**](wm-syskeydown.md), and [**WM\_SYSKEYUP**](wm-syskeyup.md).</span></span> <span data-ttu-id="a1715-122">Un procedimiento de ventana típico no tiene en cuenta todos los mensajes de pulsación de tecla, excepto el **\_ KEYDOWN de WM**.</span><span class="sxs-lookup"><span data-stu-id="a1715-122">A typical window procedure ignores all keystroke messages except **WM\_KEYDOWN**.</span></span> <span data-ttu-id="a1715-123">El sistema envía el mensaje de **\_ KEYDOWN de WM** cuando el usuario presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="a1715-123">The system posts the **WM\_KEYDOWN** message when the user presses a key.</span></span>

<span data-ttu-id="a1715-124">Cuando el procedimiento de ventana recibe el mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) , debe examinar el código de la clave virtual que acompaña al mensaje para determinar cómo procesar la pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="a1715-124">When the window procedure receives the [**WM\_KEYDOWN**](wm-keydown.md) message, it should examine the virtual-key code that accompanies the message to determine how to process the keystroke.</span></span> <span data-ttu-id="a1715-125">El código de la clave virtual está en el parámetro *wParam* del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a1715-125">The virtual-key code is in the message's *wParam* parameter.</span></span> <span data-ttu-id="a1715-126">Normalmente, una aplicación solo procesa las pulsaciones de tecla generadas por las teclas que no son de caracteres, incluidas las teclas de función, las teclas de desplazamiento del cursor y las teclas especiales, como INS, SUPR, Inicio y fin.</span><span class="sxs-lookup"><span data-stu-id="a1715-126">Typically, an application processes only keystrokes generated by noncharacter keys, including the function keys, the cursor movement keys, and the special purpose keys such as INS, DEL, HOME, and END.</span></span>

<span data-ttu-id="a1715-127">En el ejemplo siguiente se muestra el marco de trabajo de procedimientos de ventana que utiliza una aplicación típica para recibir y procesar mensajes de pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="a1715-127">The following example shows the window procedure framework that a typical application uses to receive and process keystroke messages.</span></span>


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



## <a name="translating-character-messages"></a><span data-ttu-id="a1715-128">Traducir mensajes de caracteres</span><span class="sxs-lookup"><span data-stu-id="a1715-128">Translating Character Messages</span></span>

<span data-ttu-id="a1715-129">Cualquier subproceso que reciba la entrada de caracteres del usuario debe incluir la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) en su bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a1715-129">Any thread that receives character input from the user must include the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function in its message loop.</span></span> <span data-ttu-id="a1715-130">Esta función examina el código de tecla virtual de un mensaje de pulsación de teclas y, si el código corresponde a un carácter, coloca un mensaje de carácter en la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a1715-130">This function examines the virtual-key code of a keystroke message and, if the code corresponds to a character, places a character message into the message queue.</span></span> <span data-ttu-id="a1715-131">El mensaje de carácter se quita y se envía en la siguiente iteración del bucle de mensajes; el parámetro *wParam* del mensaje contiene el código de carácter.</span><span class="sxs-lookup"><span data-stu-id="a1715-131">The character message is removed and dispatched on the next iteration of the message loop; the *wParam* parameter of the message contains the character code.</span></span>

<span data-ttu-id="a1715-132">En general, el bucle de mensajes de un subproceso debe utilizar la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para traducir todos los mensajes, no solo los mensajes de clave virtual.</span><span class="sxs-lookup"><span data-stu-id="a1715-132">In general, a thread's message loop should use the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function to translate every message, not just virtual-key messages.</span></span> <span data-ttu-id="a1715-133">Aunque **TranslateMessage** no tiene ningún efecto en otros tipos de mensajes, garantiza que la entrada del teclado se traduzca correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1715-133">Although **TranslateMessage** has no effect on other types of messages, it guarantees that keyboard input is translated correctly.</span></span> <span data-ttu-id="a1715-134">En el ejemplo siguiente se muestra cómo incluir la función **TranslateMessage** en un bucle de mensajes de subprocesos típico.</span><span class="sxs-lookup"><span data-stu-id="a1715-134">The following example shows how to include the **TranslateMessage** function in a typical thread message loop.</span></span>


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



## <a name="processing-character-messages"></a><span data-ttu-id="a1715-135">Procesamiento de mensajes de caracteres</span><span class="sxs-lookup"><span data-stu-id="a1715-135">Processing Character Messages</span></span>

<span data-ttu-id="a1715-136">Un procedimiento de ventana recibe un mensaje de carácter cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un código de tecla virtual correspondiente a una tecla de carácter.</span><span class="sxs-lookup"><span data-stu-id="a1715-136">A window procedure receives a character message when the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function translates a virtual-key code corresponding to a character key.</span></span> <span data-ttu-id="a1715-137">Los mensajes de caracteres [**son \_ WM char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)y [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md).</span><span class="sxs-lookup"><span data-stu-id="a1715-137">The character messages are [**WM\_CHAR**](wm-char.md), [**WM\_DEADCHAR**](wm-deadchar.md), [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar), and [**WM\_SYSDEADCHAR**](wm-sysdeadchar.md).</span></span> <span data-ttu-id="a1715-138">Un procedimiento de ventana típico omite todos los mensajes de caracteres excepto **WM \_ Char**.</span><span class="sxs-lookup"><span data-stu-id="a1715-138">A typical window procedure ignores all character messages except **WM\_CHAR**.</span></span> <span data-ttu-id="a1715-139">La función **TranslateMessage** genera un mensaje de **WM \_ Char** cuando el usuario presiona cualquiera de las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1715-139">The **TranslateMessage** function generates a **WM\_CHAR** message when the user presses any of the following keys:</span></span>

-   <span data-ttu-id="a1715-140">Cualquier clave de carácter</span><span class="sxs-lookup"><span data-stu-id="a1715-140">Any character key</span></span>
-   <span data-ttu-id="a1715-141">RETROCESO</span><span class="sxs-lookup"><span data-stu-id="a1715-141">BACKSPACE</span></span>
-   <span data-ttu-id="a1715-142">ENTRAR (retorno de carro)</span><span class="sxs-lookup"><span data-stu-id="a1715-142">ENTER (carriage return)</span></span>
-   <span data-ttu-id="a1715-143">ESC</span><span class="sxs-lookup"><span data-stu-id="a1715-143">ESC</span></span>
-   <span data-ttu-id="a1715-144">Mayús + entrar (avance de la alimentación)</span><span class="sxs-lookup"><span data-stu-id="a1715-144">SHIFT+ENTER (linefeed)</span></span>
-   <span data-ttu-id="a1715-145">TAB</span><span class="sxs-lookup"><span data-stu-id="a1715-145">TAB</span></span>

<span data-ttu-id="a1715-146">Cuando un procedimiento de ventana recibe el mensaje de carácter de [**WM \_**](wm-char.md) , debe examinar el código de carácter que acompaña al mensaje para determinar cómo procesar el carácter.</span><span class="sxs-lookup"><span data-stu-id="a1715-146">When a window procedure receives the [**WM\_CHAR**](wm-char.md) message, it should examine the character code that accompanies the message to determine how to process the character.</span></span> <span data-ttu-id="a1715-147">El código de carácter se encuentra en el parámetro *wParam* del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a1715-147">The character code is in the message's *wParam* parameter.</span></span>

<span data-ttu-id="a1715-148">En el ejemplo siguiente se muestra el marco de trabajo de procedimientos de ventana que utiliza una aplicación típica para recibir y procesar mensajes de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1715-148">The following example shows the window procedure framework that a typical application uses to receive and process character messages.</span></span>


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



## <a name="using-the-caret"></a><span data-ttu-id="a1715-149">Usar el símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="a1715-149">Using the Caret</span></span>

<span data-ttu-id="a1715-150">Una ventana que recibe la entrada del teclado normalmente muestra los caracteres que el usuario escribe en el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a1715-150">A window that receives keyboard input typically displays the characters the user types in the window's client area.</span></span> <span data-ttu-id="a1715-151">Una ventana debe usar un símbolo de intercalación para indicar la posición en el área cliente donde aparecerá el carácter siguiente.</span><span class="sxs-lookup"><span data-stu-id="a1715-151">A window should use a caret to indicate the position in the client area where the next character will appear.</span></span> <span data-ttu-id="a1715-152">La ventana también debe crear y mostrar el símbolo de intercalación cuando recibe el foco de teclado y ocultar y destruir el símbolo de intercalación cuando pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="a1715-152">The window should also create and display the caret when it receives the keyboard focus, and hide and destroy the caret when it loses the focus.</span></span> <span data-ttu-id="a1715-153">Una ventana puede realizar estas operaciones en el procesamiento de los mensajes de [**WM \_ SETFOCUS**](wm-setfocus.md) y [**WM \_ KILLFOCUS**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="a1715-153">A window can perform these operations in the processing of the [**WM\_SETFOCUS**](wm-setfocus.md) and [**WM\_KILLFOCUS**](wm-killfocus.md) messages.</span></span> <span data-ttu-id="a1715-154">Para obtener más información sobre las intercalaciones, consulte [Cares](/windows/desktop/menurc/carets).</span><span class="sxs-lookup"><span data-stu-id="a1715-154">For more information about carets, see [Carets](/windows/desktop/menurc/carets).</span></span>

## <a name="displaying-keyboard-input"></a><span data-ttu-id="a1715-155">Mostrar la entrada del teclado</span><span class="sxs-lookup"><span data-stu-id="a1715-155">Displaying Keyboard Input</span></span>

<span data-ttu-id="a1715-156">En el ejemplo de esta sección se muestra cómo una aplicación puede recibir caracteres del teclado, mostrarlos en el área de cliente de una ventana y actualizar la posición del símbolo de intercalación con cada carácter escrito.</span><span class="sxs-lookup"><span data-stu-id="a1715-156">The example in this section shows how an application can receive characters from the keyboard, display them in the client area of a window, and update the position of the caret with each character typed.</span></span> <span data-ttu-id="a1715-157">También muestra cómo mover el símbolo de intercalación en respuesta a la flecha izquierda, flecha derecha, Inicio y FINALización de las pulsaciones de teclas y muestra cómo resaltar el texto seleccionado en respuesta a la combinación de teclas Mayús + Flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="a1715-157">It also demonstrates how to move the caret in response to the LEFT ARROW, RIGHT ARROW, HOME, and END keystrokes, and shows how to highlight selected text in response to the SHIFT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="a1715-158">Durante el procesamiento del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) , el procedimiento de ventana que se muestra en el ejemplo asigna un búfer de 64k para almacenar la entrada del teclado.</span><span class="sxs-lookup"><span data-stu-id="a1715-158">During processing of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure shown in the example allocates a 64K buffer for storing keyboard input.</span></span> <span data-ttu-id="a1715-159">También recupera las métricas de la fuente cargada actualmente, guardando el alto y el ancho medio de los caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="a1715-159">It also retrieves the metrics of the currently loaded font, saving the height and average width of characters in the font.</span></span> <span data-ttu-id="a1715-160">El alto y el ancho se utilizan en el procesamiento del mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) para calcular la longitud de línea y el número máximo de líneas, en función del tamaño del área cliente.</span><span class="sxs-lookup"><span data-stu-id="a1715-160">The height and width are used in processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to calculate the line length and maximum number of lines, based on the size of the client area.</span></span>

<span data-ttu-id="a1715-161">El procedimiento de ventana crea y muestra el símbolo de intercalación al procesar el mensaje de [**\_ SETFOCUS de WM**](wm-setfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="a1715-161">The window procedure creates and displays the caret when processing the [**WM\_SETFOCUS**](wm-setfocus.md) message.</span></span> <span data-ttu-id="a1715-162">Oculta y elimina el símbolo de intercalación al procesar el mensaje de [**\_ KILLFOCUS de WM**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="a1715-162">It hides and deletes the caret when processing the [**WM\_KILLFOCUS**](wm-killfocus.md) message.</span></span>

<span data-ttu-id="a1715-163">Al procesar el mensaje de tipo de datos de [**WM \_**](wm-char.md) , el procedimiento de ventana muestra caracteres, los almacena en el búfer de entrada y actualiza la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a1715-163">When processing the [**WM\_CHAR**](wm-char.md) message, the window procedure displays characters, stores them in the input buffer, and updates the caret position.</span></span> <span data-ttu-id="a1715-164">El procedimiento de ventana también convierte los caracteres de tabulación en cuatro caracteres de espacio consecutivos.</span><span class="sxs-lookup"><span data-stu-id="a1715-164">The window procedure also converts tab characters to four consecutive space characters.</span></span> <span data-ttu-id="a1715-165">Los caracteres de retroceso, avance y salida generan un pitido, pero no se procesan de otra manera.</span><span class="sxs-lookup"><span data-stu-id="a1715-165">Backspace, linefeed, and escape characters generate a beep, but are not otherwise processed.</span></span>

<span data-ttu-id="a1715-166">El procedimiento de ventana realiza los movimientos de intercalación izquierda, derecha, final y inicio al procesar el mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="a1715-166">The window procedure performs the left, right, end, and home caret movements when processing the [**WM\_KEYDOWN**](wm-keydown.md) message.</span></span> <span data-ttu-id="a1715-167">Al procesar la acción de la tecla de dirección derecha, el procedimiento de ventana comprueba el estado de la tecla Mayús y, si está inactivo, selecciona el carácter situado a la derecha del símbolo de intercalación mientras se mueve el símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a1715-167">While processing the action of the RIGHT ARROW key, the window procedure checks the state of the SHIFT key and, if it is down, selects the character to the right of the caret as the caret is moved.</span></span>

<span data-ttu-id="a1715-168">Tenga en cuenta que el código siguiente se escribe para que se pueda compilar como Unicode o como ANSI.</span><span class="sxs-lookup"><span data-stu-id="a1715-168">Note that the following code is written so that it can be compiled either as Unicode or as ANSI.</span></span> <span data-ttu-id="a1715-169">Si el código fuente define Unicode, las cadenas se administran como caracteres Unicode; de lo contrario, se tratan como caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="a1715-169">If the source code defines UNICODE, strings are handled as Unicode characters; otherwise, they are handled as ANSI characters.</span></span>


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



 

 