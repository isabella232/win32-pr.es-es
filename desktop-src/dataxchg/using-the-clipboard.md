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
# <a name="using-the-clipboard"></a>Usar el portapapeles

Esta sección contiene ejemplos de código para las siguientes tareas:

-   [Implementar los comandos cortar, copiar y pegar](#implementing-the-cut-copy-and-paste-commands)
    -   [Seleccionar datos](#selecting-data)
    -   [Crear un menú de edición](#creating-an-edit-menu)
    -   [Procesar el mensaje de INITMENUPOPUP de WM \_](#processing-the-wm_initmenupopup-message)
    -   [Procesar el mensaje de comando de WM \_](#processing-the-wm_command-message)
    -   [Copiar información en el portapapeles](#copying-information-to-the-clipboard)
    -   [Pegar información del portapapeles](#pasting-information-from-the-clipboard)
    -   [Registrar un formato de Portapapeles](#registering-a-clipboard-format)
    -   [Procesamiento de los \_ mensajes de WM RENDERFORMAT y WM \_ RENDERALLFORMATS](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Procesar el mensaje de DESTROYCLIPBOARD de WM \_](#processing-the-wm_destroyclipboard-message)
    -   [Usar el formato del portapapeles Owner-Display](#using-the-owner-display-clipboard-format)
-   [Supervisar el contenido del portapapeles](#monitoring-clipboard-contents)
-   [Consultar el número de secuencia del portapapeles](#querying-the-clipboard-sequence-number)
-   [Crear un agente de escucha de formato del portapapeles](#creating-a-clipboard-format-listener)
-   [Crear una ventana del visor del portapapeles](#creating-a-clipboard-viewer-window)
-   [Agregar una ventana a la cadena del visor del portapapeles](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Procesar el mensaje de CHANGECBCHAIN de WM \_](#processing-the-wm_changecbchain-message)
    -   [Quitar una ventana de la cadena del visor del portapapeles](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Procesar el mensaje de DRAWCLIPBOARD de WM \_](#processing-the-wm_drawclipboard-message)
    -   [Ejemplo de un visor del portapapeles](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implementar los comandos cortar, copiar y pegar

En esta sección se describe cómo se implementan los comandos estándar de **cortar**, **copiar** y **pegar** en una aplicación. En el ejemplo de esta sección se usan estos métodos para colocar datos en el Portapapeles con un formato de Portapapeles registrado, el formato de **CF \_ OWNERDISPLAY** y el formato de **\_ texto CF** . El formato registrado se usa para representar ventanas de texto rectangulares o elípticas, denominadas etiquetas.

### <a name="selecting-data"></a>Seleccionar datos

Antes de que se pueda copiar la información en el portapapeles, el usuario debe seleccionar la información específica que se va a copiar o cortar. Una aplicación debe proporcionar un medio para que el usuario seleccione información dentro de un documento y algún tipo de comentario visual para indicar los datos seleccionados.

### <a name="creating-an-edit-menu"></a>Crear un menú de edición

Una aplicación debe cargar una tabla de aceleradores que contenga los aceleradores de teclado estándar para los comandos del menú **edición** . La función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) debe agregarse al bucle de mensajes de la aplicación para que los aceleradores surtan efecto. Para obtener más información acerca de los aceleradores de teclado, consulte [aceleradores de teclado](/windows/desktop/menurc/keyboard-accelerators).

### <a name="processing-the-wm_initmenupopup-message"></a>Procesar el mensaje de INITMENUPOPUP de WM \_

No todos los comandos del portapapeles están disponibles para el usuario en un momento dado. Una aplicación debe procesar el mensaje de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) para habilitar los elementos de menú para los comandos disponibles y deshabilitar los comandos no disponibles.

A continuación se indica el caso de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) para una aplicación denominada etiqueta.


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



La función InitMenu se define de la siguiente manera.


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



### <a name="processing-the-wm_command-message"></a>Procesar el mensaje de comando de WM \_

Para procesar los comandos de menú, agregue el caso de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento de ventana principal de la aplicación. A continuación se indica el caso de **\_ comando de WM** para el procedimiento de ventana de la aplicación de etiqueta.


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



Para llevar a cabo los comandos de **copiar** y **cortar** , el procedimiento de ventana llama a la función EditCopy definida por la aplicación. Para obtener más información, vea [copiar información en el portapapeles](#copying-information-to-the-clipboard). Para llevar a cabo el comando **pegar** , el procedimiento de ventana llama a la función EditPaste definida por la aplicación. Para obtener más información sobre la función EditPaste, vea [pegar información desde el portapapeles](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Copiar información en el portapapeles

En la aplicación de etiqueta, la función EditCopy definida por la aplicación copia la selección actual en el portapapeles. Esta función hace lo siguiente:

1.  Abre el portapapeles mediante una llamada a la función [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Vacía el portapapeles mediante una llamada a la función [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .
3.  Llama a la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) una vez para cada formato del portapapeles que proporciona la aplicación.
4.  Cierra el portapapeles mediante una llamada a la función [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Dependiendo de la selección actual, la función EditCopy copia un intervalo de texto o copia una estructura definida por la aplicación que representa una etiqueta completa. La estructura, denominada LABELBOX, se define como se indica a continuación.


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



A continuación se encuentra la función EditCopy.


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



### <a name="pasting-information-from-the-clipboard"></a>Pegar información del portapapeles

En la aplicación de etiqueta, la función EditPaste definida por la aplicación pega el contenido del portapapeles. Esta función hace lo siguiente:

1.  Abre el portapapeles mediante una llamada a la función [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Determina cuál de los formatos disponibles del portapapeles se va a recuperar.
3.  Recupera el identificador de los datos en el formato seleccionado mediante una llamada a la función [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .
4.  Inserta una copia de los datos en el documento.

    El portapapeles todavía posee el identificador devuelto por [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) , por lo que una aplicación no debe liberarlo ni dejarlo bloqueado.

5.  Cierra el portapapeles mediante una llamada a la función [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Si se selecciona una etiqueta y contiene un punto de inserción, la función EditPaste inserta el texto del portapapeles en el punto de inserción. Si no hay ninguna selección o si se selecciona una etiqueta, la función crea una etiqueta nueva, usando la estructura LABELBOX definida por la aplicación en el portapapeles. La estructura LABELBOX se coloca en el portapapeles mediante el uso de un formato de Portapapeles registrado.

La estructura, denominada LABELBOX, se define como se indica a continuación.


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



A continuación se encuentra la función EditPaste.


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



### <a name="registering-a-clipboard-format"></a>Registrar un formato de Portapapeles

Para registrar un formato del portapapeles, agregue una llamada a la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) a la función de inicialización de instancia de la aplicación, como se indica a continuación.


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Procesamiento de los \_ mensajes de WM RENDERFORMAT y WM \_ RENDERALLFORMATS

Si una ventana pasa un identificador **null** a la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , debe procesar los mensajes de [**WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) para representar los datos a petición.

Si una ventana retrasa la representación de un formato específico y, a continuación, otra aplicación solicita datos en ese formato, se envía un mensaje de [**\_ RENDERFORMAT de WM**](wm-renderformat.md) a la ventana. Además, si una ventana retrasa la representación de uno o más formatos y alguno de esos formatos permanece sin procesar cuando la ventana está a punto de ser destruida, se envía un mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) a la ventana antes de su destrucción.

Para representar un formato del portapapeles, el procedimiento de ventana debe colocar un identificador de datos no **null** en el portapapeles mediante la función [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) . Si el procedimiento de ventana está representando un formato en respuesta al mensaje de [**\_ RENDERFORMAT de WM**](wm-renderformat.md) , no debe abrir el portapapeles antes de llamar a **SetClipboardData**. Pero si se representan uno o varios formatos en respuesta al mensaje de [**\_ RENDERALLFORMATS de WM**](wm-renderallformats.md) , debe abrir el portapapeles y comprobar que la ventana sigue siendo propietaria del portapapeles antes de llamar a **SetClipboardData** y debe cerrar el portapapeles antes de volver.

La aplicación de etiqueta procesa los mensajes de [**WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) como se indica a continuación.


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



En ambos casos, el procedimiento de ventana llama a la función RenderFormat definida por la aplicación, que se define de la manera siguiente.

La estructura, denominada LABELBOX, se define como se indica a continuación.


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



### <a name="processing-the-wm_destroyclipboard-message"></a>Procesar el mensaje de DESTROYCLIPBOARD de WM \_

Una ventana puede procesar el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) para liberar los recursos que se han reservado para admitir la representación diferida. Por ejemplo, la aplicación de etiqueta, al copiar una etiqueta en el portapapeles, asigna un objeto de memoria local. A continuación, libera este objeto como respuesta al mensaje **de \_ DESTROYCLIPBOARD de WM** , como se indica a continuación.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Usar el formato del portapapeles Owner-Display

Si una ventana coloca información en el portapapeles mediante el formato de Portapapeles de **CF \_ OWNERDISPLAY** , debe hacer lo siguiente:

-   Procese el mensaje de [**\_ PAINTCLIPBOARD de WM**](wm-paintclipboard.md) . Este mensaje se envía al propietario del portapapeles cuando se debe volver a dibujar una parte de la ventana del visor del portapapeles.

-   Procese el mensaje de [**\_ SIZECLIPBOARD de WM**](wm-sizeclipboard.md) . Este mensaje se envía al propietario del portapapeles cuando se ha cambiado el tamaño de la ventana del visor del portapapeles o se ha modificado su contenido.

    Normalmente, una ventana responde a este mensaje estableciendo las posiciones y los intervalos de desplazamiento de la ventana del visor del portapapeles. En respuesta a este mensaje, la aplicación de etiqueta también actualiza una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) para la ventana del visor del portapapeles.

-   Procese los mensajes de [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) y [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) . Estos mensajes se envían al propietario del portapapeles cuando se produce un evento de barra de desplazamiento en la ventana del visor del portapapeles.

-   Procese el mensaje de [**\_ ASKCBFORMATNAME de WM**](wm-askcbformatname.md) . La ventana Visor del portapapeles envía este mensaje a una aplicación para recuperar el nombre del formato de presentación del propietario.

El procedimiento de ventana de la aplicación de etiqueta procesa estos mensajes, como se indica a continuación.


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



## <a name="monitoring-clipboard-contents"></a>Supervisar el contenido del portapapeles

Hay tres formas de supervisar los cambios en el portapapeles. El método más antiguo es crear una ventana del visor del portapapeles. Windows 2000 agregó la capacidad de consultar el número de secuencia del portapapeles y Windows Vista agregó compatibilidad con los agentes de escucha de formato del portapapeles. Las ventanas del visor del portapapeles se admiten por compatibilidad con versiones anteriores de Windows. Los nuevos programas deben usar agentes de escucha de formato del portapapeles o el número de secuencia del portapapeles.

## <a name="querying-the-clipboard-sequence-number"></a>Consultar el número de secuencia del portapapeles

Cada vez que cambia el contenido del portapapeles, se incrementa un valor de 32 bits conocido como el número de secuencia del portapapeles. Un programa puede recuperar el número de secuencia del portapapeles actual llamando a la función [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) . Al comparar el valor devuelto con un valor devuelto por una llamada anterior a **GetClipboardSequenceNumber**, un programa puede determinar si el contenido del portapapeles ha cambiado. Este método es más adecuado para los programas que almacenan en caché los resultados en función del contenido actual del portapapeles y necesitan saber si los cálculos siguen siendo válidos antes de usar los resultados de esa caché. Tenga en cuenta que este no es un método de notificación y no debe usarse en un bucle de sondeo. Para recibir una notificación cuando cambie el contenido del portapapeles, utilice un agente de escucha de formato del portapapeles o un visor del portapapeles.

## <a name="creating-a-clipboard-format-listener"></a>Crear un agente de escucha de formato del portapapeles

Un agente de escucha de formato del portapapeles es una ventana que se ha registrado para recibir notificaciones cuando cambia el contenido del portapapeles. Este método se recomienda para crear una ventana del visor del portapapeles porque es más fácil de implementar y evitar problemas si los programas no mantienen correctamente la cadena del visor del portapapeles o si una ventana de la cadena del visor del portapapeles deja de responder a los mensajes.

Una ventana se registra como un agente de escucha de formato del portapapeles mediante una llamada a la función [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) . Cuando cambia el contenido del portapapeles, se envía un mensaje de [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) a la ventana. El registro sigue siendo válido hasta que la ventana se anula el registro mediante una llamada a la función [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .

## <a name="creating-a-clipboard-viewer-window"></a>Crear una ventana del visor del portapapeles

Una ventana del visor del portapapeles muestra el contenido actual del portapapeles y recibe mensajes cuando cambia el contenido del portapapeles. Para crear una ventana del visor del portapapeles, la aplicación debe hacer lo siguiente:

-   Agregue la ventana a la cadena del visor del portapapeles.
-   Procese el mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .
-   Procese el mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) .
-   Quite la ventana de la cadena del visor del portapapeles antes de que se destruya.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Agregar una ventana a la cadena del visor del portapapeles

Una ventana se agrega a la cadena del visor del portapapeles mediante una llamada a la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . El valor devuelto es el identificador de la siguiente ventana de la cadena. Una ventana debe realizar un seguimiento de este valor; por ejemplo, al guardarlo en una variable estática denominada *hwndNextViewer*.

En el ejemplo siguiente se agrega una ventana a la cadena del visor del portapapeles en respuesta al mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Los fragmentos de código se muestran para las siguientes tareas:

-   [Procesar el mensaje de CHANGECBCHAIN de WM \_](/windows)
-   [Quitar una ventana de la cadena del visor del portapapeles](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Procesar el mensaje de DRAWCLIPBOARD de WM \_](/windows)
-   [Ejemplo de un visor del portapapeles](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Procesar el mensaje de CHANGECBCHAIN de WM \_

Una ventana del visor del portapapeles recibe el mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) cuando otra ventana se está quitando de la cadena del visor del portapapeles. Si la ventana que se va a quitar es la ventana siguiente de la cadena, la ventana que recibe el mensaje debe desvincular la siguiente ventana de la cadena. De lo contrario, este mensaje se debe pasar a la siguiente ventana de la cadena.

En el ejemplo siguiente se muestra el procesamiento del mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Quitar una ventana de la cadena del visor del portapapeles

Para quitarse de la cadena del visor del portapapeles, una ventana llama a la función [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . En el ejemplo siguiente se quita una ventana de la cadena del visor del portapapeles en respuesta al mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) .


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Procesar el mensaje de DRAWCLIPBOARD de WM \_

El mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) notifica a una ventana del visor del portapapeles que el contenido del portapapeles ha cambiado. Una ventana debe hacer lo siguiente al procesar el mensaje de **\_ DRAWCLIPBOARD de WM** :

1.  Determine cuál de los formatos de Portapapeles disponibles desea mostrar.
2.  Recupera los datos del portapapeles y los muestra en la ventana. O bien, si el formato del portapapeles es **CF \_ OWNERDISPLAY**, envíe un mensaje de [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) al propietario del portapapeles.
3.  Envíe el mensaje a la siguiente ventana de la cadena del visor del portapapeles.

Para obtener un ejemplo de procesamiento del mensaje de [**\_ DRAWCLIPBOARD de WM**](wm-drawclipboard.md) , vea la lista de ejemplos en el [ejemplo de un visor del portapapeles](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Ejemplo de un visor del portapapeles

En el ejemplo siguiente se muestra una aplicación sencilla del visor del portapapeles.


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



 

 