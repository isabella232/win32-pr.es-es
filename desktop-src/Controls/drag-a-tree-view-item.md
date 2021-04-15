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
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="38f52-103">Cómo arrastrar un elemento de Tree-View</span><span class="sxs-lookup"><span data-stu-id="38f52-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="38f52-104">En este tema se muestra el código para controlar el arrastre y la colocación de los elementos de la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="38f52-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="38f52-105">El código de ejemplo consta de tres funciones.</span><span class="sxs-lookup"><span data-stu-id="38f52-105">The sample code consists of three functions.</span></span> <span data-ttu-id="38f52-106">La primera función comienza la operación de arrastre, la segunda función arrastra la imagen y la tercera función finaliza la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="38f52-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="38f52-107">Arrastrar un elemento de vista de árbol implica normalmente el procesamiento del código de notificación [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)), el mensaje de de WM y el mensaje de WM [**\_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)). [**\_**](/windows/desktop/inputdev/wm-mousemove)</span><span class="sxs-lookup"><span data-stu-id="38f52-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="38f52-108">También implica el uso de las funciones de las [listas de imágenes](image-lists.md) para dibujar el elemento a medida que se arrastra.</span><span class="sxs-lookup"><span data-stu-id="38f52-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="38f52-109">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="38f52-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="38f52-110">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="38f52-110">Technologies</span></span>

-   [<span data-ttu-id="38f52-111">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="38f52-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="38f52-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38f52-112">Prerequisites</span></span>

-   <span data-ttu-id="38f52-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="38f52-113">C/C++</span></span>
-   <span data-ttu-id="38f52-114">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="38f52-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="38f52-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="38f52-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="38f52-116">Paso 1: Inicio de la operación de arrastre de la vista de árbol</span><span class="sxs-lookup"><span data-stu-id="38f52-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="38f52-117">Un control de vista de árbol envía a la ventana primaria un código de notificación [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) cada vez que el usuario comienza a arrastrar un elemento.</span><span class="sxs-lookup"><span data-stu-id="38f52-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="38f52-118">La ventana primaria recibe la notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) cuyo parámetro *lParam* es la dirección de una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="38f52-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="38f52-119">Los miembros de esta estructura incluyen las coordenadas de pantalla del puntero del mouse y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información sobre el elemento que se va a arrastrar.</span><span class="sxs-lookup"><span data-stu-id="38f52-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="38f52-120">En el ejemplo siguiente se muestra cómo procesar el mensaje de [**\_ notificación de WM**](wm-notify.md) para obtener [TVN \_ BEGINDRAG](tvn-begindrag.md).</span><span class="sxs-lookup"><span data-stu-id="38f52-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


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



<span data-ttu-id="38f52-121">El inicio de la operación de arrastre implica el uso de la función [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="38f52-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="38f52-122">Los parámetros de la función incluyen el identificador de la lista de imágenes que contiene la imagen que se va a usar durante la operación de arrastre y el índice de la imagen.</span><span class="sxs-lookup"><span data-stu-id="38f52-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="38f52-123">Puede proporcionar su propia imagen y lista de imágenes, o bien puede hacer que el control de vista de árbol las cree automáticamente mediante el mensaje [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .</span><span class="sxs-lookup"><span data-stu-id="38f52-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="38f52-124">Dado que la imagen de arrastre reemplaza el puntero del mouse mientras dure la operación de arrastre, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requiere que se especifique una zona activa dentro de la imagen.</span><span class="sxs-lookup"><span data-stu-id="38f52-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="38f52-125">Las coordenadas de la zona activa son relativas a la esquina superior izquierda de la imagen.</span><span class="sxs-lookup"><span data-stu-id="38f52-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="38f52-126">**ImageList \_ BeginDrag** también requiere que se especifique la ubicación inicial de la imagen de arrastre.</span><span class="sxs-lookup"><span data-stu-id="38f52-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="38f52-127">Normalmente, una aplicación establece la ubicación inicial para que la zona activa de la imagen de arrastre se corresponda con la del puntero del mouse en el momento en que el usuario comenzó la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="38f52-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="38f52-128">La siguiente función muestra cómo empezar a arrastrar un elemento de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="38f52-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="38f52-129">Usa la imagen de arrastre proporcionada por el control de vista de árbol y obtiene el rectángulo delimitador del elemento para determinar el punto adecuado para la zona activa.</span><span class="sxs-lookup"><span data-stu-id="38f52-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="38f52-130">Las dimensiones del rectángulo delimitador son las mismas que las de la imagen.</span><span class="sxs-lookup"><span data-stu-id="38f52-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="38f52-131">La función captura la entrada del mouse, lo que hace que los mensajes del mouse se envíen a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="38f52-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="38f52-132">La ventana primaria necesita los mensajes de Windows de [**WM \_**](/windows/desktop/inputdev/wm-mousemove) posteriores para determinar dónde arrastrar la imagen y el mensaje de [**\_ LBUTTONUP de WM**](/windows/desktop/inputdev/wm-lbuttonup) para determinar cuándo finalizar la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="38f52-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


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



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="38f52-133">Paso 2: arrastrar el elemento de vista de árbol</span><span class="sxs-lookup"><span data-stu-id="38f52-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="38f52-134">Para arrastrar un elemento de vista de árbol, llame a la función [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) cuando la ventana primaria reciba un mensaje de Windows de [**WM \_**](/windows/desktop/inputdev/wm-mousemove) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="38f52-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="38f52-135">En el ejemplo también se muestra cómo realizar pruebas de posicionamiento durante la operación de arrastre para determinar si se deben resaltar otros elementos en la vista de árbol como destinos de una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="38f52-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="38f52-136">Paso 3: finalizar la operación de arrastre de la vista de árbol</span><span class="sxs-lookup"><span data-stu-id="38f52-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="38f52-137">En el ejemplo siguiente se muestra cómo finalizar una operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="38f52-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="38f52-138">Se llama a la función [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) cuando la ventana primaria recibe un mensaje [**de \_ LBUTTONUP de WM**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="38f52-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="38f52-139">El identificador del control de vista de árbol se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="38f52-139">The handle of the tree-view control is passed to the function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38f52-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38f52-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f52-141">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="38f52-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="38f52-142">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="38f52-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 