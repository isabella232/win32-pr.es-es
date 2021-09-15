---
title: Usar cuadros de diálogo
description: Los cuadros de diálogo se usan para mostrar información y solicitar la entrada del usuario.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows Interfaz de usuario,windowing
- Windows Interfaz de usuario,cuadros de diálogo
- ventanas, cuadros de diálogo
- cuadros de diálogo, acerca de
- cuadros de diálogo, mostrar
- cuadros de diálogo modales
- cuadros de diálogo no modales
- cuadros de diálogo, modal
- cuadros de diálogo, modeless
- cuadros de diálogo, inicializar
- plantillas de cuadro de diálogo
- cuadros de diálogo, plantillas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360513"
---
# <a name="using-dialog-boxes"></a>Usar cuadros de diálogo

Los cuadros de diálogo se usan para mostrar información y solicitar la entrada del usuario. La aplicación carga e inicializa el cuadro de diálogo, procesa la entrada del usuario y destruye el cuadro de diálogo cuando el usuario finaliza la tarea. El proceso para controlar los cuadros de diálogo varía, dependiendo de si el cuadro de diálogo es modal o no modal. Un cuadro de diálogo modal requiere que el usuario cierre el cuadro de diálogo antes de activar otra ventana en la aplicación. Sin embargo, el usuario puede activar ventanas en distintas aplicaciones. Un cuadro de diálogo no modelo no requiere una respuesta inmediata del usuario. Es similar a una ventana principal que contiene controles.

En las secciones siguientes se describe cómo usar ambos tipos de cuadros de diálogo.

