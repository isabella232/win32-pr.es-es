---
title: Cómo crear un control de encabezado
description: En este tema se muestra cómo crear un control de encabezado y colocarlo dentro del área de cliente de la ventana primaria.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae5bb3ae9c323d30384f5d058a61393bf6425c2a27dfe67faa9cbedd4b3289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063205"
---
# <a name="how-to-create-a-header-control"></a>Cómo crear un control de encabezado

En este tema se muestra cómo crear un control de encabezado y colocarlo dentro del área de cliente de la ventana primaria. Puede crear un control de encabezado mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando la clase de ventana [**\_ WC HEADER**](common-control-window-classes.md) y los estilos de control de encabezado [adecuados.](header-control-styles.md) Esta clase de ventana se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, use la [**función InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


En el siguiente ejemplo de código de C++ se llama primero a [**la función InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para cargar el archivo DLL de control común. A continuación, llama [**a la función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de encabezado. Inicialmente, el control está oculto. El [**mensaje \_ HDM LAYOUT**](hdm-layout.md) se usa para calcular el tamaño y la posición del control dentro de la ventana primaria. A continuación, el control se vuelve a colocar y se hace visible.



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> <dt>

[Referencia de control de encabezado](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Usar controles de encabezado](using-header-controls.md)
</dt> </dl>

 

 