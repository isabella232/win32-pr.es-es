---
title: Uso del Portapapeles
description: En esta sección se muestran ejemplos de código para las siguientes tareas.
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- portapapeles, cortar datos
- clipboard,copying data
- portapapeles, pegar datos
- portapapeles, selección de datos
- clipboard,Editar comandos de menú
- clipboard,viewers
- portapapeles, ventanas de visor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063877"
---
# <a name="using-the-clipboard"></a>Uso del Portapapeles

En esta sección se muestran ejemplos de código para las siguientes tareas:

-   [Implementación de los comandos Cortar, Copiar y Pegar](#implementing-the-cut-copy-and-paste-commands)
    -   [Selección de datos](#selecting-data)
    -   [Crear un menú Editar](#creating-an-edit-menu)
    -   [Procesamiento del mensaje \_ WM INITMENUPOPUP](#processing-the-wm_initmenupopup-message)
    -   [Procesamiento del mensaje \_ WM COMMAND](#processing-the-wm_command-message)
    -   [Copiar información en el Portapapeles](#copying-information-to-the-clipboard)
    -   [Pegar información desde el Portapapeles](#pasting-information-from-the-clipboard)
    -   [Registrar un formato de Portapapeles](#registering-a-clipboard-format)
    -   [Procesamiento de los mensajes \_ RENDERFORMAT y WM \_ RENDERALLFORMATS](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Procesamiento del mensaje \_ WM DESTROYCLIPBOARD](#processing-the-wm_destroyclipboard-message)
    -   [Usar el formato Owner-Display clipboard](#using-the-owner-display-clipboard-format)
-   [Supervisión del contenido del Portapapeles](#monitoring-clipboard-contents)
-   [Consulta del número de secuencia del Portapapeles](#querying-the-clipboard-sequence-number)
-   [Creación de un agente de escucha de formato del Portapapeles](#creating-a-clipboard-format-listener)
-   [Crear una ventana del Visor del Portapapeles](#creating-a-clipboard-viewer-window)
-   [Agregar una ventana a la cadena del visor del Portapapeles](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Procesamiento del mensaje \_ CHANGECBCHAIN de WM](#processing-the-wm_changecbchain-message)
    -   [Quitar una ventana de la cadena de visor del Portapapeles](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Procesamiento del mensaje \_ DRAWCLIPBOARD de WM](#processing-the-wm_drawclipboard-message)
    -   [Ejemplo de visor del Portapapeles](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implementación de los comandos Cortar, Copiar y Pegar

En esta sección se describe cómo  se **implementan** los comandos **estándar Cortar,** Copiar y Pegar en una aplicación. En el ejemplo de esta sección se usan estos métodos para colocar datos en el Portapapeles mediante un formato de Portapapeles registrado, el formato **\_ OWNERDISPLAY** de CF y el formato **CF \_ TEXT.** El formato registrado se usa para representar ventanas de texto rectangulares o elípticas, denominadas etiquetas.

### <a name="selecting-data"></a>Seleccionar datos

Para poder copiar información en el Portapapeles, el usuario debe seleccionar información específica para copiarla o cortarla. Una aplicación debe proporcionar un medio para que el usuario seleccione información dentro de un documento y algún tipo de comentarios visuales para indicar los datos seleccionados.

### <a name="creating-an-edit-menu"></a>Crear un menú Editar

Una aplicación debe cargar una tabla de aceleradores que contenga los aceleradores de teclado estándar para los **comandos de** menú Editar. La [**función TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) debe agregarse al bucle de mensajes de la aplicación para que los aceleradores sumen efecto. Para obtener más información sobre los aceleradores de teclado, vea [Aceleradores de teclado.](/windows/desktop/menurc/keyboard-accelerators)

### <a name="processing-the-wm_initmenupopup-message"></a>Procesamiento del mensaje \_ WM INITMENUPOPUP

No todos los comandos del Portapapeles están disponibles para el usuario en un momento dado. Una aplicación debe procesar el mensaje [**\_ WM INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) para habilitar los elementos de menú de los comandos disponibles y deshabilitar los comandos no disponibles.

A continuación se [**muestra el \_ caso INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) para una aplicación denominada Label.


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



### <a name="processing-the-wm_command-message"></a>Procesamiento del mensaje \_ WM COMMAND

Para procesar comandos de menú, agregue el caso [**\_ WM COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento de ventana principal de la aplicación. A continuación se **muestra el caso WM \_ COMMAND** para el procedimiento de ventana de la aplicación Label.


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



Para llevar a cabo los **comandos Copy** y **Cut,** el procedimiento de ventana llama a la función EditCopy definida por la aplicación. Para obtener más información, [vea Copiar información en el Portapapeles.](#copying-information-to-the-clipboard) Para llevar a cabo el **comando Pegar,** el procedimiento de ventana llama a la función EditPaste definida por la aplicación. Para obtener más información sobre la función EditPaste, vea [Pegar información desde el Portapapeles.](#pasting-information-from-the-clipboard)

### <a name="copying-information-to-the-clipboard"></a>Copiar información en el Portapapeles

En la aplicación Etiqueta, la función EditCopy definida por la aplicación copia la selección actual en el Portapapeles. Esta función hace lo siguiente:

1.  Abre el Portapapeles mediante una llamada a la [**función OpenClipboard.**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
2.  Vacía el Portapapeles mediante una llamada a [**la función EmptyClipboard.**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
3.  Llama a [**la función SetClipboardData una**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) vez para cada formato del Portapapeles que proporciona la aplicación.
4.  Cierra el Portapapeles mediante una llamada a [**la función CloseClipboard.**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)

En función de la selección actual, la función EditCopy copia un intervalo de texto o copia una estructura definida por la aplicación que representa una etiqueta completa. La estructura, denominada LABELBOX, se define de la siguiente manera.


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



A continuación se muestra la función EditCopy.


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



### <a name="pasting-information-from-the-clipboard"></a>Pegar información desde el Portapapeles

En la aplicación Etiqueta, la función EditPaste definida por la aplicación pega el contenido del Portapapeles. Esta función hace lo siguiente:

1.  Abre el Portapapeles mediante una llamada a la [**función OpenClipboard.**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
2.  Determina cuál de los formatos de Portapapeles disponibles se va a recuperar.
3.  Recupera el identificador de los datos en el formato seleccionado llamando a la [**función GetClipboardData.**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata)
4.  Inserta una copia de los datos en el documento.

    El identificador devuelto por [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) sigue siendo propiedad del Portapapeles, por lo que una aplicación no debe liberarlo ni dejarlo bloqueado.

5.  Cierra el Portapapeles mediante una llamada a [**la función CloseClipboard.**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)

Si se selecciona una etiqueta y contiene un punto de inserción, la función EditPaste inserta el texto del Portapapeles en el punto de inserción. Si no hay ninguna selección o si se selecciona una etiqueta, la función crea una nueva etiqueta, utilizando la estructura LABELBOX definida por la aplicación en el Portapapeles. La estructura LABELBOX se coloca en el Portapapeles mediante un formato registrado del Portapapeles.

La estructura, denominada LABELBOX, se define de la siguiente manera.


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



A continuación se muestra la función EditPaste.


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

Para registrar un formato de Portapapeles, agregue una llamada a la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) a la función de inicialización de instancias de la aplicación, como se muestra a continuación.


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Procesamiento de los mensajes \_ RENDERFORMAT y WM \_ RENDERALLFORMATS

Si una ventana pasa un identificador **NULL** a la función [**SetClipboardData,**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) debe procesar los mensajes [**WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) para representar los datos a petición.

Si una ventana retrasa la representación de un formato específico y, a continuación, otra aplicación solicita datos en ese formato, se envía un mensaje [**\_ RENDERFORMAT**](wm-renderformat.md) de WM a la ventana. Además, si una ventana retrasa la representación de uno o varios formatos, y si algunos de esos formatos permanecen sin representar cuando la ventana está a punto de destruirse, se envía un mensaje [**\_ RENDERALLFORMATS**](wm-renderallformats.md) wm a la ventana antes de su destrucción.

Para representar un formato de Portapapeles, el procedimiento de ventana debe colocar un identificador de datos que no sea **NULL** en el Portapapeles mediante la [**función SetClipboardData.**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) Si el procedimiento de ventana está representando un formato en respuesta al mensaje [**\_ RENDERFORMAT de WM,**](wm-renderformat.md) no debe abrir el Portapapeles antes de llamar a **SetClipboardData**. Pero si está representando uno o varios formatos en respuesta al mensaje [**\_ RENDERALLFORMATS**](wm-renderallformats.md) de WM, debe abrir el Portapapeles y comprobar que la ventana sigue siendo propietaria del Portapapeles antes de llamar a **SetClipboardData** y debe cerrar el Portapapeles antes de volver.

La aplicación Label procesa los [**mensajes WM \_ RENDERFORMAT**](wm-renderformat.md) y [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) como se muestra a continuación.


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



En ambos casos, el procedimiento de ventana llama a la función RenderFormat definida por la aplicación, definida como se muestra a continuación.

La estructura, denominada LABELBOX, se define de la siguiente manera.


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



### <a name="processing-the-wm_destroyclipboard-message"></a>Procesamiento del mensaje \_ WM DESTROYCLIPBOARD

Una ventana puede procesar el [**mensaje \_ WM DESTROYCLIPBOARD**](wm-destroyclipboard.md) para liberar los recursos que ha reservado para admitir la representación retrasada. Por ejemplo, la aplicación Etiqueta, al copiar una etiqueta en el Portapapeles, asigna un objeto de memoria local. A continuación, libera este objeto en respuesta al mensaje **\_ WM DESTROYCLIPBOARD,** como se indica a continuación.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Usar el formato Owner-Display clipboard

Si una ventana coloca información en el Portapapeles mediante el formato del Portapapeles **\_ CF OWNERDISPLAY,** debe hacer lo siguiente:

-   [**Procese el \_ mensaje PAINTCLIPBOARD de WM.**](wm-paintclipboard.md) Este mensaje se envía al propietario del Portapapeles cuando se debe volver a dibujar una parte de la ventana del visor del Portapapeles.

-   [**Procese el \_ mensaje SIZECLIPBOARD de WM.**](wm-sizeclipboard.md) Este mensaje se envía al propietario del Portapapeles cuando se ha cambiado el tamaño de la ventana del visor del Portapapeles o se ha cambiado su contenido.

    Normalmente, una ventana responde a este mensaje estableciendo las posiciones de desplazamiento y los intervalos de la ventana del visor del Portapapeles. En respuesta a este mensaje, la aplicación Etiqueta también actualiza una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) para la ventana del visor del Portapapeles.

-   [**Procese los mensajes WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) [**y WM \_ VSCROLLCLIPBOARD.**](wm-vscrollclipboard.md) Estos mensajes se envían al propietario del Portapapeles cuando se produce un evento de barra de desplazamiento en la ventana del visor del Portapapeles.

-   [**Procese el \_ mensaje ASKCBFORMATNAME de WM.**](wm-askcbformatname.md) La ventana del visor del Portapapeles envía este mensaje a una aplicación para recuperar el nombre del formato de presentación del propietario.

El procedimiento de ventana de la aplicación Etiqueta procesa estos mensajes, como se muestra a continuación.


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



## <a name="monitoring-clipboard-contents"></a>Supervisión del contenido del Portapapeles

Hay tres maneras de supervisar los cambios en el Portapapeles. El método más antiguo consiste en crear una ventana del visor del Portapapeles. Windows 2000 agregó la capacidad de consultar el número de secuencia del Portapapeles y Windows Vista agregó compatibilidad con los agentes de escucha de formato del Portapapeles. Las ventanas del visor del Portapapeles son compatibles con versiones anteriores de Windows. Los nuevos programas deben usar agentes de escucha de formato del Portapapeles o el número de secuencia del Portapapeles.

## <a name="querying-the-clipboard-sequence-number"></a>Consulta del número de secuencia del Portapapeles

Cada vez que cambia el contenido del Portapapeles, se incrementa un valor de 32 bits conocido como número de secuencia del Portapapeles. Un programa puede recuperar el número de secuencia del Portapapeles actual llamando a la [**función GetClipboardSequenceNumber.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) Al comparar el valor devuelto con un valor devuelto por una llamada anterior a **GetClipboardSequenceNumber**, un programa puede determinar si el contenido del Portapapeles ha cambiado. Este método es más adecuado para los programas que almacena en caché los resultados en función del contenido actual del Portapapeles y necesitan saber si los cálculos siguen siendo válidos antes de usar los resultados de esa caché. Tenga en cuenta que no se trata de un método de notificación y no debe usarse en un bucle de sondeo. Para recibir una notificación cuando cambie el contenido del Portapapeles, use un agente de escucha de formato del Portapapeles o un visor del Portapapeles.

## <a name="creating-a-clipboard-format-listener"></a>Crear un agente de escucha de formato del Portapapeles

Un agente de escucha de formato del Portapapeles es una ventana que se ha registrado para recibir notificaciones cuando el contenido del Portapapeles ha cambiado. Este método se recomienda sobre la creación de una ventana del visor del Portapapeles porque es más fácil de implementar y evita problemas si los programas no mantienen correctamente la cadena del visor del Portapapeles o si una ventana de la cadena del visor del Portapapeles deja de responder a los mensajes.

Una ventana se registra como un agente de escucha de formato del Portapapeles mediante una llamada a [**la función AddClipboardFormatListener.**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) Cuando cambia el contenido del Portapapeles, la ventana se publica un [**mensaje WM \_ CLIPBOARDUPDATE.**](wm-clipboardupdate.md) El registro sigue siendo válido hasta que la ventana se anule el registro mediante una llamada a la [**función RemoveClipboardFormatListener.**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)

## <a name="creating-a-clipboard-viewer-window"></a>Crear una ventana del Visor del Portapapeles

Una ventana del visor del Portapapeles muestra el contenido actual del Portapapeles y recibe mensajes cuando cambia el contenido del Portapapeles. Para crear una ventana del visor del Portapapeles, la aplicación debe hacer lo siguiente:

-   Agregue la ventana a la cadena de visor del Portapapeles.
-   [**Procese el mensaje DE WM \_ CHANGECBCHAIN.**](wm-changecbchain.md)
-   [**Procese el \_ mensaje DRAWCLIPBOARD de WM.**](wm-drawclipboard.md)
-   Quite la ventana de la cadena del visor del Portapapeles antes de que se destruya.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Agregar una ventana a la cadena del Visor del Portapapeles

Una ventana se agrega a la cadena del visor del Portapapeles mediante una llamada a la [**función SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) El valor devuelto es el identificador de la siguiente ventana de la cadena. Una ventana debe realizar un seguimiento de este valor; por ejemplo, guardarlo en una variable estática denominada *hwndNextViewer*.

En el ejemplo siguiente se agrega una ventana a la cadena del visor del Portapapeles en respuesta al [**mensaje WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Los fragmentos de código se muestran para las tareas siguientes:

-   [Procesamiento del mensaje \_ CHANGECBCHAIN de WM](/windows)
-   [Quitar una ventana de la cadena del Visor del Portapapeles](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Procesamiento del mensaje \_ DRAWCLIPBOARD de WM](/windows)
-   [Ejemplo de visor del Portapapeles](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Procesamiento del mensaje \_ CHANGECBCHAIN de WM

Una ventana del visor del Portapapeles recibe el [**mensaje \_ WM CHANGECBCHAIN**](wm-changecbchain.md) cuando otra ventana se quita de la cadena del visor del Portapapeles. Si la ventana que se quita es la siguiente ventana de la cadena, la ventana que recibe el mensaje debe desvincular la siguiente ventana de la cadena. De lo contrario, este mensaje se debe pasar a la siguiente ventana de la cadena.

En el ejemplo siguiente se muestra el procesamiento del [**mensaje \_ CHANGECBCHAIN**](wm-changecbchain.md) de WM.


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Quitar una ventana de la cadena del Visor del Portapapeles

Para quitarse de la cadena del visor del Portapapeles, una ventana llama a [**la función ChangeClipboardChain.**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) En el ejemplo siguiente se quita una ventana de la cadena del visor del Portapapeles en respuesta al [**mensaje WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy)


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Procesamiento del mensaje \_ DRAWCLIPBOARD de WM

El [**mensaje \_ WM DRAWCLIPBOARD**](wm-drawclipboard.md) notifica a una ventana del visor del Portapapeles que el contenido del Portapapeles ha cambiado. Una ventana debe hacer lo siguiente al procesar el **mensaje \_ DRAWCLIPBOARD** de WM:

1.  Determine cuál de los formatos de Portapapeles disponibles se va a mostrar.
2.  Recuperar los datos del Portapapeles y mostrarlos en la ventana. O bien, si el formato del Portapapeles **es CF \_ OWNERDISPLAY,** envíe un mensaje [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) al propietario del Portapapeles.
3.  Envíe el mensaje a la siguiente ventana de la cadena del visor del Portapapeles.

Para obtener un ejemplo de procesamiento del [**mensaje \_ DRAWCLIPBOARD de WM,**](wm-drawclipboard.md) vea la lista de ejemplos [en Ejemplo de un Visor del Portapapeles](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Ejemplo de visor del Portapapeles

En el ejemplo siguiente se muestra una aplicación sencilla de visor del Portapapeles.


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



 

 