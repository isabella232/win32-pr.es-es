---
description: En esta sección se explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Usar procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267204"
---
# <a name="using-window-procedures"></a>Usar procedimientos de ventana

En esta sección se explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana.

-   [Diseñar un procedimiento de ventana](#designing-a-window-procedure)
-   [Asociar un procedimiento de ventana a una clase window](#associating-a-window-procedure-with-a-window-class)
-   [Subclases de una ventana](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Diseñar un procedimiento de ventana

En el ejemplo siguiente se muestra la estructura de un procedimiento de ventana típico. El procedimiento de ventana usa el argumento de mensaje en una **instrucción switch** con mensajes individuales que se controlan mediante instrucciones **case** independientes. Observe que cada caso devuelve un valor específico para cada mensaje. Para los mensajes que no procesa, el procedimiento de ventana llama a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



El [**mensaje \_ WM NCCREATE**](wm-nccreate.md) se envía justo después de crear la ventana, pero si una aplicación responde a este mensaje devolviendo **FALSE,** se produce un error en la función [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) El [**mensaje \_ WM CREATE**](wm-create.md) se envía una vez creada la ventana.

El [**mensaje \_ WM DESTROY**](wm-destroy.md) se envía cuando la ventana está a punto de destruirse. La [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) se encarga de destruir las ventanas secundarias de la ventana que se va a destruir. El [**mensaje \_ WM NCDESTROY**](wm-ncdestroy.md) se envía justo antes de que se destruya una ventana.

Como mínimo, un procedimiento de ventana debe procesar el [**mensaje \_ WM PAINT**](../gdi/wm-paint.md) para dibujarse a sí mismo. Normalmente, también debe controlar los mensajes del mouse y el teclado. Consulte las descripciones de los mensajes individuales para determinar si el procedimiento de ventana debe controlarlos.

La aplicación puede llamar a [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como parte del procesamiento de un mensaje. En tal caso, la aplicación puede modificar los parámetros del mensaje antes de pasar el mensaje a **DefWindowProc** o puede continuar con el procesamiento predeterminado después de realizar sus propias operaciones.

Un procedimiento de cuadro de diálogo recibe un mensaje [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) en lugar de un mensaje [**WM \_ CREATE**](wm-create.md) y no pasa mensajes sin procesar a la [**función DefDlgProc.**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) De lo contrario, un procedimiento de cuadro de diálogo es exactamente igual que un procedimiento de ventana.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Asociar un procedimiento de ventana a una clase window

Al registrar la clase, se asocia un procedimiento de ventana a una clase de ventana. Debe rellenar una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con información sobre la clase y el miembro **lpfnWndProc** debe especificar la dirección del procedimiento de ventana. Para registrar la clase , pase la dirección de **la estructura WNDCLASS** a la [**función RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Una vez registrada la clase de ventana, el procedimiento de ventana se asocia automáticamente a cada nueva ventana creada con esa clase.

En el ejemplo siguiente se muestra cómo asociar el procedimiento de ventana del ejemplo anterior a una clase de ventana.


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a>Subclases de una ventana

Para crear subclases de una instancia de una ventana, llame a la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) y especifique el identificador de la ventana para crear subclases de la marca WNDPROC de GWL y un puntero al procedimiento \_ de subclase. **SetWindowLong** devuelve un puntero al procedimiento de ventana original; use este puntero para pasar mensajes al procedimiento original. El procedimiento de ventana de subclase debe usar [**la función CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) para llamar al procedimiento de ventana original.

> [!Note]  
> Para escribir código compatible con las versiones de 32 y 64 bits de Windows, use la [**función SetWindowLongPtr.**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

 

En el ejemplo siguiente se muestra cómo crear subclases de una instancia de un control de edición en un cuadro de diálogo. El procedimiento de ventana de subclase permite que el control de edición reciba todas las entradas del teclado, incluidas las teclas ENTRAR y TAB, siempre que el control tenga el foco de entrada.


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
