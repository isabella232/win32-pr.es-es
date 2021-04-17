---
title: Usar el portapapeles
description: 'Esta sección contiene ejemplos de código para las tareas siguientes:'
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- portapapeles, cortar datos
- portapapeles, copiar datos
- portapapeles, pegar datos
- portapapeles, seleccionar datos
- portapapeles, comandos del menú Edición
- portapapeles, visores
- portapapeles, ventanas del visor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359082"
---
# <a name="using-the-clipboard"></a><span data-ttu-id="9754a-110">Usar el portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-110">Using the Clipboard</span></span>

<span data-ttu-id="9754a-111">Esta sección contiene ejemplos de código para las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9754a-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="9754a-112">Implementar los comandos cortar, copiar y pegar</span><span class="sxs-lookup"><span data-stu-id="9754a-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="9754a-113">Seleccionar datos</span><span class="sxs-lookup"><span data-stu-id="9754a-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="9754a-114">Crear un menú de edición</span><span class="sxs-lookup"><span data-stu-id="9754a-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="9754a-115">Procesar el mensaje de INITMENUPOPUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="9754a-116">Procesar el mensaje de comando de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="9754a-117">Copiar información en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="9754a-118">Pegar información del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="9754a-119">Registrar un formato de Portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="9754a-120">Procesamiento de los \_ mensajes de WM RENDERFORMAT y WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="9754a-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="9754a-121">Procesar el mensaje de DESTROYCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="9754a-122">Usar el formato del portapapeles Owner-Display</span><span class="sxs-lookup"><span data-stu-id="9754a-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="9754a-123">Supervisar el contenido del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="9754a-124">Consultar el número de secuencia del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="9754a-125">Crear un agente de escucha de formato del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="9754a-126">Crear una ventana del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="9754a-127">Agregar una ventana a la cadena del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="9754a-128">Procesar el mensaje de CHANGECBCHAIN de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="9754a-129">Quitar una ventana de la cadena del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="9754a-130">Procesar el mensaje de DRAWCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="9754a-131">Ejemplo de un visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="9754a-132">Implementar los comandos cortar, copiar y pegar</span><span class="sxs-lookup"><span data-stu-id="9754a-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="9754a-133">En esta sección se describe cómo se implementan los comandos estándar de **cortar**, **copiar** y **pegar** en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9754a-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="9754a-134">En el ejemplo de esta sección se usan estos métodos para colocar datos en el Portapapeles con un formato de Portapapeles registrado, el formato de **CF \_ OWNERDISPLAY** y el formato de **\_ texto CF** .</span><span class="sxs-lookup"><span data-stu-id="9754a-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="9754a-135">El formato registrado se usa para representar ventanas de texto rectangulares o elípticas, denominadas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="9754a-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="9754a-136">Seleccionar datos</span><span class="sxs-lookup"><span data-stu-id="9754a-136">Selecting Data</span></span>

<span data-ttu-id="9754a-137">Antes de que se pueda copiar la información en el portapapeles, el usuario debe seleccionar la información específica que se va a copiar o cortar.</span><span class="sxs-lookup"><span data-stu-id="9754a-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="9754a-138">Una aplicación debe proporcionar un medio para que el usuario seleccione información dentro de un documento y algún tipo de comentario visual para indicar los datos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="9754a-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="9754a-139">Crear un menú de edición</span><span class="sxs-lookup"><span data-stu-id="9754a-139">Creating an Edit Menu</span></span>

<span data-ttu-id="9754a-140">Una aplicación debe cargar una tabla de aceleradores que contenga los aceleradores de teclado estándar para los comandos del menú **edición** .</span><span class="sxs-lookup"><span data-stu-id="9754a-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="9754a-141">La función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) debe agregarse al bucle de mensajes de la aplicación para que los aceleradores surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="9754a-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="9754a-142">Para obtener más información acerca de los aceleradores de teclado, consulte [aceleradores de teclado](/windows/desktop/menurc/keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="9754a-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="9754a-143">Procesar el mensaje de INITMENUPOPUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="9754a-144">No todos los comandos del portapapeles están disponibles para el usuario en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="9754a-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="9754a-145">Una aplicación debe procesar el mensaje de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) para habilitar los elementos de menú para los comandos disponibles y deshabilitar los comandos no disponibles.</span><span class="sxs-lookup"><span data-stu-id="9754a-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="9754a-146">A continuación se indica el caso de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) para una aplicación denominada etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9754a-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="9754a-147">La función InitMenu se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="9754a-147">The InitMenu function is defined as follows.</span></span>


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="9754a-148">Procesar el mensaje de comando de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="9754a-149">Para procesar los comandos de menú, agregue el caso de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento de ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9754a-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="9754a-150">A continuación se indica el caso de **\_ comando de WM** para el procedimiento de ventana de la aplicación de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9754a-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



