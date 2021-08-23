---
description: En esta sección se explica cómo realizar tareas asociadas a la interfaz de varios documentos.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Uso de la interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09453e6f4a9301c8cdfc9d675ae1efd7853594fc472a446a021e3bd3e075fc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028333"
---
# <a name="using-the-multiple-document-interface"></a>Uso de la interfaz de varios documentos

En esta sección se explica cómo realizar las siguientes tareas:

-   [Registro de clases secundarias y de ventana de marco](#registering-child-and-frame-window-classes)
-   [Crear fotogramas y elementos Windows](#creating-frame-and-child-windows)
-   [Escribir el bucle de mensajes principal](#writing-the-main-message-loop)
-   [Escribir el procedimiento de ventana marco](#writing-the-frame-window-procedure)
-   [Escribir el procedimiento de ventana secundaria](#writing-the-child-window-procedure)
-   [Crear una ventana secundaria](#creating-a-child-window)

Para ilustrar estas tareas, en esta sección se incluyen ejemplos de Multipad, una aplicación de interfaz de múltiples documentos (MDI) típica.

## <a name="registering-child-and-frame-window-classes"></a>Registro de clases secundarias y de ventana de marco

Una aplicación MDI típica debe registrar dos clases de ventana: una para su ventana de marco y otra para sus ventanas secundarias. Si una aplicación admite más de un tipo de documento (por ejemplo, una hoja de cálculo y un gráfico), debe registrar una clase de ventana para cada tipo.

La estructura de clase de la ventana de marco es similar a la estructura de clase de la ventana principal en aplicaciones que no son MDI. La estructura de clase de las ventanas secundarias MDI difiere ligeramente de la estructura de las ventanas secundarias en aplicaciones que no son MDI como se muestra a continuación:

-   La estructura de clase debe tener un icono, ya que el usuario puede minimizar una ventana secundaria MDI como si fuera una ventana de aplicación normal.
-   El nombre del menú debe ser **NULL,** porque una ventana secundaria MDI no puede tener su propio menú.
-   La estructura de clase debe reservar espacio adicional en la estructura de la ventana. Con este espacio, la aplicación puede asociar datos, como un nombre de archivo, a una ventana secundaria determinada.

En el ejemplo siguiente se muestra cómo Multipad registra sus clases de marco y ventana secundaria.


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a>Creación de fotogramas y elementos Windows

Después de registrar sus clases de ventana, una aplicación MDI puede crear sus ventanas. En primer lugar, crea su ventana de marco mediante la [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Después de crear su ventana de marco, la aplicación crea su ventana cliente, de nuevo mediante **CreateWindow** o **CreateWindowEx.** La aplicación debe especificar MDICLIENT como nombre de clase de la ventana de cliente; **MDICLIENT** es una clase de ventana registrada previamente definida por el sistema. El *parámetro lpvParam* de **CreateWindow** o **CreateWindowEx** debe apuntar a una [**estructura CLIENTCREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) Esta estructura contiene los miembros descritos en la tabla siguiente:



| Miembro           | Descripción                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | Identificador del menú de ventana utilizado para controlar las ventanas secundarias MDI. A medida que se crean ventanas secundarias, la aplicación agrega sus títulos al menú de la ventana como elementos de menú. A continuación, el usuario puede activar una ventana secundaria haciendo clic en su título en el menú de la ventana.                                                               |
| **idFirstChild** | Especifica el identificador de la primera ventana secundaria MDI. A la primera ventana secundaria MDI creada se le asigna este identificador. Se crean ventanas adicionales con identificadores de ventana incrementados. Cuando se destruye una ventana secundaria, el sistema reasigna inmediatamente los identificadores de ventana para mantener su intervalo contiguo. |



 

Cuando se agrega el título de una ventana secundaria al menú de la ventana, el sistema asigna un identificador a la ventana secundaria. Cuando el usuario hace clic en el título de una ventana secundaria, la ventana de marco recibe un mensaje [**WM \_ COMMAND**](../menurc/wm-command.md) con el identificador en el *parámetro wParam.* Debe especificar un valor para el **miembro idFirstChild** que no entre en conflicto con los identificadores de elemento de menú en el menú de la ventana de marco.

El procedimiento de ventana de marco de Multipad crea la ventana de cliente MDI al procesar el [**mensaje WM \_ CREATE.**](wm-create.md) En el ejemplo siguiente se muestra cómo se crea la ventana de cliente.


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



Los títulos de las ventanas secundarias se agregan a la parte inferior del menú de la ventana. Si la aplicación agrega cadenas al menú de la ventana mediante la función [**AppendMenu,**](/windows/win32/api/winuser/nf-winuser-appendmenua) estas cadenas se pueden sobrescribir con los títulos de las ventanas secundarias cuando se vuelve a dibujar el menú de la ventana (siempre que se crea o destruye una ventana secundaria). Una aplicación MDI que agrega cadenas a su menú de ventana debe usar la función [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) y comprobar que los títulos de las ventanas secundarias no han sobrescrito estas nuevas cadenas.

Use el **estilo \_ CLIPCHILDREN de WS** para crear la ventana de cliente MDI para evitar que la ventana se pinte sobre sus ventanas secundarias.

## <a name="writing-the-main-message-loop"></a>Escribir el bucle de mensajes principal

El bucle de mensajes principal de una aplicación MDI es similar al de las teclas de aceleración de control de aplicaciones que no son MDI. La diferencia es que el bucle de mensajes MDI llama a la función [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) antes de comprobar las teclas de aceleración definidas por la aplicación o antes de enviar el mensaje.

En el ejemplo siguiente se muestra el bucle de mensajes de una aplicación MDI típica. Tenga en [**cuenta que GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) puede devolver -1 si se produce un error.


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



La [**función TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) traduce los mensajes [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) en mensajes [**\_ SYSCOMMAND**](../menurc/wm-syscommand.md) de WM y los envía a la ventana secundaria MDI activa. Si el mensaje no es un mensaje de acelerador MDI, la función devuelve **FALSE,** en cuyo caso la aplicación usa la función [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) para determinar si se presionó alguna de las teclas de aceleración definidas por la aplicación. Si no es así, el bucle envía el mensaje al procedimiento de ventana adecuado.

## <a name="writing-the-frame-window-procedure"></a>Escribir el procedimiento de ventana marco

El procedimiento de ventana para una ventana de marco MDI es similar al de la ventana principal de una aplicación que no es MDI. La diferencia es que un procedimiento de ventana de marco pasa todos los mensajes que no controla a la función [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) en lugar de a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Además, el procedimiento de ventana de marco también debe pasar algunos mensajes que controla, incluidos los enumerados en la tabla siguiente.



| Message                                  | Response                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO \_ WM**](../menurc/wm-command.md)     | Activa la ventana secundaria MDI que el usuario elige. Este mensaje se envía cuando el usuario elige una ventana secundaria MDI en el menú de ventana de la ventana marco MDI. El identificador de ventana que acompaña a este mensaje identifica la ventana secundaria MDI que se va a activar. |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)   | Abre el menú de ventana de la ventana secundaria MDI activa cuando el usuario presiona la combinación de teclas ALT+ - (menos).                                                                                                                                                      |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md) | Pasa el foco del teclado a la ventana del cliente MDI, que a su vez lo pasa a la ventana secundaria MDI activa.                                                                                                                                                         |
| [**TAMAÑO \_ DE WM**](wm-size.md)              | Cambia el tamaño de la ventana de cliente MDI para que quepa en el área de cliente de la nueva ventana de marco. Si el procedimiento de ventana de marco puede cambiar el tamaño de la ventana de cliente MDI, no debe pasar el mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)                   |



 

El procedimiento de ventana de marco en Multipad se denomina MPFrameWndProc. El control de otros mensajes por MPFrameWndProc es similar al de las aplicaciones que no son MDI. [**WM \_ Los**](../menurc/wm-command.md) mensajes COMMAND de Multipad se controlan mediante la función CommandHandler definida localmente. Para los mensajes de comando que Multipad no controla, CommandHandler llama a la [**función DefFrameProc.**](/windows/win32/api/winuser/nf-winuser-defframeproca) Si Multipad no usa **DefFrameProc** de forma predeterminada, el usuario no puede activar una ventana secundaria desde el menú de la ventana, ya que se perdería el mensaje **WM \_ COMMAND** enviado al hacer clic en el elemento de menú de la ventana.

## <a name="writing-the-child-window-procedure"></a>Escribir el procedimiento de ventana secundaria

Al igual que el procedimiento de ventana de marco, un procedimiento de ventana secundaria MDI usa una función especial para procesar mensajes de forma predeterminada. Todos los mensajes que el procedimiento de ventana secundaria no controla deben pasarse a la función [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) en lugar de a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Además, algunos mensajes de administración de ventanas se deben pasar **a DefMDIChildProc**, incluso si la aplicación controla el mensaje, para que MDI funcione correctamente. Estos son los mensajes que la aplicación debe pasar **a DefMDIChildProc**.



| Message                                       | Response                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHILDACTIVATE**](wm-childactivate.md) | Realiza el procesamiento de activación cuando las ventanas secundarias MDI tienen tamaño, se mueven o se muestran. Se debe pasar este mensaje.                                                                                                                                        |
| [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) | Calcula el tamaño de una ventana secundaria MDI maximizada, en función del tamaño actual de la ventana de cliente MDI.                                                                                                                                                  |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)        | Pasa el mensaje a la ventana de marco MDI.                                                                                                                                                                                                               |
| [**WM \_ MOVE**](wm-move.md)                   | Vuelve a calcular las barras de desplazamiento del cliente MDI, si están presentes.                                                                                                                                                                                                 |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)      | Activa la ventana secundaria, si no es la ventana secundaria MDI activa.                                                                                                                                                                                     |
| [**TAMAÑO \_ DE WM**](wm-size.md)                   | Realiza las operaciones necesarias para cambiar el tamaño de una ventana, especialmente para maximizar o restaurar una ventana secundaria MDI. Si no se pasa este mensaje a la [**función DefMDIChildProc,**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) se generan resultados muy no deseados. |
| [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md)    | Controla los comandos de menú de ventana (anteriormente conocido como sistema): **SC \_ NEXTWINDOW,** **SC \_ PREVWINDOW,** **SC \_ MOVE,** **SC \_ SIZE** y **SC \_ MAXIMIZE.**                                                                                                        |



 

