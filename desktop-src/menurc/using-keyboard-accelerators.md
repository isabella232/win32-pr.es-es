---
title: Usar aceleradores de teclado
description: En esta sección se describen las tareas que están asociadas a los aceleradores de teclado.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrada de usuario, aceleradores de teclado
- captura de entradas de usuario, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- tablas de aceleradores
- 'Acelerador: recursos de tabla'
- translate (función de acelerador)
- Mensaje WM_COMMAND
- WM_SYS mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077739"
---
# <a name="using-keyboard-accelerators"></a>Usar aceleradores de teclado

En esta sección se describen las tareas que están asociadas a los aceleradores de teclado.

-   [Uso de un recurso de tabla de aceleradores](#using-an-accelerator-table-resource)
    -   [Crear el recurso de tabla de aceleradores](#creating-the-accelerator-table-resource)
    -   [Cargar el recurso de tabla de aceleradores](#loading-the-accelerator-table-resource)
    -   [Llamar a la función de acelerador translate](#calling-the-translate-accelerator-function)
    -   [Procesamiento de \_ mensajes de comandos de WM](/windows)
    -   [Destruir el recurso de tabla de aceleradores](#destroying-the-accelerator-table-resource)
    -   [Crear aceleradores para atributos de fuente](#creating-accelerators-for-font-attributes)
-   [Usar una tabla de aceleradores creada en tiempo de ejecución](#using-an-accelerator-table-created-at-run-time)
    -   [Creación de una tabla de aceleradores de Run-Time](#creating-a-run-time-accelerator-table)
    -   [Aceleradores de procesamiento](#processing-accelerators)
    -   [Destruir una tabla de aceleradores de Run-Time](#destroying-a-run-time-accelerator-table)
    -   [Creación de aceleradores editables por el usuario](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Uso de un recurso de tabla de aceleradores

La forma más común de agregar compatibilidad con el acelerador a una aplicación consiste en incluir un recurso de tabla de aceleradores con el archivo ejecutable de la aplicación y, a continuación, cargar el recurso en tiempo de ejecución.

En esta sección se tratan los temas siguientes.

-   [Crear el recurso de tabla de aceleradores](#creating-the-accelerator-table-resource)
-   [Cargar el recurso de tabla de aceleradores](#loading-the-accelerator-table-resource)
-   [Llamar a la función de acelerador translate](#calling-the-translate-accelerator-function)
-   [Procesamiento de \_ mensajes de comandos de WM](/windows)
-   [Destruir el recurso de tabla de aceleradores](#destroying-the-accelerator-table-resource)
-   [Crear aceleradores para atributos de fuente](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Crear el recurso de tabla de aceleradores

Cree un recurso de tabla de aceleradores mediante la instrucción [Accelerators](./accelerators-resource.md) en el archivo de definición de recursos de la aplicación. Debe asignar un nombre o un identificador de recurso a la tabla de aceleradores, preferiblemente a diferencia de la de cualquier otro recurso. El sistema utiliza este identificador para cargar el recurso en tiempo de ejecución.

Cada acelerador que defina requiere una entrada independiente en la tabla de aceleradores. En cada entrada, se define la pulsación de tecla (un código de carácter ASCII o un código de tecla virtual) que genera el acelerador y el identificador del acelerador. También debe especificar si se debe utilizar la pulsación de tecla en alguna combinación con las teclas ALT, Mayús o CTRL. Para obtener más información acerca de las claves virtuales, consulte [entrada de teclado](/windows/desktop/inputdev/keyboard-input).

Una pulsación de tecla ASCII se especifica mediante la inclusión del carácter ASCII entre comillas dobles o mediante el valor entero del carácter en combinación con la marca ASCII. En los siguientes ejemplos se muestra cómo definir aceleradores ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Una pulsación de tecla de código de tecla virtual se especifica de manera diferente en función de si la pulsación de tecla es una clave alfanumérica o una clave no alfanumérica. En el caso de una clave alfanumérica, la letra o el número de la clave, entre comillas dobles, se combina con la marca **VIRTKEY** . En el caso de una clave no alfanumérica, el código de la clave virtual para la clave específica se combina con la marca **VIRTKEY** . En los siguientes ejemplos se muestra cómo definir aceleradores de código de clave virtual.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

En el ejemplo siguiente se muestra un recurso de tabla de aceleradores que define los aceleradores para las operaciones de archivos. El nombre del recurso es *FileAccel*.

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Si desea que el usuario presione las teclas ALT, Mayús o CTRL en alguna combinación con la pulsación de tecla del acelerador, especifique las marcas ALT, Mayús y CONTROL en la definición del acelerador. A continuación se muestran algunos ejemplos.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

De forma predeterminada, cuando una tecla de aceleración corresponde a un elemento de menú, el sistema resalta el elemento de menú. Puede usar la marca **noinvertir** para evitar el resaltado de un acelerador individual. En el ejemplo siguiente se muestra cómo usar la marca **Invert** :

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Para definir los aceleradores que corresponden a los elementos de menú de la aplicación, incluya los aceleradores en el texto de los elementos de menú. En el ejemplo siguiente se muestra cómo incluir los aceleradores en el texto de elementos de menú en un archivo de definición de recursos.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Cargar el recurso de tabla de aceleradores

Una aplicación carga un recurso de tabla de aceleradores mediante una llamada a la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) y especificando el identificador de instancia de la aplicación cuyo archivo ejecutable contiene el recurso y el nombre o el identificador del recurso. **LoadAccelerators** carga la tabla de aceleradores especificada en la memoria y devuelve el identificador a la tabla de aceleradores.

Una aplicación puede cargar un recurso de tabla de aceleradores en cualquier momento. Normalmente, una aplicación de un solo subproceso carga su tabla de aceleradores antes de escribir su bucle de mensajes principal. Una aplicación que usa varios subprocesos normalmente carga el recurso de tabla de aceleradores para un subproceso antes de escribir el bucle de mensajes para el subproceso. Una aplicación o un subproceso también puede usar varias tablas de aceleradores, cada una de las cuales está asociada a una ventana determinada de la aplicación. Este tipo de aplicación cargaría la tabla de aceleradores para la ventana cada vez que el usuario activara la ventana. Para obtener más información sobre los subprocesos, vea [procesos y subprocesos](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Llamar a la función de acelerador translate

Para procesar aceleradores, el bucle de mensajes de una aplicación (o del subproceso) debe contener una llamada a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . **TranslateAccelerator** compara las pulsaciones de teclas con una tabla de aceleradores y, si encuentra una coincidencia, traduce las pulsaciones de teclas en un mensaje de [**\_ comando WM**](wm-command.md) (o [**WM \_ SYSCOMMAND**](wm-syscommand.md)). A continuación, la función envía el mensaje a un procedimiento de ventana. Los parámetros de la función **TranslateAccelerator** incluyen el identificador de la ventana que va a recibir los mensajes de **\_ comandos de WM** , el identificador de la tabla de aceleradores que se usa para traducir los aceleradores y un puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene un mensaje de la cola. En el ejemplo siguiente se muestra cómo llamar a **TranslateAccelerator** desde dentro de un bucle de mensajes.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Procesamiento de \_ mensajes de comandos de WM

Cuando se utiliza un acelerador, la ventana especificada en la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) recibe [**un \_ comando de WM**](wm-command.md) o un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) . La palabra de orden inferior del parámetro *wParam* contiene el identificador del acelerador. El procedimiento de ventana examina el identificador para determinar el origen del mensaje de **\_ comando de WM** y procesar el mensaje en consecuencia.

Normalmente, si un acelerador corresponde a un elemento de menú de la aplicación, se asigna el mismo identificador al acelerador y al elemento de menú. Si necesita saber si un mensaje de [**\_ comando de WM**](wm-command.md) se generó mediante un acelerador o un elemento de menú, puede examinar la palabra de orden superior del parámetro *wParam* . Si un acelerador generó el mensaje, la palabra de orden superior es 1; Si un elemento de menú ha generado el mensaje, la palabra de orden superior es 0.

### <a name="destroying-the-accelerator-table-resource"></a>Destruir el recurso de tabla de aceleradores

El sistema destruye automáticamente los recursos de la tabla de aceleradores cargados por la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , quitando el recurso de la memoria después de que se cierre la aplicación.

### <a name="creating-accelerators-for-font-attributes"></a>Crear aceleradores para atributos de fuente

En el ejemplo de esta sección se muestra cómo realizar las tareas siguientes:

-   Cree un recurso de tabla de aceleradores.
-   Cargue la tabla de aceleradores en tiempo de ejecución.
-   Traduzca los aceleradores en un bucle de mensajes.
-   Procese los mensajes de [**\_ comandos de WM**](wm-command.md) generados por los aceleradores.

Estas tareas se muestran en el contexto de una aplicación que incluye un menú de **caracteres** y los aceleradores correspondientes que permiten al usuario seleccionar atributos de la fuente actual.

La siguiente parte de un archivo de definición de recursos define el menú de **caracteres** y la tabla de aceleradores asociada. Tenga en cuenta que los elementos de menú muestran las pulsaciones de teclas de aceleración y que cada acelerador tiene el mismo identificador que el elemento de menú asociado.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



En las secciones siguientes del archivo de código fuente de la aplicación se muestra cómo implementar los aceleradores.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Usar una tabla de aceleradores creada en tiempo de ejecución

En este tema se describe cómo usar las tablas de aceleradores creadas en tiempo de ejecución.

-   [Creación de una tabla de aceleradores de Run-Time](#creating-a-run-time-accelerator-table)
-   [Aceleradores de procesamiento](#processing-accelerators)
-   [Destruir una tabla de aceleradores de Run-Time](#destroying-a-run-time-accelerator-table)
-   [Creación de aceleradores editables por el usuario](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Creación de una tabla de aceleradores de Run-Time

El primer paso para crear una tabla de aceleradores en tiempo de ejecución es llenar una matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) . Cada estructura de la matriz define un acelerador en la tabla. La definición de un acelerador incluye sus marcas, su clave y su identificador. La estructura de **aceleración** tiene el formato siguiente.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Para definir la pulsación de tecla del acelerador, especifique un código de carácter ASCII o un código de clave virtual en el miembro **clave** de la estructura de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) . Si especifica un código de tecla virtual, primero debe incluir la marca **FVIRTKEY** en el miembro **fVirt** ; de lo contrario, el sistema interpreta el código como un código de carácter ASCII. Puede incluir las marcas **FCONTROL**, **FALT** o **FSHIFT** , o las tres, para combinar las teclas Ctrl, Alt o Mayús con la pulsación de tecla.

Para crear la tabla de aceleradores, pase un puntero a la matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) a la función [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . **CreateAcceleratorTable** crea la tabla de aceleradores y devuelve el identificador de la tabla.

### <a name="processing-accelerators"></a>Aceleradores de procesamiento

El proceso de cargar y llamar a los aceleradores proporcionados por una tabla de aceleradores creada en tiempo de ejecución es igual que el procesamiento de los proporcionados por un recurso de tabla de aceleradores. Para obtener más información, vea [cargar el recurso de tabla de aceleradores](#loading-the-accelerator-table-resource) mediante el [procesamiento de mensajes de \_ comandos de WM](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Destruir una tabla de aceleradores de Run-Time

El sistema destruye automáticamente las tablas de acelerador creadas en tiempo de ejecución y quita los recursos de la memoria después de que se cierre la aplicación. Puede destruir una tabla de aceleradores y quitarla de la memoria antes si pasa el identificador de la tabla a la función [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

### <a name="creating-user-editable-accelerators"></a>Creación de aceleradores editables por el usuario

En este ejemplo se muestra cómo crear un cuadro de diálogo que permite al usuario cambiar el acelerador asociado a un elemento de menú. El cuadro de diálogo se compone de un cuadro combinado que contiene elementos de menú, un cuadro combinado que contiene los nombres de las teclas y casillas para seleccionar las teclas CTRL, ALT y Mayús. En la ilustración siguiente se muestra el cuadro de diálogo.

![cuadro de diálogo con cuadros combinados y casillas](images/useredit.gif)

En el ejemplo siguiente se muestra cómo se define el cuadro de diálogo en el archivo de definición de recursos.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

La barra de menús de la aplicación contiene un submenú de **caracteres** cuyos elementos tienen aceleradores asociados.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

Los valores de elemento de menú de la plantilla de menú son constantes que se definen como se indica a continuación en el archivo de encabezado de la aplicación.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

El cuadro de diálogo utiliza una matriz de estructuras VKEY definidas por la aplicación, cada una de las cuales contiene una cadena de texto de pulsación de tecla y una cadena de texto acelerador. Cuando se crea el cuadro de diálogo, analiza la matriz y agrega cada cadena de texto de pulsación de tecla al cuadro combinado de **pulsación de tecla** . Cuando el usuario hace clic en el botón **Aceptar** , el cuadro de diálogo busca la cadena de texto de pulsación de tecla seleccionada y recupera la cadena de texto de acelerador correspondiente. El cuadro de diálogo anexa la cadena de texto del acelerador al texto del elemento de menú seleccionado por el usuario. En el ejemplo siguiente se muestra la matriz de estructuras VKEY:


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



El procedimiento de inicialización del cuadro de diálogo rellena los cuadros de la combinación **Seleccionar elemento** y **seleccionar pulsación de tecla** . Una vez que el usuario selecciona un elemento de menú y el acelerador asociado, el cuadro de diálogo examina los controles del cuadro de diálogo para obtener la selección del usuario, actualiza el texto del elemento de menú y, a continuación, crea una nueva tabla de aceleradores que contiene el nuevo acelerador definido por el usuario. En el ejemplo siguiente se muestra el procedimiento de cuadro de diálogo. Tenga en cuenta que debe inicializar en el procedimiento de ventana.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 