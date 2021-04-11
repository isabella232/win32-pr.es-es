---
title: Cómo crear un control de Tree-View
description: Para crear un control de vista de árbol, utilice la función CreateWindowEx, especificando el \_ valor TREEVIEW de CT para la clase de ventana.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149669"
---
# <a name="how-to-create-a-tree-view-control"></a>Cómo crear un control de Tree-View

Para crear un control de vista de árbol, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando el valor [**\_ TREEVIEW de CT**](common-control-window-classes.md) para la clase de ventana. La clase de ventana de vista de árbol se registra en el espacio de direcciones de la aplicación cuando se carga el archivo DLL de control común. Para asegurarse de que se carga el archivo DLL, utilice la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="create-an-instance-of-a-tree-view-control"></a>Crear una instancia de un control Tree-View

En el ejemplo siguiente se crea un control de vista de árbol cuyo tamaño se ajusta para el área cliente de la ventana primaria. También utiliza funciones definidas por la aplicación para asociar una lista de imágenes con el control y agregar elementos al control.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Observaciones

Al crear un control de vista de árbol, también puede enviarle un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para establecer la fuente que se utilizará para el texto. Debe enviar este mensaje antes de insertar elementos. De forma predeterminada, una vista de árbol utiliza la fuente del título del icono. Aunque puede personalizar la fuente por elemento mediante el uso de [Draw personalizado](custom-draw.md), el control de vista de árbol utiliza las dimensiones de la fuente especificada por el mensaje de **WM de \_ WM** para determinar el espaciado y el diseño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Tree-View](using-treeview.md)
</dt> <dt>

[En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 