## <a name="creating-a-child-window"></a>Crear una ventana secundaria

Para crear una ventana secundaria MDI, una aplicación puede llamar a la función [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o enviar un mensaje [**\_ WM MDICREATE**](wm-mdicreate.md) a la ventana de cliente MDI. (La aplicación puede usar la [**función CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con el estilo **\_ \_ MDICHILD** de WS EX para crear ventanas secundarias MDI). Una aplicación MDI de un solo subproceso puede usar cualquiera de los métodos para crear una ventana secundaria. Un subproceso de una aplicación MDI multiproceso debe usar las funciones **CreateMDIWindow** o **CreateWindowEx** para crear una ventana secundaria en un subproceso diferente.

El *parámetro lParam* de un [**mensaje WM \_ MDICREATE**](wm-mdicreate.md) es un puntero lejano a una [**estructura MDICREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) La estructura incluye cuatro miembros de dimensión: **x** e **y**, que indican las posiciones horizontal y vertical de la ventana, y **cx** y **cy**, que indican las extensiones horizontal y vertical de la ventana. La aplicación puede asignar explícitamente cualquiera de estos miembros, o se pueden establecer en **CW \_ USEDEFAULT**, en cuyo caso el sistema selecciona una posición, un tamaño o ambos, según un algoritmo en cascada. En cualquier caso, se deben inicializar los cuatro miembros. Multipad usa **CW \_ USEDEFAULT** para todas las dimensiones.

El último miembro de la [**estructura MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) es el miembro **de** estilo, que puede contener bits de estilo para la ventana. Para crear una ventana secundaria MDI que pueda tener cualquier combinación de estilos de ventana, especifique el estilo de ventana **MDIS \_ ALLCHILDSTYLES.** Cuando no se especifica este estilo, una ventana secundaria MDI tiene los estilos **WS \_ MINIMIZE**, **WS \_ MAXIMIZE,** **WS \_ HSCROLL** y **WS \_ VSCROLL** como valores predeterminados.

Multipad crea sus ventanas secundarias MDI mediante su función AddFile definida localmente (ubicada en el archivo de origen MPFILE. C). La función AddFile establece el título de la ventana secundaria asignando el miembro **szTitle** de la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) de la ventana al nombre del archivo que se está editando o a "Sin título". El **miembro szClass** se establece en el nombre de la clase de ventana secundaria MDI registrada en la función InitializeApplication de Multipad. El **miembro hOwner** se establece en el identificador de instancia de la aplicación.

En el ejemplo siguiente se muestra la función AddFile en Multipad.


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



El puntero pasado en el parámetro *lParam* del mensaje [**\_ WM MDICREATE**](wm-mdicreate.md) se pasa a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) y aparece como el primer miembro de la estructura [**CREATESTRUCT,**](/windows/win32/api/winuser/ns-winuser-createstructa) pasado en el [**mensaje WM \_ CREATE.**](wm-create.md) En Multipad, la ventana secundaria se inicializa durante el procesamiento de mensajes **WM \_ CREATE** inicializando variables de documento en sus datos adicionales y creando la ventana secundaria del control de edición.

 

 
