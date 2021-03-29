---
title: Usar la entrada del mouse
description: En esta sección se describen las tareas asociadas a la entrada del mouse.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- entrada del usuario, entrada del mouse
- capturar datos proporcionados por el usuario, entrada del mouse
- entrada del mouse
- cursores, entrada del mouse
- cursor del mouse
- hacer doble clic en procesamiento de mensajes
- rueda del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b34f180aad6aec6120bf4e3ffa997eba13e760
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358910"
---
# <a name="using-mouse-input"></a><span data-ttu-id="b52de-110">Usar la entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-110">Using Mouse Input</span></span>

<span data-ttu-id="b52de-111">En esta sección se describen las tareas asociadas a la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-111">This section covers tasks associated with mouse input.</span></span>

-   [<span data-ttu-id="b52de-112">Seguimiento del cursor del mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-112">Tracking the Mouse Cursor</span></span>](#tracking-the-mouse-cursor)
-   [<span data-ttu-id="b52de-113">Dibujar líneas con el mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-113">Drawing Lines with the Mouse</span></span>](#drawing-lines-with-the-mouse)
-   [<span data-ttu-id="b52de-114">Procesamiento de un mensaje de doble clic</span><span class="sxs-lookup"><span data-stu-id="b52de-114">Processing a Double Click Message</span></span>](#processing-a-double-click-message)
-   [<span data-ttu-id="b52de-115">Seleccionar una línea de texto</span><span class="sxs-lookup"><span data-stu-id="b52de-115">Selecting a Line of Text</span></span>](#selecting-a-line-of-text)
-   [<span data-ttu-id="b52de-116">Usar una rueda del mouse en un documento con objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="b52de-116">Using a Mouse Wheel in a Document with Embedded Objects</span></span>](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [<span data-ttu-id="b52de-117">Recuperar el número de líneas de desplazamiento de la rueda del mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-117">Retrieving the Number of Mouse Wheel Scroll Lines</span></span>](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a><span data-ttu-id="b52de-118">Seguimiento del cursor del mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-118">Tracking the Mouse Cursor</span></span>

<span data-ttu-id="b52de-119">Las aplicaciones suelen realizar tareas que implican el seguimiento de la posición del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-119">Applications often perform tasks that involve tracking the position of the mouse cursor.</span></span> <span data-ttu-id="b52de-120">La mayoría de las aplicaciones de dibujo, por ejemplo, hacen un seguimiento de la posición del cursor del mouse durante las operaciones de dibujo, lo que permite al usuario dibujar en el área de cliente de una ventana arrastrando el mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-120">Most drawing applications, for example, track the position of the mouse cursor during drawing operations, allowing the user to draw in a window's client area by dragging the mouse.</span></span> <span data-ttu-id="b52de-121">Las aplicaciones de procesamiento de texto también realizan el seguimiento del cursor, lo que permite al usuario seleccionar una palabra o un bloque de texto haciendo clic y arrastrando el mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-121">Word-processing applications also track the cursor, enabling the user to select a word or block of text by clicking and dragging the mouse.</span></span>

<span data-ttu-id="b52de-122">El seguimiento del cursor normalmente implica el procesamiento de los mensajes de [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)y [**WM \_ LBUTTONUP**](wm-lbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="b52de-122">Tracking the cursor typically involves processing the [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_MOUSEMOVE**](wm-mousemove.md), and [**WM\_LBUTTONUP**](wm-lbuttonup.md) messages.</span></span> <span data-ttu-id="b52de-123">Una ventana determina cuándo debe comenzar el seguimiento del cursor comprobando la posición del cursor proporcionada en el parámetro *lParam* del mensaje de **\_ LBUTTONDOWN de WM** .</span><span class="sxs-lookup"><span data-stu-id="b52de-123">A window determines when to begin tracking the cursor by checking the cursor position provided in the *lParam* parameter of the **WM\_LBUTTONDOWN** message.</span></span> <span data-ttu-id="b52de-124">Por ejemplo, una aplicación de procesamiento de texto comenzaría a realizar el seguimiento del cursor solo si el mensaje de **\_ LBUTTONDOWN de WM** se produjera mientras el cursor estaba en una línea de texto, pero no si estuviera más allá del final del documento.</span><span class="sxs-lookup"><span data-stu-id="b52de-124">For example, a word-processing application would begin tracking the cursor only if the **WM\_LBUTTONDOWN** message occurred while the cursor was on a line of text, but not if it was past the end of the document.</span></span>

<span data-ttu-id="b52de-125">Una ventana realiza un seguimiento de la posición del cursor mediante el procesamiento de la secuencia de mensajes de la [**\_ MOUSEMOVE de WM**](wm-mousemove.md) enviados a la ventana a medida que se mueve el mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-125">A window tracks the position of the cursor by processing the stream of [**WM\_MOUSEMOVE**](wm-mousemove.md) messages posted to the window as the mouse moves.</span></span> <span data-ttu-id="b52de-126">El procesamiento del mensaje de **\_ MOUSEMOVE de WM** normalmente implica una operación de dibujo o dibujo repetitivo en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="b52de-126">Processing the **WM\_MOUSEMOVE** message typically involves a repetitive painting or drawing operation in the client area.</span></span> <span data-ttu-id="b52de-127">Por ejemplo, una aplicación de dibujo podría volver a dibujar una línea varias veces mientras se mueve el mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-127">For example, a drawing application might redraw a line repeatedly as the mouse moves.</span></span> <span data-ttu-id="b52de-128">Una ventana usa el mensaje de [**\_ LBUTTONUP de WM**](wm-lbuttonup.md) como una señal para detener el seguimiento del cursor.</span><span class="sxs-lookup"><span data-stu-id="b52de-128">A window uses the [**WM\_LBUTTONUP**](wm-lbuttonup.md) message as a signal to stop tracking the cursor.</span></span>

<span data-ttu-id="b52de-129">Además, una aplicación puede llamar a la función [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que el sistema envíe otros mensajes que son útiles para realizar el seguimiento del cursor.</span><span class="sxs-lookup"><span data-stu-id="b52de-129">In addition, an application can call the [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) function to have the system send other messages that are useful for tracking the cursor.</span></span> <span data-ttu-id="b52de-130">El sistema envía el mensaje de [**\_ MOUSEHOVER de WM**](wm-mousehover.md) cuando el cursor se mantiene sobre el área de cliente durante un período de tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="b52de-130">The system posts the [**WM\_MOUSEHOVER**](wm-mousehover.md) message when the cursor hovers over the client area for a certain time period.</span></span> <span data-ttu-id="b52de-131">Envía el mensaje de [**WM \_ MOUSELEAVE**](wm-mouseleave.md) cuando el cursor sale del área cliente.</span><span class="sxs-lookup"><span data-stu-id="b52de-131">It posts the [**WM\_MOUSELEAVE**](wm-mouseleave.md) message when the cursor leaves the client area.</span></span> <span data-ttu-id="b52de-132">Los mensajes de [**WM \_ NCMOUSEHOVER**](wm-ncmousehover.md) y [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md) son los mensajes correspondientes para las áreas no cliente.</span><span class="sxs-lookup"><span data-stu-id="b52de-132">The [**WM\_NCMOUSEHOVER**](wm-ncmousehover.md) and [**WM\_NCMOUSELEAVE**](wm-ncmouseleave.md) messages are the corresponding messages for the nonclient areas.</span></span>

## <a name="drawing-lines-with-the-mouse"></a><span data-ttu-id="b52de-133">Dibujar líneas con el mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-133">Drawing Lines with the Mouse</span></span>

<span data-ttu-id="b52de-134">En el ejemplo de esta sección se muestra cómo realizar el seguimiento del cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-134">The example in this section demonstrates how to track the mouse cursor.</span></span> <span data-ttu-id="b52de-135">Contiene partes de un procedimiento de ventana que permiten al usuario dibujar líneas en el área de cliente de una ventana arrastrando el mouse.</span><span class="sxs-lookup"><span data-stu-id="b52de-135">It contains portions of a window procedure that enables the user to draw lines in a window's client area by dragging the mouse.</span></span>

<span data-ttu-id="b52de-136">Cuando el procedimiento de ventana recibe un mensaje de [**\_ LBUTTONDOWN de WM**](wm-lbuttondown.md) , captura el mouse y guarda las coordenadas del cursor, usando las coordenadas como el punto inicial de la línea.</span><span class="sxs-lookup"><span data-stu-id="b52de-136">When the window procedure receives a [**WM\_LBUTTONDOWN**](wm-lbuttondown.md) message, it captures the mouse and saves the coordinates of the cursor, using the coordinates as the starting point of the line.</span></span> <span data-ttu-id="b52de-137">También utiliza la función [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) para limitar el cursor al área cliente durante la operación de dibujo de línea.</span><span class="sxs-lookup"><span data-stu-id="b52de-137">It also uses the [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function to confine the cursor to the client area during the line drawing operation.</span></span>

<span data-ttu-id="b52de-138">Durante el primer mensaje de Windows de [**WM \_**](wm-mousemove.md) , el procedimiento de ventana dibuja una línea desde el punto inicial hasta la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="b52de-138">During the first [**WM\_MOUSEMOVE**](wm-mousemove.md) message, the window procedure draws a line from the starting point to the current position of the cursor.</span></span> <span data-ttu-id="b52de-139">Durante los mensajes del **\_ MOUSEMOVE de WM** posteriores, el procedimiento de ventana borra la línea anterior dibujando sobre ella con un color de lápiz invertido.</span><span class="sxs-lookup"><span data-stu-id="b52de-139">During subsequent **WM\_MOUSEMOVE** messages, the window procedure erases the previous line by drawing over it with an inverted pen color.</span></span> <span data-ttu-id="b52de-140">A continuación, dibuja una nueva línea desde el punto inicial hasta la nueva posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="b52de-140">Then it draws a new line from the starting point to the new position of the cursor.</span></span>

<span data-ttu-id="b52de-141">El mensaje de [**\_ LBUTTONUP de WM**](wm-lbuttonup.md) señala el final de la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b52de-141">The [**WM\_LBUTTONUP**](wm-lbuttonup.md) message signals the end of the drawing operation.</span></span> <span data-ttu-id="b52de-142">El procedimiento de ventana libera la captura del mouse y libera el mouse desde el área cliente.</span><span class="sxs-lookup"><span data-stu-id="b52de-142">The window procedure releases the mouse capture and frees the mouse from the client area.</span></span>


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



## <a name="processing-a-double-click-message"></a><span data-ttu-id="b52de-143">Procesamiento de un mensaje de doble clic</span><span class="sxs-lookup"><span data-stu-id="b52de-143">Processing a Double Click Message</span></span>

<span data-ttu-id="b52de-144">Para recibir mensajes de doble clic, una ventana debe pertenecer a una clase de ventana que tenga el estilo de clase [**CS \_ DBLCLKS**](/windows/desktop/winmsg/about-window-classes) .</span><span class="sxs-lookup"><span data-stu-id="b52de-144">To receive double-click messages, a window must belong to a window class that has the [**CS\_DBLCLKS**](/windows/desktop/winmsg/about-window-classes) class style.</span></span> <span data-ttu-id="b52de-145">Este estilo se establece al registrar la clase de ventana, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b52de-145">You set this style when registering the window class, as shown in the following example.</span></span>


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



<span data-ttu-id="b52de-146">Un mensaje de doble clic siempre va precedido de un mensaje de botón presionado.</span><span class="sxs-lookup"><span data-stu-id="b52de-146">A double-click message is always preceded by a button-down message.</span></span> <span data-ttu-id="b52de-147">Por este motivo, las aplicaciones suelen usar un mensaje de doble clic para extender una tarea que comenzó durante un mensaje de botón.</span><span class="sxs-lookup"><span data-stu-id="b52de-147">For this reason, applications typically use a double-click message to extend a task that it began during a button-down message.</span></span>

## <a name="selecting-a-line-of-text"></a><span data-ttu-id="b52de-148">Seleccionar una línea de texto</span><span class="sxs-lookup"><span data-stu-id="b52de-148">Selecting a Line of Text</span></span>

<span data-ttu-id="b52de-149">El ejemplo de esta sección se toma de una sencilla aplicación de procesamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="b52de-149">The example in this section is taken from a simple word-processing application.</span></span> <span data-ttu-id="b52de-150">Incluye código que permite al usuario establecer la posición del símbolo de intercalación haciendo clic en cualquier parte de una línea de texto y seleccionando (resaltando) una línea de texto haciendo doble clic en cualquier parte de la línea.</span><span class="sxs-lookup"><span data-stu-id="b52de-150">It includes code that enables the user to set the position of the caret by clicking anywhere on a line of text, and to select (highlight) a line of text by double-clicking anywhere on the line.</span></span>


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



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a><span data-ttu-id="b52de-151">Usar una rueda del mouse en un documento con objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="b52de-151">Using a Mouse Wheel in a Document with Embedded Objects</span></span>

<span data-ttu-id="b52de-152">En este ejemplo se da por supuesto que es un documento de Microsoft Word con varios objetos incrustados:</span><span class="sxs-lookup"><span data-stu-id="b52de-152">This example assumes a Microsoft Word document with various embedded objects:</span></span>

-   <span data-ttu-id="b52de-153">Una hoja de cálculo de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="b52de-153">A Microsoft Excel spreadsheet</span></span>
-   <span data-ttu-id="b52de-154">Un control de cuadro de lista incrustado que se desplaza en respuesta a la rueda</span><span class="sxs-lookup"><span data-stu-id="b52de-154">An embedded list box control that scrolls in response to the wheel</span></span>
-   <span data-ttu-id="b52de-155">Un control de cuadro de texto incrustado que no responde a la rueda</span><span class="sxs-lookup"><span data-stu-id="b52de-155">An embedded text box control that does not respond to the wheel</span></span>

<span data-ttu-id="b52de-156">El mensaje [MSH \_ MOUSEWHEEL](about-mouse-input.md) siempre se envía a la ventana principal de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b52de-156">The [MSH\_MOUSEWHEEL](about-mouse-input.md) message is always sent to the main window in Microsoft Word.</span></span> <span data-ttu-id="b52de-157">Esto es así incluso si la hoja de cálculo incrustada está activa.</span><span class="sxs-lookup"><span data-stu-id="b52de-157">This is true even if the embedded spreadsheet is active.</span></span> <span data-ttu-id="b52de-158">En la tabla siguiente se explica cómo \_ se controla el mensaje de MSH MOUSEWHEEL según el foco.</span><span class="sxs-lookup"><span data-stu-id="b52de-158">The following table explains how the MSH\_MOUSEWHEEL message is handled according to the focus.</span></span>



| <span data-ttu-id="b52de-159">El foco está activado</span><span class="sxs-lookup"><span data-stu-id="b52de-159">Focus is on</span></span>                | <span data-ttu-id="b52de-160">El control es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b52de-160">Handling is as follows</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52de-161">Documento de Word</span><span class="sxs-lookup"><span data-stu-id="b52de-161">Word document</span></span>              | <span data-ttu-id="b52de-162">Word desplaza la ventana de documento.</span><span class="sxs-lookup"><span data-stu-id="b52de-162">Word scrolls the document window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b52de-163">Hoja de cálculo de Excel incrustada</span><span class="sxs-lookup"><span data-stu-id="b52de-163">Embedded Excel spreadsheet</span></span> | <span data-ttu-id="b52de-164">Word envía el mensaje a Excel.</span><span class="sxs-lookup"><span data-stu-id="b52de-164">Word posts the message to Excel.</span></span> <span data-ttu-id="b52de-165">Debe decidir si la aplicación incrustada debe responder al mensaje o no.</span><span class="sxs-lookup"><span data-stu-id="b52de-165">You must decide if the embedded application should respond to the message or not.</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b52de-166">Control incrustado</span><span class="sxs-lookup"><span data-stu-id="b52de-166">Embedded control</span></span>           | <span data-ttu-id="b52de-167">Depende de la aplicación enviar el mensaje a un control incrustado que tenga el foco y comprobar el código de retorno para ver si el control lo ha controlado.</span><span class="sxs-lookup"><span data-stu-id="b52de-167">It is up to the application to send the message to an embedded control that has the focus and check the return code to see if the control handled it.</span></span> <span data-ttu-id="b52de-168">Si el control no lo controla, la aplicación debe desplazarse por la ventana de documento.</span><span class="sxs-lookup"><span data-stu-id="b52de-168">If the control did not handle it, then the application should scroll the document window.</span></span> <span data-ttu-id="b52de-169">Por ejemplo, si el usuario hizo clic en un cuadro de lista y, a continuación, revirtió la rueda, ese control se desplazaría en respuesta a un giro de la rueda.</span><span class="sxs-lookup"><span data-stu-id="b52de-169">For example, if the user clicked a list box and then rolled the wheel, that control would scroll in response to a wheel rotation.</span></span> <span data-ttu-id="b52de-170">Si el usuario hizo clic en un cuadro de texto y luego girara la rueda, se desplazaría todo el documento.</span><span class="sxs-lookup"><span data-stu-id="b52de-170">If the user clicked a text box and then rotated the wheel, the whole document would scroll.</span></span> |



 

<span data-ttu-id="b52de-171">En el ejemplo siguiente se muestra cómo una aplicación podría controlar los dos mensajes de la rueda.</span><span class="sxs-lookup"><span data-stu-id="b52de-171">This following example shows how an application might handle the two wheel messages.</span></span>


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



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a><span data-ttu-id="b52de-172">Recuperar el número de líneas de desplazamiento de la rueda del mouse</span><span class="sxs-lookup"><span data-stu-id="b52de-172">Retrieving the Number of Mouse Wheel Scroll Lines</span></span>

<span data-ttu-id="b52de-173">El código siguiente permite que una aplicación recupere el número de líneas de desplazamiento mediante la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b52de-173">The following code allows an application to retrieve the number of scroll lines using the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>


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



 

 