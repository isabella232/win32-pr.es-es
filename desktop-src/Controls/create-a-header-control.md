---
title: Cómo crear un control de encabezado
description: En este tema se muestra cómo crear un control de encabezado y colocarlo en el área de cliente de la ventana primaria.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078631"
---
# <a name="how-to-create-a-header-control"></a>Cómo crear un control de encabezado

En este tema se muestra cómo crear un control de encabezado y colocarlo en el área de cliente de la ventana primaria. Puede crear un control de encabezado mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando la clase de ventana de [**\_ encabezado WC**](common-control-window-classes.md) y los [estilos de control de encabezado](header-control-styles.md)adecuados. Esta clase de ventana se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, utilice la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


En el siguiente ejemplo de código de C++ se llama primero a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para cargar el archivo dll de control común. A continuación, llama a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de encabezado. El control está oculto inicialmente. El mensaje de [**\_ diseño HDM**](hdm-layout.md) se usa para calcular el tamaño y la posición del control dentro de la ventana primaria. Después, el control cambia de posición y se hace visible.



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

 

 