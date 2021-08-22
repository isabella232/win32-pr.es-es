---
description: En los ejemplos de código siguientes se muestra cómo realizar las siguientes tareas asociadas a Windows mensajes y colas de mensajes.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Uso de mensajes y colas de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee617f2c48325eccf5a2fdb07741bb88b47738dea812d372acda1454c9dd3d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028343"
---
# <a name="using-messages-and-message-queues"></a>Uso de mensajes y colas de mensajes

En los ejemplos de código siguientes se muestra cómo realizar las siguientes tareas asociadas a Windows mensajes y colas de mensajes.

-   [Crear un bucle de mensajes](#creating-a-message-loop)
-   [Examinar una cola de mensajes](#examining-a-message-queue)
-   [Publicar un mensaje](#posting-a-message)
-   [Envío de un mensaje](#sending-a-message)

## <a name="creating-a-message-loop"></a>Crear un bucle de mensajes

El sistema no crea automáticamente una cola de mensajes para cada subproceso. En su lugar, el sistema crea una cola de mensajes solo para los subprocesos que realizan operaciones que requieren una cola de mensajes. Si el subproceso crea una o varias ventanas, se debe proporcionar un bucle de mensajes; este bucle de mensajes recupera mensajes de la cola de mensajes del subproceso y los envía a los procedimientos de ventana adecuados.

Dado que el sistema dirige mensajes a ventanas individuales de una aplicación, un subproceso debe crear al menos una ventana antes de iniciar su bucle de mensajes. La mayoría de las aplicaciones contienen un único subproceso que crea ventanas. Una aplicación típica registra la clase de ventana para su ventana principal, crea y muestra la ventana principal y, a continuación, inicia su bucle de mensajes, todo en la [**función WinMain.**](/windows/win32/api/winbase/nf-winbase-winmain)

Puede crear un bucle de mensajes mediante las [**funciones GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) Si la aplicación debe obtener la entrada de caracteres del usuario, incluya la [**función TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) en el bucle . **TranslateMessage** traduce los mensajes de clave virtual en mensajes de caracteres. En el ejemplo siguiente se muestra el bucle de mensajes [**en la función WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de una aplicación Windows aplicación sencilla.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



En el ejemplo siguiente se muestra un bucle de mensajes para un subproceso que usa aceleradores y muestra un cuadro de diálogo no modelo. Cuando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) o [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) devuelve **TRUE** (lo que indica que se ha procesado el mensaje), no se llama a [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) El motivo es que **TranslateAccelerator** e **IsDialogMessage** realizan todas las operaciones necesarias de traducción y distribución de mensajes.


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a>Examinar una cola de mensajes

En ocasiones, una aplicación debe examinar el contenido de la cola de mensajes de un subproceso desde fuera del bucle de mensajes del subproceso. Por ejemplo, si el procedimiento de ventana de una aplicación realiza una operación de dibujo larga, es posible que desee que el usuario pueda interrumpir la operación. A menos que la aplicación examine periódicamente la cola de mensajes durante la operación para los mensajes del mouse y el teclado, no responderá a la entrada del usuario hasta que se haya completado la operación. El motivo es que la función [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) del bucle de mensajes del subproceso no se devuelve hasta que el procedimiento de ventana termina de procesar un mensaje.

Puede usar la función [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar una cola de mensajes durante una operación larga. **PeekMessage** es similar a la [**función GetMessage;**](/windows/win32/api/winuser/nf-winuser-getmessage) ambos comprueban una cola de mensajes para un mensaje que coincida con los criterios de filtro y, a continuación, copian el mensaje en una [**estructura MSG.**](/windows/win32/api/winuser/ns-winuser-msg) La principal diferencia entre las dos funciones es que **GetMessage** no devuelve hasta que un mensaje que coincide con los criterios de filtro se coloca en la cola, mientras que **PeekMessage** devuelve inmediatamente independientemente de si un mensaje está en la cola.

En el ejemplo siguiente se muestra cómo usar [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) para examinar una cola de mensajes para los clics del mouse y la entrada del teclado durante una operación larga.


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



Otras funciones, [**como GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) y [**GetInputState,**](/windows/win32/api/winuser/nf-winuser-getinputstate)también permiten examinar el contenido de la cola de mensajes de un subproceso. **GetQueueStatus** devuelve una matriz de marcas que indica los tipos de mensajes de la cola; es la manera más rápida de detectar si la cola contiene algún mensaje. **GetInputState devuelve** **TRUE si** la cola contiene mensajes del mouse o del teclado. Ambas funciones se pueden usar para determinar si la cola contiene mensajes que deben procesarse.

## <a name="posting-a-message"></a>Publicar un mensaje

Puede publicar un mensaje en una cola de mensajes mediante la [**función PostMessage.**](/windows/win32/api/winuser/nf-winuser-postmessagea) **PostMessage** coloca un mensaje al final de la cola de mensajes de un subproceso y vuelve inmediatamente, sin esperar a que el subproceso procese el mensaje. Los parámetros de la función incluyen un identificador de ventana, un identificador de mensaje y dos parámetros de mensaje. El sistema copia estos parámetros en una estructura [**MSG,**](/windows/win32/api/winuser/ns-winuser-msg) rellena los miembros **time** y **pt** de la estructura y coloca la estructura en la cola de mensajes.

El sistema usa el identificador de ventana pasado con la [**función PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para determinar qué cola de mensajes de subproceso debe recibir el mensaje. Si el identificador es **HWND \_ TOPMOST,** el sistema envía el mensaje a las colas de mensajes de subproceso de todas las ventanas de nivel superior.

Puede usar la función [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) para publicar un mensaje en una cola de mensajes de subproceso específica. **PostThreadMessage** es similar a [**PostMessage,**](/windows/win32/api/winuser/nf-winuser-postmessagea)salvo que el primer parámetro es un identificador de subproceso en lugar de un identificador de ventana. Puede recuperar el identificador del subproceso llamando a [**la función GetCurrentThreadId.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)

Use la [**función PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para salir de un bucle de mensajes. **PostQuitMessage publica** el mensaje [**DE SALIDA \_ de WM**](wm-quit.md) en el subproceso que se está ejecutando actualmente. El bucle de mensajes del subproceso finaliza y devuelve el control al sistema cuando encuentra el **mensaje \_ QUIT de WM.** Normalmente, una aplicación llama **a PostQuitMessage** en respuesta al mensaje [**WM \_ DESTROY,**](wm-destroy.md) como se muestra en el ejemplo siguiente.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Envío de un mensaje

La [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) se usa para enviar un mensaje directamente a un procedimiento de ventana. **SendMessage** llama a un procedimiento de ventana y espera a que ese procedimiento procese el mensaje y devuelva un resultado.

Se puede enviar un mensaje a cualquier ventana del sistema; todo lo que se necesita es un identificador de ventana. El sistema usa el identificador para determinar qué procedimiento de ventana debe recibir el mensaje.

Antes de procesar un mensaje que se puede haber enviado desde otro subproceso, un procedimiento de ventana debe llamar primero a la [**función InSendMessage.**](/windows/win32/api/winuser/nf-winuser-insendmessage) Si esta función devuelve **TRUE**, el procedimiento de ventana debe llamar a [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) antes de cualquier función que haga que el subproceso devuelva el control, como se muestra en el ejemplo siguiente.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



Se pueden enviar varios mensajes a los controles de un cuadro de diálogo. Estos mensajes de control establecen la apariencia, el comportamiento y el contenido de los controles o recuperan información sobre los controles. Por ejemplo, el mensaje [**\_ CB ADDSTRING**](../controls/cb-addstring.md) puede agregar una cadena a un cuadro combinado y el mensaje [**BM \_ SETCHECK**](../controls/bm-setcheck.md) puede establecer el estado de una casilla o un botón de radio.

Use la [**función SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) para enviar un mensaje a un control, especificando el identificador del control y el identificador de la ventana del cuadro de diálogo que contiene el control. En el ejemplo siguiente, tomado de un procedimiento de cuadro de diálogo, se copia una cadena del control de edición de un cuadro combinado en su cuadro de lista. En el ejemplo **se usa SendDlgItemMessage** para enviar un mensaje [**\_ ADDSTRING de CB**](../controls/cb-addstring.md) al cuadro combinado.


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
