---
description: En los ejemplos de esta sección se describe cómo realizar tareas asociadas con el uso de ventanas.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Uso de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75681987a4bc012618135f666b3ff973880b8129d2ad1ee896bcdbed266d179d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436971"
---
# <a name="using-windows"></a>Uso de Windows

En los ejemplos de esta sección se describe cómo realizar las siguientes tareas:

-   [Crear una ventana principal](#creating-a-main-window)
-   [Crear, enumerar y dimensionar elementos secundarios Windows](#creating-enumerating-and-sizing-child-windows)
-   [Destruir una ventana](#destroying-a-window)
-   [Uso de capas Windows](#using-layered-windows)

## <a name="creating-a-main-window"></a>Crear una ventana principal

La primera ventana que crea una aplicación suele ser la ventana principal. La ventana principal se crea mediante la función [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) que especifica la clase de ventana, el nombre de la ventana, los estilos de ventana, el tamaño, la posición, el identificador de menú, el identificador de instancia y los datos de creación. Una ventana principal pertenece a una clase de ventana definida por la aplicación, por lo que debe registrar la clase de ventana y proporcionar un procedimiento de ventana para la clase antes de crear la ventana principal.

La mayoría de las aplicaciones suelen usar [**el estilo \_ OVERLAPPEDWINDOW**](window-styles.md) de WS para crear la ventana principal. Este estilo proporciona a la ventana una barra de título, un menú de ventana, un borde de tamaño y minimiza y maximiza los botones. La [**función CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) devuelve un identificador que identifica de forma única la ventana.

En el ejemplo siguiente se crea una ventana principal que pertenece a una clase de ventana definida por la aplicación. El nombre de la **ventana, Ventana** principal , aparecerá en la barra de título de la ventana. Al combinar los estilos [**WS \_ VSCROLL**](window-styles.md) y **WS \_ HSCROLL** con el estilo **WS \_ OVERLAPPEDWINDOW,** la aplicación crea una ventana principal con barras de desplazamiento horizontal y vertical, además de los componentes proporcionados por el estilo **\_ OVERLAPPEDWINDOW de WS.** Las cuatro repeticiones de la **constante \_ CW USEDEFAULT** establecen el tamaño inicial y la posición de la ventana en los valores predeterminados definidos por el sistema. Al especificar **NULL en** lugar de un identificador de menú, la ventana tendrá el menú definido para la clase de ventana.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



Observe que en el ejemplo anterior se llama a [**la función ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) después de crear la ventana principal. Esto se hace porque el sistema no muestra automáticamente la ventana principal después de crearla. Al pasar la **marca \_ SW SHOWDEFAULT** a **ShowWindow,** la aplicación permite al programa que inició la aplicación establecer el estado de presentación inicial de la ventana principal. La [**función UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envía a la ventana su primer [**mensaje WM \_ PAINT.**](../gdi/wm-paint.md)

## <a name="creating-enumerating-and-sizing-child-windows"></a>Crear, enumerar y dimensionar elementos secundarios Windows

Puede dividir el área de cliente de una ventana en distintas áreas funcionales mediante ventanas secundarias. La creación de una ventana secundaria es como crear una ventana principal: se usa [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Para crear una ventana de una clase de ventana definida por la aplicación, debe registrar la clase de ventana y proporcionar un procedimiento de ventana antes de crear la ventana secundaria. Debe proporcionar a la ventana secundaria el estilo [**WS \_ CHILD**](window-styles.md) y especificar una ventana primaria para la ventana secundaria al crearla.

En el ejemplo siguiente se divide el área cliente de la ventana principal de una aplicación en tres áreas funcionales mediante la creación de tres ventanas secundarias del mismo tamaño. Cada ventana secundaria tiene el mismo alto que el área cliente de la ventana principal, pero cada una tiene un tercio de su ancho. La ventana principal crea las ventanas secundarias en respuesta al mensaje [**\_ WM CREATE,**](wm-create.md) que la ventana principal recibe durante su propio proceso de creación de ventanas. Dado que cada ventana secundaria tiene el estilo BORDER de [**WS, \_**](window-styles.md) cada una tiene un borde de línea fina. Además, dado que no se especifica el estilo VISIBLE de **WS, \_** cada ventana secundaria se oculta inicialmente. Observe también que a cada ventana secundaria se le asigna un identificador de ventana secundaria.

La ventana principal cambia de tamaño y coloca las ventanas secundarias en respuesta al mensaje [**WM \_ SIZE,**](wm-size.md) que la ventana principal recibe cuando cambia su tamaño. En respuesta a **WM \_ SIZE**, la ventana principal recupera las dimensiones de su área cliente mediante la función [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) y, a continuación, pasa las dimensiones a la función [**EnumChildWindows.**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) **EnumChildWindows** pasa el identificador a cada ventana secundaria, a su vez, a la función de devolución de llamada [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definida por la aplicación. Esta función tamaños y posiciones de cada ventana secundaria mediante una llamada a la [**función MoveWindow;**](/windows/win32/api/winuser/nf-winuser-movewindow) el tamaño y la posición se basan en las dimensiones del área de cliente de la ventana principal y el identificador de la ventana secundaria. Después, **EnumChildProc llama** a [**la función ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) para que la ventana sea visible.


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a>Destruir una ventana

Puede usar la [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir una ventana. Normalmente, una aplicación envía el [**mensaje WM \_ CLOSE**](wm-close.md) antes de destruir una ventana, lo que ofrece a la ventana la oportunidad de pedir confirmación al usuario antes de que se destruya la ventana. Una ventana que incluye un menú de ventana recibe automáticamente el mensaje **WM \_ CLOSE** cuando el usuario hace clic **en Cerrar en** el menú de la ventana. Si el usuario confirma que se debe destruir la ventana, la aplicación llama a **DestroyWindow**. El sistema envía el [**mensaje WM \_ DESTROY**](wm-destroy.md) a la ventana después de quitarlo de la pantalla. En respuesta a **WM \_ DESTROY,** la ventana guarda sus datos y libera los recursos que asignó. Una ventana principal concluye su procesamiento de **WM \_ DESTROY** llamando a la [**función PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para salir de la aplicación.

En el ejemplo siguiente se muestra cómo solicitar confirmación del usuario antes de destruir una ventana. En respuesta a [**WM \_ CLOSE**](wm-close.md), en el ejemplo se muestra un cuadro de diálogo que contiene los botones **Sí,** **No** **y Cancelar.** Si el usuario hace clic **en Sí,** [**se llama a DestroyWindow;**](/windows/win32/api/winuser/nf-winuser-destroywindow) De lo contrario, la ventana no se destruye. Dado que la ventana que se está destruyendo es una ventana principal, en el ejemplo se llama a [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) en respuesta a [**WM \_ DESTROY**](wm-destroy.md).


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a>Uso de capas Windows

Para que un cuadro de diálogo se cree como una ventana translúcida, cree primero el diálogo como de costumbre. A continuación, en [**WM \_ INITDIALOG,**](../dlgbox/wm-initdialog.md)establezca el bit en capas del estilo extendido de la ventana y llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) con el valor alfa deseado. El código podría tener este aspecto:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Tenga en cuenta que el tercer parámetro de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) es un valor que oscila entre 0 y 255, con 0, lo que hace que la ventana sea completamente transparente y 255 lo haga completamente opaca. Este parámetro imita la [**BLENDFUNCTION más versátil**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) de la función [**AlphaBlend.**](/windows/win32/api/wingdi/nf-wingdi-alphablend)

Para volver a hacer que esta ventana sea completamente opaca, quite el bit **WS \_ EX \_ LAYERED** llamando a [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) y, a continuación, pida a la ventana que vuelva a dibujar. Se desea quitar el bit para que el sistema sepa que puede liberar algo de memoria asociada con la capa y el redireccionamiento. El código podría tener este aspecto:


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



Para usar ventanas secundarias en capas, la aplicación tiene que declararse Windows 8 en el manifiesto.

 

 