<span data-ttu-id="9754a-151">Para llevar a cabo los comandos de **copiar** y **cortar** , el procedimiento de ventana llama a la función EditCopy definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9754a-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="9754a-152">Para obtener más información, vea [copiar información en el portapapeles](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="9754a-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="9754a-153">Para llevar a cabo el comando **pegar** , el procedimiento de ventana llama a la función EditPaste definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9754a-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="9754a-154">Para obtener más información sobre la función EditPaste, vea [pegar información desde el portapapeles](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="9754a-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="9754a-155">Copiar información en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="9754a-156">En la aplicación de etiqueta, la función EditCopy definida por la aplicación copia la selección actual en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="9754a-157">Esta función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9754a-157">This function does the following:</span></span>

1.  <span data-ttu-id="9754a-158">Abre el portapapeles mediante una llamada a la función [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="9754a-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="9754a-159">Vacía el portapapeles mediante una llamada a la función [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .</span><span class="sxs-lookup"><span data-stu-id="9754a-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="9754a-160">Llama a la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) una vez para cada formato del portapapeles que proporciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9754a-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="9754a-161">Cierra el portapapeles mediante una llamada a la función [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="9754a-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="9754a-162">Dependiendo de la selección actual, la función EditCopy copia un intervalo de texto o copia una estructura definida por la aplicación que representa una etiqueta completa.</span><span class="sxs-lookup"><span data-stu-id="9754a-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="9754a-163">La estructura, denominada LABELBOX, se define como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-163">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="9754a-164">A continuación se encuentra la función EditCopy.</span><span class="sxs-lookup"><span data-stu-id="9754a-164">Following is the EditCopy function.</span></span>


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="9754a-165">Pegar información del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="9754a-166">En la aplicación de etiqueta, la función EditPaste definida por la aplicación pega el contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="9754a-167">Esta función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9754a-167">This function does the following:</span></span>

1.  <span data-ttu-id="9754a-168">Abre el portapapeles mediante una llamada a la función [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="9754a-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="9754a-169">Determina cuál de los formatos disponibles del portapapeles se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9754a-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="9754a-170">Recupera el identificador de los datos en el formato seleccionado mediante una llamada a la función [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="9754a-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="9754a-171">Inserta una copia de los datos en el documento.</span><span class="sxs-lookup"><span data-stu-id="9754a-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="9754a-172">El portapapeles todavía posee el identificador devuelto por [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) , por lo que una aplicación no debe liberarlo ni dejarlo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9754a-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="9754a-173">Cierra el portapapeles mediante una llamada a la función [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="9754a-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="9754a-174">Si se selecciona una etiqueta y contiene un punto de inserción, la función EditPaste inserta el texto del portapapeles en el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="9754a-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="9754a-175">Si no hay ninguna selección o si se selecciona una etiqueta, la función crea una etiqueta nueva, usando la estructura LABELBOX definida por la aplicación en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="9754a-176">La estructura LABELBOX se coloca en el portapapeles mediante el uso de un formato de Portapapeles registrado.</span><span class="sxs-lookup"><span data-stu-id="9754a-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="9754a-177">La estructura, denominada LABELBOX, se define como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-177">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="9754a-178">A continuación se encuentra la función EditPaste.</span><span class="sxs-lookup"><span data-stu-id="9754a-178">Following is the EditPaste function.</span></span>


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="9754a-179">Registrar un formato de Portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="9754a-180">Para registrar un formato del portapapeles, agregue una llamada a la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) a la función de inicialización de instancia de la aplicación, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="9754a-181">Procesamiento de los \_ mensajes de WM RENDERFORMAT y WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="9754a-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="9754a-182">Si una ventana pasa un identificador **null** a la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , debe procesar los mensajes de [**WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) para representar los datos a petición.</span><span class="sxs-lookup"><span data-stu-id="9754a-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="9754a-183">Si una ventana retrasa la representación de un formato específico y, a continuación, otra aplicación solicita datos en ese formato, se envía un mensaje de [**\_ RENDERFORMAT de WM**](wm-renderformat.md) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="9754a-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="9754a-184">Además, si una ventana retrasa la representación de uno o más formatos y alguno de esos formatos permanece sin procesar cuando la ventana está a punto de ser destruida, se envía un mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) a la ventana antes de su destrucción.</span><span class="sxs-lookup"><span data-stu-id="9754a-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="9754a-185">Para representar un formato del portapapeles, el procedimiento de ventana debe colocar un identificador de datos no **null** en el portapapeles mediante la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="9754a-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="9754a-186">Si el procedimiento de ventana está representando un formato en respuesta al mensaje de [**\_ RENDERFORMAT de WM**](wm-renderformat.md) , no debe abrir el portapapeles antes de llamar a **SetClipboardData**.</span><span class="sxs-lookup"><span data-stu-id="9754a-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="9754a-187">Pero si se representan uno o varios formatos en respuesta al mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) , debe abrir el portapapeles y comprobar que la ventana sigue siendo propietaria del portapapeles antes de llamar a **SetClipboardData** y debe cerrar el portapapeles antes de volver.</span><span class="sxs-lookup"><span data-stu-id="9754a-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="9754a-188">La aplicación de etiqueta procesa los mensajes de [**WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



<span data-ttu-id="9754a-189">En ambos casos, el procedimiento de ventana llama a la función RenderFormat definida por la aplicación, que se define de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="9754a-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="9754a-190">La estructura, denominada LABELBOX, se define como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-190">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="9754a-191">Procesar el mensaje de DESTROYCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="9754a-192">Una ventana puede procesar el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) para liberar los recursos que se han reservado para admitir la representación diferida.</span><span class="sxs-lookup"><span data-stu-id="9754a-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="9754a-193">Por ejemplo, la aplicación de etiqueta, al copiar una etiqueta en el portapapeles, asigna un objeto de memoria local.</span><span class="sxs-lookup"><span data-stu-id="9754a-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="9754a-194">A continuación, libera este objeto como respuesta al mensaje **de \_ DESTROYCLIPBOARD de WM** , como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="9754a-195">Usar el formato del portapapeles Owner-Display</span><span class="sxs-lookup"><span data-stu-id="9754a-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="9754a-196">Si una ventana coloca información en el portapapeles mediante el formato de Portapapeles de **CF \_ OWNERDISPLAY** , debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9754a-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="9754a-197">Procese el mensaje de [**\_ PAINTCLIPBOARD de WM**](wm-paintclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="9754a-198">Este mensaje se envía al propietario del portapapeles cuando se debe volver a dibujar una parte de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="9754a-199">Procese el mensaje de [**\_ SIZECLIPBOARD de WM**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="9754a-200">Este mensaje se envía al propietario del portapapeles cuando se ha cambiado el tamaño de la ventana del visor del portapapeles o se ha modificado su contenido.</span><span class="sxs-lookup"><span data-stu-id="9754a-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="9754a-201">Normalmente, una ventana responde a este mensaje estableciendo las posiciones y los intervalos de desplazamiento de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="9754a-202">En respuesta a este mensaje, la aplicación de etiqueta también actualiza una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) para la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="9754a-203">Procese los mensajes de [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) y [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="9754a-204">Estos mensajes se envían al propietario del portapapeles cuando se produce un evento de barra de desplazamiento en la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="9754a-205">Procese el mensaje de [**\_ ASKCBFORMATNAME de WM**](wm-askcbformatname.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="9754a-206">La ventana Visor del portapapeles envía este mensaje a una aplicación para recuperar el nombre del formato de presentación del propietario.</span><span class="sxs-lookup"><span data-stu-id="9754a-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="9754a-207">El procedimiento de ventana de la aplicación de etiqueta procesa estos mensajes, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9754a-207">The window procedure for the Label application processes these messages, as follows.</span></span>


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="9754a-208">Supervisar el contenido del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="9754a-209">Hay tres formas de supervisar los cambios en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="9754a-210">El método más antiguo es crear una ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="9754a-211">Windows 2000 agregó la capacidad de consultar el número de secuencia del portapapeles y Windows Vista agregó compatibilidad con los agentes de escucha de formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="9754a-212">Las ventanas del visor del portapapeles se admiten por compatibilidad con versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="9754a-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="9754a-213">Los nuevos programas deben usar agentes de escucha de formato del portapapeles o el número de secuencia del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="9754a-214">Consultar el número de secuencia del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="9754a-215">Cada vez que cambia el contenido del portapapeles, se incrementa un valor de 32 bits conocido como el número de secuencia del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="9754a-216">Un programa puede recuperar el número de secuencia del portapapeles actual llamando a la función [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .</span><span class="sxs-lookup"><span data-stu-id="9754a-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="9754a-217">Al comparar el valor devuelto con un valor devuelto por una llamada anterior a **GetClipboardSequenceNumber**, un programa puede determinar si el contenido del portapapeles ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9754a-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="9754a-218">Este método es más adecuado para los programas que almacenan en caché los resultados en función del contenido actual del portapapeles y necesitan saber si los cálculos siguen siendo válidos antes de usar los resultados de esa caché.</span><span class="sxs-lookup"><span data-stu-id="9754a-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="9754a-219">Tenga en cuenta que este no es un método de notificación y no debe usarse en un bucle de sondeo.</span><span class="sxs-lookup"><span data-stu-id="9754a-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="9754a-220">Para recibir una notificación cuando cambie el contenido del portapapeles, utilice un agente de escucha de formato del portapapeles o un visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="9754a-221">Crear un agente de escucha de formato del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="9754a-222">Un agente de escucha de formato del portapapeles es una ventana que se ha registrado para recibir notificaciones cuando cambia el contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="9754a-223">Este método se recomienda para crear una ventana del visor del portapapeles porque es más fácil de implementar y evitar problemas si los programas no mantienen correctamente la cadena del visor del portapapeles o si una ventana de la cadena del visor del portapapeles deja de responder a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="9754a-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="9754a-224">Una ventana se registra como un agente de escucha de formato del portapapeles mediante una llamada a la función [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="9754a-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="9754a-225">Cuando cambia el contenido del portapapeles, se envía un mensaje de [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="9754a-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="9754a-226">El registro sigue siendo válido hasta que la ventana se anula el registro mediante una llamada a la función [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="9754a-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="9754a-227">Crear una ventana del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="9754a-228">Una ventana del visor del portapapeles muestra el contenido actual del portapapeles y recibe mensajes cuando cambia el contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="9754a-229">Para crear una ventana del visor del portapapeles, la aplicación debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9754a-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="9754a-230">Agregue la ventana a la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="9754a-231">Procese el mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="9754a-232">Procese el mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="9754a-233">Quite la ventana de la cadena del visor del portapapeles antes de que se destruya.</span><span class="sxs-lookup"><span data-stu-id="9754a-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="9754a-234">Agregar una ventana a la cadena del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="9754a-235">Una ventana se agrega a la cadena del visor del portapapeles mediante una llamada a la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="9754a-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="9754a-236">El valor devuelto es el identificador de la siguiente ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9754a-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="9754a-237">Una ventana debe realizar un seguimiento de este valor; por ejemplo, al guardarlo en una variable estática denominada *hwndNextViewer*.</span><span class="sxs-lookup"><span data-stu-id="9754a-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="9754a-238">En el ejemplo siguiente se agrega una ventana a la cadena del visor del portapapeles en respuesta al mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="9754a-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="9754a-239">Los fragmentos de código se muestran para las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9754a-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="9754a-240">Procesar el mensaje de CHANGECBCHAIN de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="9754a-241">Quitar una ventana de la cadena del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="9754a-242">Procesar el mensaje de DRAWCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="9754a-243">Ejemplo de un visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="9754a-244">Procesar el mensaje de CHANGECBCHAIN de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="9754a-245">Una ventana del visor del portapapeles recibe el mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) cuando otra ventana se está quitando de la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="9754a-246">Si la ventana que se va a quitar es la ventana siguiente de la cadena, la ventana que recibe el mensaje debe desvincular la siguiente ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9754a-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="9754a-247">De lo contrario, este mensaje se debe pasar a la siguiente ventana de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9754a-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="9754a-248">En el ejemplo siguiente se muestra el procesamiento del mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="9754a-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="9754a-249">Quitar una ventana de la cadena del visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="9754a-250">Para quitarse de la cadena del visor del portapapeles, una ventana llama a la función [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) .</span><span class="sxs-lookup"><span data-stu-id="9754a-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="9754a-251">En el ejemplo siguiente se quita una ventana de la cadena del visor del portapapeles en respuesta al mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="9754a-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="9754a-252">Procesar el mensaje de DRAWCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="9754a-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="9754a-253">El mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) notifica a una ventana del visor del portapapeles que el contenido del portapapeles ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9754a-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="9754a-254">Una ventana debe hacer lo siguiente al procesar el mensaje de **\_ DRAWCLIPBOARD de WM** :</span><span class="sxs-lookup"><span data-stu-id="9754a-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="9754a-255">Determine cuál de los formatos de Portapapeles disponibles desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="9754a-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="9754a-256">Recupera los datos del portapapeles y los muestra en la ventana.</span><span class="sxs-lookup"><span data-stu-id="9754a-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="9754a-257">O bien, si el formato del portapapeles es **CF \_ OWNERDISPLAY**, envíe un mensaje de [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) al propietario del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="9754a-258">Envíe el mensaje a la siguiente ventana de la cadena del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="9754a-259">Para obtener un ejemplo de procesamiento del mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) , vea la lista de ejemplos en el [ejemplo de un visor del portapapeles](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="9754a-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="9754a-260">Ejemplo de un visor del portapapeles</span><span class="sxs-lookup"><span data-stu-id="9754a-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="9754a-261">En el ejemplo siguiente se muestra una aplicación sencilla del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9754a-261">The following example shows a simple clipboard viewer application.</span></span>


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 