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
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="cd8e8-103">Cómo crear un control de Tree-View</span><span class="sxs-lookup"><span data-stu-id="cd8e8-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="cd8e8-104">Para crear un control de vista de árbol, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando el valor [**\_ TREEVIEW de CT**](common-control-window-classes.md) para la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="cd8e8-105">La clase de ventana de vista de árbol se registra en el espacio de direcciones de la aplicación cuando se carga el archivo DLL de control común.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="cd8e8-106">Para asegurarse de que se carga el archivo DLL, utilice la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="cd8e8-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cd8e8-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="cd8e8-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cd8e8-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="cd8e8-108">Technologies</span></span>

-   [<span data-ttu-id="cd8e8-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="cd8e8-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cd8e8-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd8e8-110">Prerequisites</span></span>

-   <span data-ttu-id="cd8e8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="cd8e8-111">C/C++</span></span>
-   <span data-ttu-id="cd8e8-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="cd8e8-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cd8e8-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cd8e8-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="cd8e8-114">Crear una instancia de un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="cd8e8-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="cd8e8-115">En el ejemplo siguiente se crea un control de vista de árbol cuyo tamaño se ajusta para el área cliente de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="cd8e8-116">También utiliza funciones definidas por la aplicación para asociar una lista de imágenes con el control y agregar elementos al control.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="cd8e8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd8e8-117">Remarks</span></span>

<span data-ttu-id="cd8e8-118">Al crear un control de vista de árbol, también puede enviarle un mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para establecer la fuente que se utilizará para el texto.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="cd8e8-119">Debe enviar este mensaje antes de insertar elementos.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="cd8e8-120">De forma predeterminada, una vista de árbol utiliza la fuente del título del icono.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="cd8e8-121">Aunque puede personalizar la fuente por elemento mediante el uso de [Draw personalizado](custom-draw.md), el control de vista de árbol utiliza las dimensiones de la fuente especificada por el mensaje de **WM de \_ WM** para determinar el espaciado y el diseño.</span><span class="sxs-lookup"><span data-stu-id="cd8e8-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd8e8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd8e8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd8e8-123">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="cd8e8-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="cd8e8-124">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="cd8e8-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 