---
title: Cómo arrastrar un elemento de Tree-View
description: En este tema se muestra el código para controlar el arrastre y la colocación de los elementos de la vista de árbol.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488402"
---
# <a name="how-to-drag-a-tree-view-item"></a>Cómo arrastrar un elemento de Tree-View

En este tema se muestra el código para controlar el arrastre y la colocación de los elementos de la vista de árbol. El código de ejemplo consta de tres funciones. La primera función comienza la operación de arrastre, la segunda función arrastra la imagen y la tercera función finaliza la operación de arrastre.

> [!Note]  
> Arrastrar un elemento de vista de árbol implica normalmente el procesamiento del código de notificación [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)), el mensaje de de WM y el mensaje de WM [**\_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)). [**\_**](/windows/desktop/inputdev/wm-mousemove) También implica el uso de las funciones de las [listas de imágenes](image-lists.md) para dibujar el elemento a medida que se arrastra.

 

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Paso 1: Inicio de la operación de arrastre de la vista de árbol

Un control de vista de árbol envía a la ventana primaria un código de notificación [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) cada vez que el usuario comienza a arrastrar un elemento. La ventana primaria recibe la notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) cuyo parámetro *lParam* es la dirección de una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Los miembros de esta estructura incluyen las coordenadas de pantalla del puntero del mouse y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información sobre el elemento que se va a arrastrar.

En el ejemplo siguiente se muestra cómo procesar el mensaje de [**\_ notificación de WM**](wm-notify.md) para obtener [TVN \_ BEGINDRAG](tvn-begindrag.md).


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



El inicio de la operación de arrastre implica el uso de la función [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) . Los parámetros de la función incluyen el identificador de la lista de imágenes que contiene la imagen que se va a usar durante la operación de arrastre y el índice de la imagen. Puede proporcionar su propia imagen y lista de imágenes, o bien puede hacer que el control de vista de árbol las cree automáticamente mediante el mensaje [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .

Dado que la imagen de arrastre reemplaza el puntero del mouse mientras dure la operación de arrastre, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requiere que se especifique una zona activa dentro de la imagen. Las coordenadas de la zona activa son relativas a la esquina superior izquierda de la imagen. **ImageList \_ BeginDrag** también requiere que se especifique la ubicación inicial de la imagen de arrastre. Normalmente, una aplicación establece la ubicación inicial para que la zona activa de la imagen de arrastre se corresponda con la del puntero del mouse en el momento en que el usuario comenzó la operación de arrastre.

La siguiente función muestra cómo empezar a arrastrar un elemento de vista de árbol. Usa la imagen de arrastre proporcionada por el control de vista de árbol y obtiene el rectángulo delimitador del elemento para determinar el punto adecuado para la zona activa. Las dimensiones del rectángulo delimitador son las mismas que las de la imagen.

La función captura la entrada del mouse, lo que hace que los mensajes del mouse se envíen a la ventana primaria. La ventana primaria necesita los mensajes de Windows de [**WM \_**](/windows/desktop/inputdev/wm-mousemove) posteriores para determinar dónde arrastrar la imagen y el mensaje de [**\_ LBUTTONUP de WM**](/windows/desktop/inputdev/wm-lbuttonup) para determinar cuándo finalizar la operación de arrastre.


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a>Paso 2: arrastrar el elemento de vista de árbol

Para arrastrar un elemento de vista de árbol, llame a la función [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) cuando la ventana primaria reciba un mensaje de Windows de [**WM \_**](/windows/desktop/inputdev/wm-mousemove) , como se muestra en el ejemplo siguiente. En el ejemplo también se muestra cómo realizar pruebas de posicionamiento durante la operación de arrastre para determinar si se deben resaltar otros elementos en la vista de árbol como destinos de una operación de arrastrar y colocar.


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Paso 3: finalizar la operación de arrastre de la vista de árbol

En el ejemplo siguiente se muestra cómo finalizar una operación de arrastre. Se llama a la función [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) cuando la ventana primaria recibe un mensaje [**de \_ LBUTTONUP de WM**](/windows/desktop/inputdev/wm-lbuttonup) . El identificador del control de vista de árbol se pasa a la función.


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Tree-View](using-treeview.md)
</dt> <dt>

[En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 