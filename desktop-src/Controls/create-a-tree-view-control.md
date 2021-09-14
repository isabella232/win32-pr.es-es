---
title: Cómo crear un control Tree-View control
description: Para crear un control de vista de árbol, use la función CreateWindowEx y especifique el valor TREEVIEW de WC \_ para la clase de ventana.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254558"
---
# <a name="how-to-create-a-tree-view-control"></a>Cómo crear un control Tree-View control

Para crear un control de vista de árbol, use la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique el valor [**\_ TREEVIEW de WC**](common-control-window-classes.md) para la clase de ventana. La clase de ventana de vista de árbol se registra en el espacio de direcciones de la aplicación cuando se carga la DLL de control común. Para asegurarse de que se carga el archivo DLL, use la [**función InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-an-instance-of-a-tree-view-control"></a>Crear una instancia de un control Tree-View control

En el ejemplo siguiente se crea un control de vista de árbol con el tamaño adecuado para ajustarse al área de cliente de la ventana primaria. También usa funciones definidas por la aplicación para asociar una lista de imágenes al control y agregar elementos al control.


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

Al crear un control de vista de árbol, también puede enviarle un mensaje [**\_ WM SETFONT**](/windows/desktop/winmsg/wm-setfont) para establecer la fuente que se usará para el texto. Debe enviar este mensaje antes de insertar los elementos. De forma predeterminada, una vista de árbol usa la fuente de título del icono. Aunque puede personalizar la fuente por elemento mediante El dibujo personalizado [,](custom-draw.md)el control de vista de árbol usa las dimensiones de la fuente especificada por el mensaje **WM \_ SETFONT** para determinar el espaciado y el diseño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Tree-View controles](using-treeview.md)
</dt> <dt>

[El ejemplo CustDTv muestra el dibujo personalizado en un control Tree-View datos](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 