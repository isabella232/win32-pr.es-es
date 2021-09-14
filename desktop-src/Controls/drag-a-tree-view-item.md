---
title: Cómo arrastrar un elemento Tree-View de datos
description: En este tema se muestra el código para controlar el arrastre y la colocación de elementos de vista de árbol.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174133"
---
# <a name="how-to-drag-a-tree-view-item"></a>Cómo arrastrar un elemento Tree-View de datos

En este tema se muestra el código para controlar el arrastre y la colocación de elementos de vista de árbol. El código de ejemplo consta de tres funciones. La primera función comienza la operación de arrastre, la segunda función arrastra la imagen y la tercera finaliza la operación de arrastre.

> [!Note]  
> Arrastrar un elemento de vista de árbol normalmente implica procesar el código de notificación [ \_ TVN BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG),](tvn-beginrdrag.md)el mensaje [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) y el mensaje [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP).**](/windows/desktop/inputdev/wm-rbuttonup) También implica el uso de las [funciones Listas de](image-lists.md) imágenes para dibujar el elemento mientras se arrastra.

 

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Paso 1: Inicio de la operación de arrastre de la vista de árbol

Un control de vista de árbol envía a la ventana primaria un código de notificación [ \_ TVN BEGINDRAG](tvn-begindrag.md) [(o TVN \_ BEGINRDRAG)](tvn-beginrdrag.md)cada vez que el usuario empieza a arrastrar un elemento. La ventana primaria recibe la notificación en forma de mensaje [**\_ WM NOTIFY**](wm-notify.md) cuyo parámetro *lParam* es la dirección de una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Los miembros de esta estructura incluyen las coordenadas de pantalla del puntero del mouse y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información sobre el elemento que se va a arrastrar.

En el ejemplo siguiente se muestra cómo procesar el mensaje [**\_ WM NOTIFY**](wm-notify.md) para obtener [TVN \_ BEGINDRAG](tvn-begindrag.md).


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



El inicio de la operación de arrastre implica el uso [**de la \_ función BeginDrag de ImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) Los parámetros de la función incluyen el identificador de la lista de imágenes que contiene la imagen que se va a usar durante la operación de arrastre y el índice de la imagen. Puede proporcionar su propia lista de imágenes e imagen, o puede hacer que el control de vista de árbol los cree automáticamente mediante el mensaje [**DE TVM \_ CREATEDRAGIMAGE.**](tvm-createdragimage.md)

Dado que la imagen de arrastre reemplaza el puntero del mouse durante la operación de arrastre, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requiere que se especifique un punto de acceso en la imagen. Las coordenadas de la zona de acceso es relativa a la esquina superior izquierda de la imagen. **ImageList \_ BeginDrag también** requiere que especifique la ubicación inicial de la imagen de arrastre. Normalmente, una aplicación establece la ubicación inicial para que la zona activa de la imagen de arrastre se corresponda con la del puntero del mouse en el momento en que el usuario inició la operación de arrastre.

La siguiente función muestra cómo empezar a arrastrar un elemento de vista de árbol. Usa la imagen de arrastre proporcionada por el control de vista de árbol y obtiene el rectángulo delimitador del elemento para determinar el punto adecuado para la zona de acceso. Las dimensiones del rectángulo delimitador son las mismas que las de la imagen.

La función captura la entrada del mouse, lo que hace que los mensajes del mouse se envíen a la ventana primaria. La ventana primaria necesita los mensajes [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) posteriores para determinar dónde arrastrar la imagen y el mensaje [**\_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) de WM para determinar cuándo finalizar la operación de arrastre.


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



### <a name="step-2-dragging-the-tree-view-item"></a>Paso 2: Arrastrar el elemento de vista de árbol

Arrastre un elemento de vista de árbol llamando a la función [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) cuando la ventana primaria reciba un [**mensaje WM \_ MOUSEMOVE,**](/windows/desktop/inputdev/wm-mousemove) como se muestra en el ejemplo siguiente. En el ejemplo también se muestra cómo realizar pruebas de acceso durante la operación de arrastrar para determinar si se deben resaltar otros elementos de la vista de árbol como destinos de una operación de arrastrar y colocar.


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Paso 3: Finalización de la operación de arrastre de la vista de árbol

En el ejemplo siguiente se muestra cómo finalizar una operación de arrastre. Se [**llama a la función \_ ImageList EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) cuando la ventana primaria recibe un [**mensaje \_ LBUTTONUP de WM.**](/windows/desktop/inputdev/wm-lbuttonup) El identificador del control de vista de árbol se pasa a la función .


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

[Usar Tree-View controles](using-treeview.md)
</dt> <dt>

[El ejemplo CustDTv muestra el dibujo personalizado en un control Tree-View datos](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 