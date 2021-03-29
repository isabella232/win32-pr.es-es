---
description: En los ejemplos de esta sección se describe cómo realizar tareas asociadas al uso de Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Uso de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912606"
---
# <a name="using-windows"></a>Uso de Windows

En los ejemplos de esta sección se describe cómo realizar las tareas siguientes:

-   [Crear una ventana principal](#creating-a-main-window)
-   [Crear, enumerar y ajustar el tamaño de las ventanas secundarias](#creating-enumerating-and-sizing-child-windows)
-   [Destruir una ventana](#destroying-a-window)
-   [Usar ventanas superpuestas](#using-layered-windows)

## <a name="creating-a-main-window"></a>Crear una ventana principal

La primera ventana que crea una aplicación es normalmente la ventana principal. La ventana principal se crea mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana, el nombre de la ventana, los estilos de ventana, el tamaño, la posición, el identificador de menú, el identificador de instancia y los datos de creación. Una ventana principal pertenece a una clase de ventana definida por la aplicación, por lo que debe registrar la clase de ventana y proporcionar un procedimiento de ventana para la clase antes de crear la ventana principal.

Normalmente, la mayoría de las aplicaciones usan el estilo [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) para crear la ventana principal. Este estilo proporciona a la ventana una barra de título, un menú ventana, un borde de ajuste de tamaño y botones minimizar y maximizar. La función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) devuelve un identificador que identifica de forma única la ventana.

En el ejemplo siguiente se crea una ventana principal que pertenece a una clase de ventana definida por la aplicación. El nombre de la ventana, la **ventana principal**, aparecerá en la barra de título de la ventana. Mediante la combinación de los estilos [**WS \_ VSCROLL**](window-styles.md) y **WS \_ HSCROLL** con el estilo **WS \_ OVERLAPPEDWINDOW** , la aplicación crea una ventana principal con barras de desplazamiento horizontal y vertical además de los componentes proporcionados por el estilo **WS \_ OVERLAPPEDWINDOW** . Las cuatro apariciones de la constante **\_ USEDEFAULT de CW** establecen el tamaño inicial y la posición de la ventana en los valores predeterminados definidos por el sistema. Al especificar **null** en lugar de un identificador de menú, la ventana tendrá el menú definido para la clase de ventana.


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



Observe que en el ejemplo anterior se llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) después de crear la ventana principal. Esto se hace porque el sistema no muestra automáticamente la ventana principal después de crearla. Al pasar la marca **SW \_ SHOWDEFAULT** a **ShowWindow**, la aplicación permite que el programa que inició la aplicación establezca el estado de presentación inicial de la ventana principal. La función [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envía la ventana su primer mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) .

## <a name="creating-enumerating-and-sizing-child-windows"></a>Crear, enumerar y ajustar el tamaño de las ventanas secundarias

Puede dividir el área de cliente de una ventana en distintas áreas funcionales mediante el uso de ventanas secundarias. La creación de una ventana secundaria es como la creación de una ventana principal: se usa la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Para crear una ventana de una clase de ventana definida por la aplicación, debe registrar la clase de ventana y proporcionar un procedimiento de ventana antes de crear la ventana secundaria. Debe asignar a la ventana secundaria el [**estilo \_ secundario WS**](window-styles.md) y especificar una ventana primaria para la ventana secundaria al crearla.

En el ejemplo siguiente se divide el área cliente de la ventana principal de una aplicación en tres áreas funcionales mediante la creación de tres ventanas secundarias de igual tamaño. Cada ventana secundaria tiene el mismo alto que el área cliente de la ventana principal, pero cada una de ellas tiene un ancho de un tercio. La ventana principal crea las ventanas secundarias en respuesta al mensaje de [**\_ creación de WM**](wm-create.md) , que la ventana principal recibe durante su propio proceso de creación de ventanas. Dado que cada ventana secundaria tiene el estilo de [**\_ borde de WS**](window-styles.md) , cada una tiene un borde de línea fino. Además, dado que no se especifica el estilo **\_ visible de WS** , cada ventana secundaria está oculta inicialmente. Observe también que a cada ventana secundaria se le asigna un identificador de ventana secundaria.

La ventana principal cambia el tamaño de las ventanas secundarias en respuesta al mensaje de [**\_ tamaño de WM**](wm-size.md) , que recibe la ventana principal cuando cambia el tamaño. En respuesta al **\_ tamaño de WM**, la ventana principal recupera las dimensiones de su área de cliente mediante la función [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) y, a continuación, pasa las dimensiones a la función [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) . **EnumChildWindows** pasa el identificador a cada ventana secundaria, a su vez, a la función de devolución de llamada [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definida por la aplicación. Esta función dimensiona y coloca cada ventana secundaria mediante una llamada a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) . el tamaño y la posición se basan en las dimensiones del área cliente de la ventana principal y el identificador de la ventana secundaria. Después, **EnumChildProc** llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) para que la ventana sea visible.


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

Puede usar la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir una ventana. Normalmente, una aplicación envía el mensaje de [**\_ cierre de WM**](wm-close.md) antes de destruir una ventana, con lo que la ventana tiene la oportunidad de solicitar confirmación al usuario antes de que se destruya la ventana. Una ventana que incluye un menú ventana recibe automáticamente el mensaje de **\_ cierre de WM** cuando el usuario hace clic en **cerrar** en el menú ventana. Si el usuario confirma que se debe destruir la ventana, la aplicación llama a **DestroyWindow**. El sistema envía el mensaje de [**\_ destrucción de WM**](wm-destroy.md) a la ventana después de quitarlo de la pantalla. En respuesta a **la \_ destrucción de WM**, la ventana guarda sus datos y libera todos los recursos que ha asignado. Una ventana principal finaliza su procesamiento de **WM \_ Destroy** mediante una llamada a la función [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para salir de la aplicación.

En el ejemplo siguiente se muestra cómo solicitar confirmación del usuario antes de destruir una ventana. En respuesta a [**la \_ cierre de WM**](wm-close.md), en el ejemplo se muestra un cuadro de diálogo que contiene los botones **sí**, **no** y **Cancelar** . Si el usuario hace clic en **sí**, se llama a [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ; de lo contrario, no se destruye la ventana. Dado que la ventana que se va a destruir es una ventana principal, el ejemplo llama a [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) en respuesta a [**WM \_ Destroy**](wm-destroy.md).


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



## <a name="using-layered-windows"></a>Usar ventanas superpuestas

Para que aparezca un cuadro de diálogo como ventana translúcida, primero debe crear el cuadro de diálogo como de costumbre. Después, en [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), establezca el bit en capas del estilo extendido de la ventana y llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) con el valor alfa deseado. El código podría tener este aspecto:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Tenga en cuenta que el tercer parámetro de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) es un valor comprendido entre 0 y 255, con 0 para que la ventana sea completamente transparente y 255 lo que lo convierte en totalmente opaca. Este parámetro imita el [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) más versátil de la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .

Para que esta ventana vuelva a ser totalmente opaca, quite el bit por **\_ \_ capas de WS ex** llamando a [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) y, a continuación, pida a la ventana que vuelva a dibujarse. Se desea quitar el bit para que el sistema sepa que puede liberar alguna memoria asociada a la disposición en capas y el redireccionamiento. El código podría tener este aspecto:


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



Para usar las ventanas secundarias superpuestas, la aplicación tiene que declararse como compatible con Windows 8 en el manifiesto.

 

 
