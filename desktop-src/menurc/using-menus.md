---
title: Uso de los menús
description: En esta sección se proporcionan ejemplos de código para las tareas relacionadas con los menús.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- resources,menus
- menús, crear
- recursos de plantilla de menú
- resources,menu-template
- formato de plantilla de menú extendido
- formato de plantilla de menú antiguo
- carga de recursos de plantilla de menú
- menus,class
- menús, acceso directo
- crear menús
- menús de clase
- menús contextuales
- mapas de bits de elementos de menú
- menús, propietario dibujado
- menús dibujados por el propietario
- mapas de bits de marca de verificación personalizados
- menús, casillas
- menús, fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3a71a580a323fa2058613f8c9a14d9c2782bd3ba139e5d182750e5047fe74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971934"
---
# <a name="using-menus"></a>Uso de los menús

En esta sección se describen las siguientes tareas:

-   [Uso de un Menu-Template compartido](#using-a-menu-template-resource)
    -   [Formato de Menu-Template extendido](#extended-menu-template-format)
    -   [Formato Menu-Template anterior](#old-menu-template-format)
    -   [Carga de un recurso Menu-Template carga](#loading-a-menu-template-resource)
    -   [Menú Crear una clase](#creating-a-class-menu)
-   [Crear un menú contextual](#creating-a-shortcut-menu)
    -   [Procesamiento del mensaje \_ CONTEXTMENU de WM](/windows)
    -   [Crear un menú contextual Font-Attributes acceso directo](#creating-a-shortcut-font-attributes-menu)
    -   [Mostrar un menú contextual](#displaying-a-shortcut-menu)
-   [Uso de Menu-Item mapa de bits](#using-menu-item-bitmaps)
    -   [Establecer la marca de tipo de mapa de bits](#setting-the-bitmap-type-flag)
    -   [Creación del mapa de bits](#creating-the-bitmap)
    -   [Agregar líneas y gráficos a un menú](#adding-lines-and-graphs-to-a-menu)
    -   [Ejemplo de mapas Menu-Item mapa de bits](#example-of-menu-item-bitmaps)
-   [Crear elementos Owner-Drawn menú](#creating-owner-drawn-menu-items)
    -   [Establecimiento de la Owner-Drawn marcador](#setting-the-owner-drawn-flag)
    -   [Menús dibujados por el propietario y el mensaje \_ MEASUREITEM de WM](/windows)
    -   [Menús dibujados por el propietario y el mensaje \_ DRAWITEM de WM](/windows)
    -   [Menús dibujados por el propietario y el mensaje \_ MENUCHAR de WM](/windows)
    -   [Establecimiento de fuentes para Menu-Item cadenas de texto](#setting-fonts-for-menu-item-text-strings)
    -   [Ejemplo de elementos Owner-Drawn menú](#example-of-owner-drawn-menu-items)
-   [Uso de mapas de bits de marca de verificación personalizados](#using-custom-check-mark-bitmaps)
    -   [Crear mapas de bits de marca de verificación personalizados](#creating-custom-check-mark-bitmaps)
    -   [Asociación de mapas de bits a un elemento de menú](#associating-bitmaps-with-a-menu-item)
    -   [Establecimiento del atributo check-mark](#setting-the-check-mark-attribute)
    -   [Simulación de casillas en un menú](#simulating-check-boxes-in-a-menu)
    -   [Ejemplo de uso de mapas de bits de marca de verificación personalizados](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Uso de un Menu-Template compartido

Normalmente se incluye un menú en una aplicación mediante la creación de un recurso de plantilla de menú y, a continuación, la carga del menú en tiempo de ejecución. En esta sección se describe el formato de una plantilla de menú y se explica cómo cargar un recurso de plantilla de menú y usarlo en la aplicación. Para obtener información sobre cómo crear un recurso de plantilla de menú, consulte la documentación incluida con las herramientas de desarrollo.

-   [Formato de Menu-Template extendido](#extended-menu-template-format)
-   [Formato Menu-Template anterior](#old-menu-template-format)
-   [Carga de un recurso Menu-Template carga](#loading-a-menu-template-resource)
-   [Menú Crear una clase](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Formato de Menu-Template extendido

El formato de plantilla de menú extendido admite funcionalidad de menú adicional. Al igual que los recursos estándar de plantilla de menú, los recursos extendidos de plantilla de menú tienen el tipo de recurso **\_ RT MENU.** El sistema distingue los dos formatos de recurso por el número de versión, que es el primer miembro del encabezado del recurso.

Una plantilla de menú extendida consta de una estructura [**MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguida de otras estructuras de definición de elementos [**MENUEX \_ TEMPLATE \_ ITEM.**](menuex-template-item.md)

### <a name="old-menu-template-format"></a>Formato Menu-Template anterior

Una plantilla de menú antigua (Microsoft Windows NT 3.51 y versiones anteriores) define un menú, pero no admite la nueva funcionalidad de menú. Un recurso de plantilla de menú antiguo tiene el **tipo de recurso RT \_ MENU.**

Una plantilla de menú antigua consta de una [**estructura MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida de una o varias [**estructuras MENUITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

### <a name="loading-a-menu-template-resource"></a>Carga de un Menu-Template de carga

Para cargar un recurso de plantilla de menú, use la función [**LoadMenu,**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) especificando un identificador para el módulo que contiene el recurso y el identificador de la plantilla de menú. La **función LoadMenu** devuelve un identificador de menú que puede usar para asignar el menú a una ventana. Esta ventana se convierte en la ventana del propietario del menú y recibe todos los mensajes generados por el menú.

Para crear un menú a partir de una plantilla de menú que ya está en memoria, use la [**función LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) Esto resulta útil si la aplicación genera plantillas de menú dinámicamente.

Para asignar un menú a una ventana, use la función [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) o especifique el identificador del menú en el *parámetro hMenu* de la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) al crear una ventana. Otra manera de asignar un menú a una ventana es especificar una plantilla de menú al registrar una clase de ventana; la plantilla identifica el menú especificado como menú de clase para esa clase de ventana.

Para que el sistema asigne automáticamente un menú específico a una ventana, especifique la plantilla del menú al registrar la clase de la ventana. La plantilla identifica el menú especificado como menú de clase para esa clase de ventana. A continuación, al crear una ventana de la clase especificada, el sistema asigna automáticamente el menú especificado a la ventana.

No se puede asignar un menú a una ventana que sea una ventana secundaria.

Para crear un menú de clase, incluya el identificador del recurso de plantilla de menú como miembro **lpszMenuName** de una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) y, a continuación, pase un puntero a la estructura a la [**función RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)

### <a name="creating-a-class-menu"></a>Menú Crear una clase

En el ejemplo siguiente se muestra cómo crear un menú de clases para una aplicación, crear una ventana que use el menú clase y procesar comandos de menú en el procedimiento de ventana.

A continuación se muestra la parte pertinente del archivo de encabezado de la aplicación:


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



A continuación se encuentran las partes pertinentes de la propia aplicación:


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a>Crear un menú contextual

Para usar un menú contextual en una aplicación, pase su identificador a la [**función TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Normalmente, una aplicación llama a **TrackPopupMenuEx** en un procedimiento de ventana en respuesta a un mensaje generado por el usuario, como [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) o [**WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)

Además del identificador del menú emergente, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requiere que especifique un identificador para la ventana del propietario, la posición del menú contextual (en coordenadas de pantalla) y el botón del mouse que el usuario puede usar para elegir un elemento.

Todavía se [**admite la función TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) anterior, pero las nuevas aplicaciones deben usar la [**función TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) La **función TrackPopupMenuEx** requiere los mismos parámetros que **TrackPopupMenu,** pero también permite especificar una parte de la pantalla que el menú no debe ocultar. Normalmente, una aplicación llama a estas funciones en un procedimiento de ventana al procesar el [**mensaje \_ CONTEXTMENU de WM.**](wm-contextmenu.md)

Puede especificar la posición de un menú contextual proporcionando coordenadas x e y junto con la marca **TPM \_ CENTERALIGN,** **TPM \_ LEFTALIGN** o **TPM \_ RIGHTALIGN.** La marca especifica la posición del menú contextual con respecto a las coordenadas x e y.

Debe permitir que el usuario elija un elemento de un menú contextual con el mismo botón del mouse que se usa para mostrar el menú. Para ello, especifique la **marca TPM \_ LEFTBUTTON** o **TPM \_ RIGHTBUTTON** para indicar qué botón del mouse puede usar el usuario para elegir un elemento de menú.

-   [Procesamiento del mensaje \_ CONTEXTMENU de WM](/windows)
-   [Crear un menú contextual Font-Attributes acceso directo](#creating-a-shortcut-font-attributes-menu)
-   [Mostrar un menú contextual](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Procesamiento del mensaje \_ CONTEXTMENU de WM

El [**mensaje \_ CONTEXTMENU de WM**](wm-contextmenu.md) se genera cuando el procedimiento de ventana de una aplicación pasa el mensaje WM [**\_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) La aplicación puede procesar este mensaje para mostrar un menú contextual adecuado para una parte específica de su pantalla. Si la aplicación no muestra un menú contextual, debe pasar el mensaje a **DefWindowProc para** el control predeterminado.

A continuación se muestra un ejemplo del procesamiento de mensajes [**\_ CONTEXTMENU**](wm-contextmenu.md) de WM tal como podría aparecer en el procedimiento de ventana de una aplicación. Las palabras de orden bajo y orden superior del parámetro *lParam* especifican las coordenadas de pantalla del mouse cuando se libera el botón derecho del mouse (tenga en cuenta que estas coordenadas pueden tomar valores negativos en sistemas con varios monitores). La función **OnContextMenu** definida por la aplicación devuelve **TRUE** si muestra un menú contextual, o **FALSE** si no lo hace.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



La siguiente función OnContextMenu definida por la aplicación muestra un menú contextual si la posición del mouse especificada está dentro del área cliente de la ventana. Una función más sofisticada podría mostrar uno de varios menús diferentes, dependiendo de la parte del área de cliente especificada. Para mostrar realmente el menú contextual, en este ejemplo se llama a una función definida por la aplicación denominada DisplayContextMenu. Para obtener una descripción de esta función, vea [Mostrar un menú contextual.](#displaying-a-shortcut-menu)


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a>Crear un menú contextual Font-Attributes acceso directo

El ejemplo de esta sección contiene partes de código de una aplicación que crea y muestra un menú contextual que permite al usuario establecer fuentes y atributos de fuente. La aplicación muestra el menú en el área cliente de su ventana principal cada vez que el usuario hace clic en el botón izquierdo del mouse.

Esta es la plantilla de menú del menú contextual que se proporciona en el archivo de definición de recursos de la aplicación.


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



En el ejemplo siguiente se proporciona el procedimiento de ventana y las funciones de soporte que se usan para crear y mostrar el menú contextual.


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a>Mostrar un menú contextual

La función que se muestra en el ejemplo siguiente muestra un menú contextual.

La aplicación incluye un recurso de menú identificado por la cadena "ShortcutExample". La barra de menús simplemente contiene un nombre de menú. La aplicación usa la [**función TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) para mostrar el menú asociado a este elemento de menú. (La propia barra de menús no se muestra porque **TrackPopupMenu** requiere un identificador para un menú, un submenú o un menú contextual).


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a>Uso de mapas Menu-Item mapa de bits

El sistema puede usar un mapa de bits en lugar de una cadena de texto para mostrar un elemento de menú. Para usar un mapa de bits, debe establecer la marca **MIIM \_ BITMAP** para el elemento de menú y especificar un identificador para el mapa de bits que el sistema debe mostrar para el elemento de menú en el **miembro hbmpItem** de la [**estructura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) En esta sección se describe cómo usar mapas de bits para los elementos de menú.

-   [Establecer la marca de tipo de mapa de bits](#setting-the-bitmap-type-flag)
-   [Crear el mapa de bits](#creating-the-bitmap)
-   [Agregar líneas y gráficos a un menú](#adding-lines-and-graphs-to-a-menu)
-   [Ejemplo de mapas Menu-Item mapa de bits](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Establecer la marca de tipo de mapa de bits

La **marca MIIM \_ BITMAP o** MF **\_ BITMAP** indica al sistema que use un mapa de bits en lugar de una cadena de texto para mostrar un elemento de menú. La marca **MIIM \_ BITMAP** o **MF \_ BITMAP** de un elemento de menú debe establecerse en tiempo de ejecución; no se puede establecer en el archivo de definición de recursos.

Para las nuevas aplicaciones, puede usar las funciones [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) o [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) para establecer la marca de tipo BITMAP de **MIIM. \_** Para cambiar un elemento de menú de un elemento de texto a un elemento de mapa de bits, use **SetMenuItemInfo**. Para agregar un nuevo elemento de mapa de bits a un menú, use la **función InsertMenuItem.**

Las aplicaciones escritas para versiones anteriores del sistema pueden seguir usando las funciones [**ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para establecer la marca **MF \_ BITMAP.** Para cambiar un elemento de menú de un elemento de cadena de texto a un elemento de mapa de bits, use **ModifyMenu**. Para agregar un nuevo elemento de mapa de bits a un menú, use la marca **MF \_ BITMAP** con la **función InsertMenu** **o AppendMenu.**

### <a name="creating-the-bitmap"></a>Crear el mapa de bits

Al establecer la marca de tipo **MIIM \_ BITMAP** o **MF \_ BITMAP** para un elemento de menú, también debe especificar un identificador para el mapa de bits que el sistema debe mostrar para el elemento de menú. Puede proporcionar el mapa de bits como un recurso de mapa de bits o crear el mapa de bits en tiempo de ejecución. Si usa un recurso de mapa de bits, puede usar la [**función LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) para cargar el mapa de bits y obtener su identificador.

Para crear el mapa de bits en tiempo de ejecución, use Windows Interfaz de dispositivo gráfico (GDI). GDI proporciona varias maneras de crear un mapa de bits en tiempo de ejecución, pero los desarrolladores suelen usar el método siguiente:

1.  Use la [**función CreateCompatibleDC para**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) crear un contexto de dispositivo compatible con el contexto de dispositivo que usa la ventana principal de la aplicación.
2.  Use la [**función CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) para crear un mapa de bits compatible con la ventana principal de la aplicación o use la [**función CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) para crear un mapa de bits monocroma.
3.  Use la [**función SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para seleccionar el mapa de bits en el contexto de dispositivo compatible.
4.  Use funciones de dibujo GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) y [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para dibujar una imagen en el mapa de bits.

Para obtener más información, vea [Mapas de bits.](/windows/desktop/gdi/bitmaps)

### <a name="adding-lines-and-graphs-to-a-menu"></a>Agregar líneas y gráficos a un menú

En el ejemplo de código siguiente se muestra cómo crear un menú que contiene mapas de bits de elementos de menú. Crea dos menús. El primero es un menú Gráfico que contiene tres mapas de bits de elementos de menú: un gráfico circular, un gráfico de líneas y un gráfico de barras. En el ejemplo se muestra cómo cargar estos mapas de bits desde el archivo de recursos de la aplicación y, a continuación, usar las funciones [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) y [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para crear los elementos de menú y menú.

El segundo menú es un menú Líneas. Contiene mapas de bits que muestran los estilos de línea proporcionados por el lápiz predefinido en el sistema. Los mapas de bits de estilo de línea se crean en tiempo de ejecución mediante funciones GDI.

Estas son las definiciones de los recursos de mapa de bits en el archivo de definición de recursos de la aplicación.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Estas son las partes pertinentes del archivo de encabezado de la aplicación.


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



En el ejemplo siguiente se muestra cómo se crean los menús y los mapas de bits de elementos de menú en una aplicación.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a>Ejemplo de mapas Menu-Item mapa de bits

En el ejemplo de este tema se crean dos menús, cada uno con varios elementos de menú de mapa de bits. Para cada menú, la aplicación agrega un nombre de menú correspondiente a la barra de menús de la ventana principal.

El primer menú contiene elementos de menú que muestran cada uno de los tres tipos de gráfico: circular, línea y barra. Los mapas de bits de estos elementos de menú se definen como recursos y se cargan mediante la [**función LoadBitmap.**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) Asociado a este menú es un nombre de menú "Gráfico" en la barra de menús.

El segundo menú contiene elementos de menú que muestran cada uno de los cinco estilos de línea usados con la función [**CreatePen:**](/windows/desktop/api/wingdi/nf-wingdi-createpen) **PS \_ SOLID,** **PS \_ DASH,** **PS \_ DOT,** **PS \_ DASHDOT** y **PS \_ DASHDOTDOT.** La aplicación crea los mapas de bits para estos elementos de menú en tiempo de ejecución mediante funciones de dibujo GDI. Asociado a este menú es un nombre **de menú Líneas** en la barra de menús.

Se definen en el procedimiento de ventana de la aplicación dos matrices estáticas de identificadores de mapa de bits. Una matriz contiene los identificadores de los tres mapas de bits usados para el **menú** Gráfico. El otro contiene los identificadores de los cinco mapas de bits usados para el **menú** Líneas. Al procesar el [**mensaje WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) el procedimiento de ventana carga los mapas de bits del gráfico, crea los mapas de bits de línea y, a continuación, agrega los elementos de menú correspondientes. Al procesar el [**mensaje WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) el procedimiento de ventana elimina todos los mapas de bits.

A continuación se encuentran las partes pertinentes del archivo de encabezado de la aplicación.


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



A continuación se encuentran las partes pertinentes del procedimiento de ventana. El procedimiento de ventana realiza la mayor parte de su inicialización mediante una llamada a las funciones LoadChartBitmaps, CreateLineBitmaps y AddBitmapMenu definidas por la aplicación, que se describen más adelante en este tema.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



La función LoadChartBitmaps definida por la aplicación carga los recursos de mapa de bits para el menú del gráfico mediante una llamada a la [**función LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) como se muestra a continuación.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



La función CreateLineBitmaps definida por la aplicación crea los mapas de bits para el menú Líneas mediante funciones de dibujo GDI. La función crea un contexto de dispositivo de memoria (DC) con las mismas propiedades que el controlador de dominio de la ventana de escritorio. Para cada estilo de línea, la función crea un mapa de bits, lo selecciona en el controlador de dominio de memoria y dibuja en él.


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



La función AddBitmapMenu definida por la aplicación crea un menú y le agrega el número especificado de elementos de menú de mapa de bits. A continuación, agrega un nombre de menú correspondiente a la barra de menús de la ventana especificada.


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a>Crear elementos Owner-Drawn menú

Si necesita un control completo sobre la apariencia de un elemento de menú, puede usar un elemento de menú dibujado por el propietario en la aplicación. En esta sección se describen los pasos necesarios para crear y usar un elemento de menú dibujado por el propietario.

-   [Establecimiento de la Owner-Drawn de datos](#setting-the-owner-drawn-flag)
-   [Menús dibujados por el propietario y el mensaje \_ MEASUREITEM de WM](/windows)
-   [Menús dibujados por el propietario y el mensaje \_ DRAWITEM de WM](/windows)
-   [Menús dibujados por el propietario y el mensaje \_ WM MENUCHAR](/windows)
-   [Establecimiento de fuentes para Menu-Item cadenas de texto](#setting-fonts-for-menu-item-text-strings)
-   [Ejemplo de elementos Owner-Drawn menú](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Establecimiento de la Owner-Drawn de datos

No se puede definir un elemento de menú dibujado por el propietario en el archivo de definición de recursos de la aplicación. En su lugar, debe crear un nuevo elemento de menú o modificar uno existente mediante la marca **de menú MFT \_ OWNERDRAW.**

Puede usar las [**funciones InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) o [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para especificar un elemento de menú dibujado por el propietario. Use **InsertMenuItem** para insertar un nuevo elemento de menú en la posición especificada en una barra de menús o un menú. Use **SetMenuItemInfo para** cambiar el contenido de un menú.

Al llamar a estas dos funciones, debe especificar un puntero a una estructura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) que especifica las propiedades del nuevo elemento de menú o las propiedades que desea cambiar para un elemento de menú existente. Para convertir un elemento en un elemento dibujado por el propietario, especifique el valor **\_ de MIIM FTYPE** para el miembro **fMask** y el valor **MFT \_ OWNERDRAW** para el **miembro fType.**

Al establecer los miembros adecuados de la estructura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) puede asociar un valor definido por la aplicación, denominado datos de elemento **,** a cada elemento de menú. Para ello, especifique el valor **DE MIIM \_ DATA** para el miembro **fMask** y el valor definido por la aplicación para el **miembro dwItemData.**

Puede usar datos de elementos con cualquier tipo de elemento de menú, pero es especialmente útil para los elementos dibujados por el propietario. Por ejemplo, suponga que una estructura contiene información utilizada para dibujar un elemento de menú. Una aplicación podría usar los datos de elemento de un elemento de menú para almacenar un puntero a la estructura . Los datos del elemento se envían a la ventana de propietario del menú con los [**mensajes \_ WM MEASUREITEM**](../controls/wm-measureitem.md) [**y WM \_ DRAWITEM.**](../controls/wm-drawitem.md) Para recuperar los datos de elementos de un menú en cualquier momento, use la [**función GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Las aplicaciones escritas para versiones anteriores del sistema pueden seguir llamadas [**a AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para asignar la marca **MF \_ OWNERDRAW** a un elemento de menú dibujado por el propietario.

Al llamar a cualquiera de estas tres funciones, puede pasar un valor como parámetro *lpNewItem.* Este valor puede representar cualquier información significativa para la aplicación y que estará disponible para la aplicación cuando se muestre el elemento. Por ejemplo, el valor podría contener un puntero a una estructura ; La estructura, a su vez, puede contener una cadena de texto y un identificador de la fuente lógica que la aplicación usará para dibujar la cadena.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn menús y el mensaje \_ MEASUREITEM de WM

Antes de que el sistema muestre un elemento de menú dibujado por el propietario por primera vez, envía el mensaje [**DE WM \_ MEASUREITEM**](../controls/wm-measureitem.md) al procedimiento de ventana de la ventana que posee el menú del elemento. Este mensaje contiene un puntero a una [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que identifica el elemento y contiene los datos de elemento que una aplicación puede haber asignado a él. El procedimiento de ventana debe rellenar los **miembros itemWidth** y **itemHeight** de la estructura antes de volver del procesamiento del mensaje. El sistema usa la información de estos miembros al crear el rectángulo delimitador en el que una aplicación dibuja el elemento de menú. También usa la información para detectar cuándo el usuario elige el elemento.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn menús y el mensaje \_ DRAWITEM de WM

Siempre que se deba dibujar el elemento (por ejemplo, cuando se muestra por primera vez o cuando el usuario lo selecciona), el sistema envía el mensaje [**\_ DRAWITEM**](../controls/wm-drawitem.md) de WM al procedimiento de ventana de la ventana de propietario del menú. Este mensaje contiene un puntero a una [**estructura DRAWITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento, incluidos los datos de elemento que una aplicación puede haber asignado a él. Además, **DRAWITEMSTRUCT** contiene marcas que indican el estado del elemento (por ejemplo, si está atenuado o seleccionado), así como un rectángulo delimitador y un contexto de dispositivo que la aplicación usa para dibujar el elemento.

Una aplicación debe hacer lo siguiente al procesar el [**mensaje \_ DRAWITEM de WM:**](../controls/wm-drawitem.md)

-   Determine el tipo de dibujo necesario. Para ello, compruebe el miembro **itemAction** de la [**estructura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
-   Dibuje el elemento de menú correctamente, usando el rectángulo delimitador y el contexto del dispositivo obtenidos de la [**estructura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) La aplicación solo debe dibujar dentro del rectángulo delimitador. Por motivos de rendimiento, el sistema no recorta partes de la imagen dibujadas fuera del rectángulo.
-   Restaure todos los objetos GDI seleccionados para el contexto del dispositivo del elemento de menú.

Si el usuario selecciona el elemento de menú, el sistema establece el miembro **itemAction** de la estructura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) en el valor **ODA \_ SELECT** y establece el valor SELECCIONADO **de ODS \_** en el **miembro itemState.** Esta es la indicación de una aplicación para volver a dibujar el elemento de menú para indicar que está seleccionado.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn menús y el mensaje \_ MENUCHAR de WM

Los menús que no son menús dibujados por el propietario pueden especificar un menú mnemotécnico insertando un carácter de subrayado junto a un carácter en la cadena de menú. Esto permite al usuario seleccionar el menú presionando ALT y presionando el carácter mnemotécnico del menú. Sin embargo, en los menús dibujados por el propietario no se puede especificar un menú mnemotécnico de esta manera. En su lugar, la aplicación debe procesar el [**mensaje \_ MENUCHAR de WM**](wm-menuchar.md) para proporcionar menús dibujados por el propietario con menús mnemotécnicos.

El [**mensaje \_ MENUCHAR**](wm-menuchar.md) de WM se envía cuando el usuario tipos un menú mnemotécnico que no coincide con ninguno de los elementos mnemotécnicos predefinidos del menú actual. El valor contenido en *wParam* especifica el carácter ASCII que corresponde a la tecla que el usuario presionó con la tecla ALT. La palabra de orden bajo *de wParam* especifica el tipo del menú seleccionado y puede ser uno de los valores siguientes:

-   **MF \_ POPUP** si el menú actual es un submenú.
-   **MF \_ SYSMENU** si el menú es el menú del sistema.

La palabra de orden superior *de wParam* contiene el identificador de menú del menú actual. La ventana con los menús dibujados por el propietario puede procesar [**WM \_ MENUCHAR**](wm-menuchar.md) de la siguiente manera:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



Los dos de la palabra de orden superior del valor devuelto informan al sistema de que la palabra de orden bajo del valor devuelto contiene el índice de base cero del elemento de menú que se va a seleccionar.

Las siguientes constantes corresponden a los posibles valores devueltos del [**mensaje \_ MENUCHAR de WM.**](wm-menuchar.md)



| Constante         | Value | Significado                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MNC \_ IGNORE**  | 0     | El sistema debe descartar el carácter que el usuario presionó y crear un pitido corto en el altavoz del sistema.                                                       |
| **MNC \_ CLOSE**   | 1     | El sistema debe cerrar el menú activo.                                                                                                                      |
| **MNC \_ EXECUTE** | 2     | El sistema debe elegir el elemento especificado en la palabra de orden bajo del valor devuelto. La ventana de propietario recibe un [**mensaje \_ WM COMMAND.**](wm-command.md) |
| **MNC \_ SELECT**  | 3     | El sistema debe seleccionar el elemento especificado en la palabra de orden bajo del valor devuelto.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Establecimiento de fuentes para Menu-Item cadenas de texto

Este tema contiene un ejemplo de una aplicación que usa elementos de menú dibujados por el propietario en un menú. El menú contiene elementos que establecen los atributos de la fuente actual y los elementos se muestran con el atributo de fuente adecuado.

Aquí se muestra cómo se define el menú en el archivo de definición de recursos. Tenga en cuenta que las cadenas de los elementos de menú Normal, Negrita, Cursiva y Subrayado se asignan en tiempo de ejecución, por lo que sus cadenas están vacías en el archivo de definición de recursos.


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



El procedimiento de ventana de la aplicación procesa los mensajes implicados en el uso de elementos de menú dibujados por el propietario. La aplicación usa el [**mensaje \_ WM CREATE**](/windows/desktop/winmsg/wm-create) para hacer lo siguiente:

-   Establezca la **marca MF \_ OWNERDRAW** para los elementos de menú.
-   Establezca las cadenas de texto de los elementos de menú.
-   Obtenga identificadores de las fuentes utilizadas para dibujar los elementos.
-   Obtenga los valores de color de fondo y texto para los elementos de menú seleccionados.

Las cadenas de texto y los identificadores de fuente se almacenan en una matriz de estructuras MYITEM definidas por la aplicación. La función GetAFont definida por la aplicación crea una fuente que corresponde al atributo de fuente especificado y devuelve un identificador a la fuente. Los identificadores se destruyen durante el procesamiento del [**mensaje WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy)

Durante el procesamiento del mensaje [**\_ MEASUREITEM**](../controls/wm-measureitem.md) de WM, el ejemplo obtiene el ancho y alto de una cadena de elemento de menú y copia estos valores en la [**estructura MEASUREITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) El sistema usa los valores de ancho y alto para calcular el tamaño del menú.

Durante el procesamiento del mensaje [**\_ DRAWITEM de WM,**](../controls/wm-drawitem.md) la cadena del elemento de menú se dibuja con espacio a la izquierda junto a la cadena del mapa de bits de marca de verificación. Si el usuario selecciona el elemento, se usan el texto y los colores de fondo seleccionados para dibujar el elemento.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a>Ejemplo de elementos Owner-Drawn menú

En el ejemplo de este tema se usan elementos de menú dibujados por el propietario en un menú. Los elementos de menú seleccionan atributos de fuente específicos y la aplicación muestra cada elemento de menú mediante una fuente que tiene el atributo correspondiente. Por ejemplo, el elemento de menú **Cursiva** se muestra en una fuente cursiva. El **nombre del** menú Carácter de la barra de menús abre el menú.

La barra de menús y el menú desplegable se definen inicialmente mediante un recurso de plantilla de menú extendido. Dado que una plantilla de menú no puede especificar elementos dibujados por el propietario, el menú contiene inicialmente cuatro elementos de menú de texto con las siguientes cadenas: "Regular", "Negrita", "Cursiva" y "Subrayado". El procedimiento de ventana de la aplicación los cambia a elementos dibujados por el propietario cuando procesa el [**mensaje \_ WM CREATE.**](/windows/desktop/winmsg/wm-create) Cuando recibe el mensaje **WM \_ CREATE,** el procedimiento de ventana llama a la función OnCreate definida por la aplicación, que realiza los pasos siguientes para cada elemento de menú:

-   Asigna una estructura MYITEM definida por la aplicación.
-   Obtiene el texto del elemento de menú y lo guarda en la estructura MYITEM definida por la aplicación.
-   Crea la fuente utilizada para mostrar el elemento de menú y guarda su identificador en la estructura MYITEM definida por la aplicación.
-   Cambia el tipo de elemento de menú a **MFT \_ OWNERDRAW** y guarda un puntero a la estructura MYITEM definida por la aplicación como datos de elemento.

Dado que un puntero a cada estructura MYITEM definida por la aplicación se guarda como datos de elemento, se pasa al procedimiento de ventana junto con los mensajes [**\_ WM MEASUREITEM**](../controls/wm-measureitem.md) y [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) para el elemento de menú correspondiente. El puntero se encuentra en el miembro **itemData** de las estructuras [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) [**y DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)

Se [**envía un mensaje \_ MEASUREITEM**](../controls/wm-measureitem.md) de WM para cada elemento de menú dibujado por el propietario la primera vez que se muestra. La aplicación procesa este mensaje seleccionando la fuente del elemento de menú en un contexto de dispositivo y, a continuación, determinando el espacio necesario para mostrar el texto del elemento de menú en esa fuente. Tanto la estructura del elemento de menú como la fuente especifican el texto del elemento de `MYITEM` menú (la estructura definida por la aplicación). La aplicación determina el tamaño del texto mediante la [**función GetTextExtentPoint32.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a)

El procedimiento de ventana procesa el [**mensaje \_ DRAWITEM de WM**](../controls/wm-drawitem.md) mostrando el texto del elemento de menú en la fuente adecuada. La estructura del elemento de menú especifica tanto la fuente como el texto del elemento de `MYITEM` menú. La aplicación selecciona el texto y los colores de fondo adecuados para el estado del elemento de menú.

El procedimiento de ventana procesa el [**mensaje \_ WM DESTROY**](/windows/desktop/winmsg/wm-destroy) para destruir fuentes y liberar memoria. La aplicación elimina la fuente y libera la estructura MYITEM definida por la aplicación para cada elemento de menú.

Las siguientes son las partes pertinentes del archivo de encabezado de la aplicación.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



Las siguientes son las partes pertinentes del procedimiento de ventana de la aplicación y sus funciones asociadas.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a>Uso de mapas de bits de marca de verificación personalizados

El sistema proporciona un mapa de bits de marca de verificación predeterminado para mostrar junto a un elemento de menú seleccionado. Puede personalizar un elemento de menú individual proporcionando un par de mapas de bits para reemplazar el mapa de bits de marca de verificación predeterminado. El sistema muestra un mapa de bits cuando se selecciona el elemento y el otro cuando está claro. En esta sección se describen los pasos necesarios para crear y usar mapas de bits de marca de verificación personalizados.

-   [Crear mapas de bits de marca de verificación personalizados](#creating-custom-check-mark-bitmaps)
-   [Asociación de mapas de bits a un elemento de menú](#associating-bitmaps-with-a-menu-item)
-   [Establecimiento del atributo check-mark](#setting-the-check-mark-attribute)
-   [Simulación de casillas en un menú](#simulating-check-boxes-in-a-menu)
-   [Ejemplo de uso de mapas de bits de marca de verificación personalizados](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Crear mapas de bits de marca de verificación personalizados

Un mapa de bits de marca de verificación personalizado debe tener el mismo tamaño que el mapa de bits de marca de verificación predeterminado. Puede recuperar el tamaño de marca de verificación predeterminado del mapa de bits llamando a la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) La palabra de orden bajo del valor devuelto de esta función especifica el ancho; la palabra de orden superior especifica el alto.

Puede usar recursos de mapa de bits para proporcionar mapas de bits de marca de verificación. Sin embargo, dado que el tamaño de mapa de bits necesario varía en función del tipo de pantalla, es posible que tenga que cambiar el tamaño del mapa de bits en tiempo de ejecución mediante la [**función StretchBlt.**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) En función del mapa de bits, la distorsión causada por el tamaño podría producir resultados inaceptables.

En lugar de usar un recurso de mapa de bits, puede crear un mapa de bits en tiempo de ejecución mediante funciones GDI.

**Para crear un mapa de bits en tiempo de ejecución**

1.  Use la [**función CreateCompatibleDC para**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) crear un contexto de dispositivo compatible con el que usa la ventana principal de la aplicación.

    El parámetro *hdc* de la función puede especificar **NULL** o el valor devuelto de la función. [**CreateCompatibleDC devuelve**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) un identificador al contexto de dispositivo compatible.

2.  Use la [**función CreateCompatibleBitmap para**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) crear un mapa de bits compatible con la ventana principal de la aplicación.

    Los parámetros *nWidth* y *nHeight* de esta función establecen el tamaño del mapa de bits; deben especificar la información de ancho y alto devuelta por la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

    > [!Note]  
    > También puede usar la función [**CreateBitmap para**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) crear un mapa de bits monocroma.

     

3.  Use la [**función SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) para seleccionar el mapa de bits en el contexto de dispositivo compatible.
4.  Use funciones de dibujo GDI, como [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) y [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), para dibujar una imagen en el mapa de bits, o use funciones como [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) y [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) para copiar una imagen en el mapa de bits.

Para obtener más información, vea [Mapas de bits.](/windows/desktop/gdi/bitmaps)

### <a name="associating-bitmaps-with-a-menu-item"></a>Asociación de mapas de bits a un elemento de menú

Para asociar un par de mapas de bits de marca de verificación a un elemento de menú, pase los identificadores de los mapas de bits a la [**función SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) El *parámetro hBitmapUnchecked* identifica el mapa de bits sin borrar y el *parámetro hBitmapChecked* identifica el mapa de bits seleccionado. Si desea quitar una o ambas marcas de verificación de un elemento de menú, puede establecer el parámetro *hBitmapUnchecked* o *hBitmapChecked,* o ambos, en **NULL.**

### <a name="setting-the-check-mark-attribute"></a>Establecimiento del atributo check-mark

La [**función CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) establece el atributo de marca de verificación de un elemento de menú en seleccionado o desactivado. Puede especificar el valor **MF \_ CHECKED para** establecer el atributo de marca de verificación en seleccionado y el valor MF **\_ UNCHECKED** para establecerlo en clear.

También puede establecer el estado de comprobación de un elemento de menú mediante la [**función SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

A veces, un grupo de elementos de menú representa un conjunto de opciones mutuamente excluyentes. Mediante la función [**CheckMenuRadioItem,**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) puede comprobar un elemento de menú al mismo tiempo que quita la marca de verificación de todos los demás elementos de menú del grupo.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulación de casillas en un menú

Este tema contiene un ejemplo que muestra cómo simular casillas en un menú. El ejemplo contiene un menú Carácter cuyos elementos permiten al usuario establecer los atributos negrita, cursiva y subrayado de la fuente actual. Cuando un atributo de fuente está en vigor, se muestra una marca de verificación en la casilla situada junto al elemento de menú correspondiente; De lo contrario, se muestra una casilla vacía junto al elemento.

En el ejemplo se reemplaza el mapa de bits de marca de verificación predeterminado por dos mapas de bits: un mapa de bits con una casilla seleccionada y el mapa de bits con una casilla vacía. El mapa de bits de casilla seleccionado se muestra junto al elemento de menú Negrita, Cursiva o Subrayado cuando el atributo de marca de verificación del elemento está establecido en **MF \_ CHECKED.** El mapa de bits de casilla desactivada o vacía se muestra cuando el atributo de marca de verificación se establece en **MF \_ UNCHECKED.**

El sistema proporciona un mapa de bits predefinido que contiene las imágenes usadas para las casillas y los botones de radio. En el ejemplo se aíslan las casillas seleccionadas y vacías, se copian en dos mapas de bits independientes y, a continuación, se usan como mapas de bits seleccionados y borrados para los elementos del **menú** Carácter.

Para recuperar un identificador en el mapa de bits de casilla definido por el sistema, en el ejemplo se llama a la función [**LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) especificando **NULL** como parámetro *hInstance* y **OBM \_ CHECKBOXES** como parámetro *lpBitmapName.* Dado que las imágenes del mapa de bits tienen el mismo tamaño, el ejemplo puede aislarlas dividiendo el ancho y el alto del mapa de bits por el número de imágenes de sus filas y columnas.

La siguiente parte de un archivo de definición de recursos muestra cómo se definen los elementos de menú **del** menú Carácter. Tenga en cuenta que no hay atributos de fuente en vigor inicialmente, por lo que el atributo de marca de verificación del elemento **Regular** se establece en seleccionado y, de forma predeterminada, el atributo de marca de verificación de los elementos restantes se establece en borrar.


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



Este es el contenido pertinente del archivo de encabezado de la aplicación.


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



En el ejemplo siguiente se muestran las partes del procedimiento de ventana que crean los mapas de bits de marca de verificación; establezca el atributo de marca de verificación de los elementos de menú **Negrita,** **Cursiva** **y** Subrayado; y destruyen mapas de bits de marca de verificación.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Ejemplo de uso de mapas de bits de marca de verificación personalizados

En el ejemplo de este tema se asignan mapas de bits de marca de verificación personalizados a los elementos de menú de dos menús. Los elementos de menú del primer menú especifican atributos de carácter: negrita, cursiva y subrayado. Cada elemento de menú se puede seleccionar o borrar. Para estos elementos de menú, en el ejemplo se usan mapas de bits de marca de verificación que se parecen a los estados seleccionados y borrados de un control de casilla.

Los elementos de menú del segundo menú especifican la configuración de alineación del párrafo: izquierda, centrada y derecha. Solo se selecciona uno de estos elementos de menú en cualquier momento. Para estos elementos de menú, en el ejemplo se usan mapas de bits de marca de verificación que se parecen a los estados seleccionados y claros de un control de botón de radio.

El procedimiento de ventana procesa el [**mensaje \_ CREATE de WM**](/windows/desktop/winmsg/wm-create) llamando a la función OnCreate definida por la aplicación. `OnCreate`crea los cuatro mapas de bits de marca de verificación y, a continuación, los asigna a sus elementos de menú adecuados mediante la [**función SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)

Para crear cada mapa de bits, OnCreate llama a la función CreateMenuBitmaps definida por la aplicación y especifica un puntero a una función de dibujo específica del mapa de bits. CreateMenuBitmaps crea un mapa de bits monocromático del tamaño necesario, lo selecciona en un contexto de dispositivo de memoria y borra el fondo. A continuación, llama a la función de dibujo especificada para rellenar el primer plano.

Las cuatro funciones de dibujo definidas por la aplicación son DrawCheck, DrawUncheck, **DrawRadioCheck** y DrawRadioUncheck. Dibujan un rectángulo con una X, un rectángulo vacío, una elipse que contiene una elipse rellena más pequeña y una elipse vacía, respectivamente.

El procedimiento de ventana procesa el [**mensaje \_ WM DESTROY**](/windows/desktop/winmsg/wm-destroy) eliminando los mapas de bits de marca de verificación. Recupera cada identificador de mapa de bits mediante la [**función GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) y, a continuación, pasa un identificador a la función.

Cuando el usuario elige un elemento de menú, se envía un [**mensaje \_ WM COMMAND**](wm-command.md) a la ventana del propietario. Para los elementos de menú del **menú Carácter,** el procedimiento de ventana llama a la función CheckCharacterItem definida por la aplicación. Para los elementos del **menú Párrafo,** el procedimiento de ventana llama a la función CheckParagraphItem definida por la aplicación.

Cada elemento del **menú Carácter** se puede seleccionar y borrar de forma independiente. Por lo tanto, CheckCharacterItem simplemente cambia el estado de comprobación del elemento de menú especificado. En primer lugar, la función llama [**a la función GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) para obtener el estado actual del elemento de menú. A continuación, cambia la **marca de estado \_ MFS CHECKED** y establece el nuevo estado mediante una llamada a la función [**SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

A diferencia de los atributos de caracteres, solo se puede seleccionar una alineación de párrafo a la vez. Por lo tanto, CheckParagraphItem comprueba el elemento de menú especificado y quita la marca de verificación de todos los demás elementos del menú. Para ello, llama a la [**función CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

A continuación se encuentran las partes pertinentes del archivo de encabezado de la aplicación.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



Las siguientes son las partes pertinentes del procedimiento de ventana de la aplicación y las funciones relacionadas.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 