-   [Mostrar un cuadro de mensaje](#displaying-a-message-box)
-   [Crear un cuadro de diálogo modal](#creating-a-modal-dialog-box)
-   [Crear un cuadro de diálogo no modelo](#creating-a-modeless-dialog-box)
-   [Inicializar un cuadro de diálogo](#initializing-a-dialog-box)
-   [Crear una plantilla en memoria](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Mostrar un cuadro de mensaje

La forma más sencilla de cuadro de diálogo modal es el cuadro de mensaje. La mayoría de las aplicaciones usan cuadros de mensaje para advertir al usuario de errores y solicitar instrucciones sobre cómo continuar después de que se haya producido un error. Cree un cuadro de mensaje mediante la función [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) especificando el mensaje y el número y tipo de botones que se mostrarán. El sistema crea un cuadro de diálogo modal, proporcionando su propia plantilla y procedimiento de cuadro de diálogo. Una vez que el usuario cierra el cuadro de mensaje, **MessageBox** o **MessageBoxEx** devuelven un valor que identifica el botón elegido por el usuario para cerrar el cuadro de mensaje.

En el ejemplo siguiente, la aplicación muestra un cuadro de mensaje que solicita al usuario una acción después de que se haya producido una condición de error. El cuadro de mensaje muestra el mensaje que describe la condición de error y cómo resolverla. El **estilo \_ MB YESNO** indica a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) que proporcione dos botones con los que el usuario puede elegir cómo continuar:


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



En la imagen siguiente se muestra la salida del ejemplo de código anterior:

![cuadro de mensaje](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Crear un cuadro de diálogo modal

Para crear un cuadro de diálogo modal, use la [**función DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Debe especificar el identificador o el nombre de un recurso de plantilla de cuadro de diálogo y un puntero al procedimiento del cuadro de diálogo. La **función DialogBox** carga la plantilla, muestra el cuadro de diálogo y procesa toda la entrada del usuario hasta que el usuario cierra el cuadro de diálogo.

En el ejemplo siguiente, la aplicación muestra un cuadro de diálogo modal cuando el usuario hace clic **en Eliminar elemento** desde un menú de la aplicación. El cuadro de diálogo contiene un control de edición (en el que el usuario escribe el nombre de un elemento) y **los botones Aceptar** **y** Cancelar. Los identificadores de control para estos controles son ID \_ ITEMNAME, IDOK e IDCANCEL, respectivamente.

La primera parte del ejemplo consta de las instrucciones que crean el cuadro de diálogo modal. Estas instrucciones, en el procedimiento de ventana de la ventana principal de la aplicación, crean el cuadro de diálogo cuando el sistema recibe un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) que tiene el identificador de menú \_ DELETEITEM de IDM. La segunda parte del ejemplo es el procedimiento del cuadro de diálogo, que recupera el contenido del control de edición y cierra el cuadro de diálogo al recibir un **mensaje \_ WM COMMAND.**

Las instrucciones siguientes crean el cuadro de diálogo modal. La plantilla de cuadro de diálogo es un recurso en el archivo ejecutable de la aplicación y tiene el identificador de recurso DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



En este ejemplo, la aplicación especifica su ventana principal como ventana propietaria del cuadro de diálogo. Cuando el sistema muestra inicialmente el cuadro de diálogo, su posición es relativa a la esquina superior izquierda del área de cliente de la ventana propietaria. La aplicación usa el valor devuelto de [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) para determinar si se debe continuar con la operación o cancelarla. Las instrucciones siguientes definen el procedimiento del cuadro de diálogo.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



En este ejemplo, el procedimiento usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) para recuperar el texto actual del control de edición identificado por ID \_ ITEMNAME. A continuación, el procedimiento llama a la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para establecer el valor devuelto del cuadro de diálogo en IDOK o IDCANCEL, en función del mensaje recibido, y para iniciar el proceso de cierre del cuadro de diálogo. Los identificadores IDOK e IDCANCEL corresponden a los **botones Aceptar** **y** Cancelar. Después de que el procedimiento llame a **EndDialog**, el sistema envía mensajes adicionales al procedimiento para destruir el cuadro de diálogo y devuelve el valor devuelto del cuadro de diálogo a la función que creó el cuadro de diálogo.

## <a name="creating-a-modeless-dialog-box"></a>Crear un cuadro de diálogo no modelo

Puede crear un cuadro de diálogo no modelo mediante la función [**CreateDialog,**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) especificando el identificador o el nombre de un recurso de plantilla de cuadro de diálogo y un puntero al procedimiento del cuadro de diálogo. **CreateDialog** carga la plantilla, crea el cuadro de diálogo y, opcionalmente, la muestra. La aplicación es responsable de recuperar y enviar mensajes de entrada de usuario al procedimiento del cuadro de diálogo.

En el ejemplo siguiente, la aplicación muestra un cuadro de diálogo no modelo (si aún no se muestra) cuando el usuario hace clic en **Ir** a desde un menú de la aplicación. El cuadro de diálogo contiene un control de edición, una casilla y los **botones Aceptar** **y** Cancelar. La plantilla de cuadro de diálogo es un recurso en el archivo ejecutable de la aplicación y tiene el identificador de recurso DLG \_ GOTO. El usuario escribe un número de línea en el control de edición y comprueba la casilla para especificar que el número de línea es relativo a la línea actual. Los identificadores de control son ID \_ LINE, ID \_ ABSREL, IDOK e IDCANCEL.

Las instrucciones de la primera parte del ejemplo crean el cuadro de diálogo modeless. Estas instrucciones, en el procedimiento de ventana de la ventana principal de la aplicación, crean el cuadro de diálogo cuando el procedimiento de ventana recibe un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) que tiene el identificador de menú IDM GOTO, pero solo si la variable global aún no contiene un identificador \_ válido. La segunda parte del ejemplo es el bucle de mensajes principal de la aplicación. El bucle incluye la [**función IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para asegurarse de que el usuario puede usar la interfaz de teclado del cuadro de diálogo en este cuadro de diálogo no modelo. La tercera parte del ejemplo es el procedimiento del cuadro de diálogo. El procedimiento recupera el contenido del control de edición y la casilla cuando el usuario hace clic en el **botón** Aceptar. El procedimiento destruye el cuadro de diálogo cuando el usuario hace clic en el **botón** Cancelar.


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



En las instrucciones anteriores, se llama a [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) solo si `hwndGoto` no contiene un identificador de ventana válido. Esto garantiza que la aplicación no muestra dos cuadros de diálogo al mismo tiempo. Para admitir este método de comprobación, el procedimiento de diálogo debe establecerse en **NULL** cuando destruye el cuadro de diálogo.

El bucle de mensajes de una aplicación consta de las siguientes instrucciones.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



El bucle comprueba la validez del identificador de ventana en el cuadro de diálogo y solo llama a la [**función IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) si el identificador es válido. **IsDialogMessage** solo procesa el mensaje si pertenece al cuadro de diálogo. De lo contrario, **devuelve FALSE** y el bucle envía el mensaje a la ventana adecuada.

Las instrucciones siguientes definen el procedimiento del cuadro de diálogo.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



En las instrucciones anteriores, el procedimiento procesa los [**mensajes WM \_ INITDIALOG**](wm-initdialog.md) [**y WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) Durante **el procesamiento de WM \_ INITDIALOG,** el procedimiento inicializa la casilla pasando el valor actual de la variable global a [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). A continuación, el **procedimiento devuelve TRUE** para dirigir el sistema para establecer el foco de entrada predeterminado.

Durante [**el procesamiento de WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) el procedimiento cierra  el cuadro de diálogo solo si el usuario hace clic en el botón Cancelar, es decir, el botón que tiene el identificador IDCANCEL. El procedimiento debe llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para cerrar un cuadro de diálogo no modelo. Observe que el procedimiento también establece la variable en **NULL** para asegurarse de que otras instrucciones que dependen de esta variable funcionan correctamente.

Si el usuario hace clic **en** el botón Aceptar, el procedimiento recupera el estado actual de la casilla y lo asigna a la variable **fRelative.** A continuación, usa la variable para recuperar el número de línea del control de edición. [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) traduce el texto del control de edición en un entero. El valor de **fRelative** determina si la función interpreta el número como un valor con signo o sin signo. Si el texto del control de edición no es un número válido, **GetDlgItemInt** establece el valor de la variable **fError** en distinto de cero. El procedimiento comprueba este valor para determinar si se debe mostrar un mensaje de error o llevar a cabo la tarea. En caso de error, el procedimiento del cuadro de diálogo envía un mensaje al control de edición, que le indica que seleccione el texto del control para que el usuario pueda reemplazarlo fácilmente. Si **GetDlgItemInt** no devuelve un error, el procedimiento puede llevar a cabo la propia tarea solicitada o enviar un mensaje a la ventana de propietario, lo que le indica que lleve a cabo la operación.

## <a name="initializing-a-dialog-box"></a>Inicializar un cuadro de diálogo

Inicialice el cuadro de diálogo y su contenido al procesar el [**mensaje \_ WM INITDIALOG.**](wm-initdialog.md) La tarea más común es inicializar los controles para reflejar la configuración actual del cuadro de diálogo. Otra tarea común consiste en centrar un cuadro de diálogo en la pantalla o dentro de su ventana de propietario. Una tarea útil para algunos cuadros de diálogo es establecer el foco de entrada en un control especificado en lugar de aceptar el foco de entrada predeterminado.

En el ejemplo siguiente, el procedimiento del cuadro de diálogo centra el cuadro de diálogo y establece el foco de entrada al procesar el [**mensaje \_ WM INITDIALOG.**](wm-initdialog.md) Para centrar el cuadro de diálogo, el procedimiento recupera los rectángulos de ventana para el cuadro de diálogo y la ventana de propietario y calcula una nueva posición para el cuadro de diálogo. Para establecer el foco de entrada, el procedimiento comprueba el *parámetro wParam* para determinar el identificador del foco de entrada predeterminado.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



En las instrucciones anteriores, el procedimiento usa la función [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para recuperar el identificador de ventana de propietario en un cuadro de diálogo. La función devuelve el identificador de la ventana de propietario a los cuadros de diálogo y el identificador de la ventana primaria a las ventanas secundarias. Dado que una aplicación puede crear un cuadro de diálogo que no tiene propietario, el procedimiento comprueba el identificador devuelto y usa la función [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) para recuperar el identificador de ventana de escritorio, si es necesario. Después de calcular la nueva posición, el procedimiento usa la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover el cuadro de diálogo, especificando el valor HWND TOP para asegurarse de que el cuadro de diálogo permanece en la parte superior de la \_ ventana del propietario.

Antes de establecer el foco de entrada, el procedimiento comprueba el identificador de control del foco de entrada predeterminado. El sistema pasa el identificador de ventana del foco de entrada predeterminado en el *parámetro wParam.* La [**función GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) devuelve el identificador del control identificado por el identificador de ventana. Si el identificador no coincide con el identificador correcto, el procedimiento usa la [**función SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) para establecer el foco de entrada. La [**función GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) es necesaria para recuperar el identificador de ventana del control deseado.

## <a name="creating-a-template-in-memory"></a>Creación de una plantilla en memoria

Las aplicaciones a veces adaptan o modifican el contenido de los cuadros de diálogo en función del estado actual de los datos que se procesan. En tales casos, no es práctico proporcionar todas las plantillas de cuadro de diálogo posibles como recursos en el archivo ejecutable de la aplicación. Pero la creación de plantillas en memoria proporciona a la aplicación más flexibilidad para adaptarse a cualquier circunstancia.

En el ejemplo siguiente, la aplicación crea una plantilla en memoria para un cuadro de diálogo modal que contiene un mensaje y **botones Aceptar** **y** Ayuda.

En una plantilla de diálogo, todas las cadenas de caracteres, como el cuadro de diálogo y los títulos de botón, deben ser cadenas Unicode. En este ejemplo se [**usa la función MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para generar estas cadenas Unicode.

Las [**estructuras DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) de una plantilla de diálogo deben alinearse en los **límites DWORD.** Para alinear estas estructuras, en este ejemplo se usa una rutina auxiliar que toma un puntero de entrada y devuelve el puntero más cercano que se alinea en un **límite DWORD.**


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 