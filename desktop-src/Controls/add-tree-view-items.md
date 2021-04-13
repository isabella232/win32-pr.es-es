---
title: Cómo agregar elementos de Tree-View
description: Un elemento se agrega a un control de vista de árbol mediante el envío del mensaje de la INSERTITEM de TVM \_ al control.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420331"
---
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="01e49-103">Cómo agregar elementos de Tree-View</span><span class="sxs-lookup"><span data-stu-id="01e49-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="01e49-104">Un elemento se agrega a un control de vista de árbol mediante el envío del mensaje de la [**\_ INSERTITEM de TVM**](tvm-insertitem.md) al control.</span><span class="sxs-lookup"><span data-stu-id="01e49-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="01e49-105">El mensaje incluye la dirección de una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , especificando el elemento primario, el elemento después del cual se inserta el nuevo elemento y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define los atributos del elemento.</span><span class="sxs-lookup"><span data-stu-id="01e49-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="01e49-106">Los atributos incluyen la etiqueta del elemento, sus imágenes seleccionadas y no seleccionadas y un valor definido por la aplicación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="01e49-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="01e49-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="01e49-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="01e49-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="01e49-108">Technologies</span></span>

-   [<span data-ttu-id="01e49-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="01e49-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="01e49-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01e49-110">Prerequisites</span></span>

-   <span data-ttu-id="01e49-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="01e49-111">C/C++</span></span>
-   <span data-ttu-id="01e49-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="01e49-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="01e49-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="01e49-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="01e49-114">Agregar elementos al Tree-View</span><span class="sxs-lookup"><span data-stu-id="01e49-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="01e49-115">En el ejemplo de esta sección se muestra cómo crear una tabla de contenido basada en la información de encabezado del documento que se proporciona en una matriz definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="01e49-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="01e49-116">Cada elemento de matriz consta de una cadena de encabezado y un entero que indica el nivel de encabezado.</span><span class="sxs-lookup"><span data-stu-id="01e49-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="01e49-117">El ejemplo admite tres niveles de encabezado (1, 2 y 3).</span><span class="sxs-lookup"><span data-stu-id="01e49-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="01e49-118">En el ejemplo se incluyen dos funciones.</span><span class="sxs-lookup"><span data-stu-id="01e49-118">The example includes two functions.</span></span> <span data-ttu-id="01e49-119">La primera función extrae cada encabezado y el nivel de encabezado adjunto y, a continuación, los pasa a la segunda función.</span><span class="sxs-lookup"><span data-stu-id="01e49-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="01e49-120">La segunda función agrega un elemento a un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="01e49-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="01e49-121">Usa el texto del encabezado como etiqueta del elemento y usa el nivel de encabezado para determinar el elemento primario del nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="01e49-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="01e49-122">Se agrega un encabezado de nivel uno a la raíz del control de vista de árbol, se agrega un encabezado de nivel dos como elemento secundario del nivel anterior un elemento, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="01e49-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="01e49-123">La función asigna una imagen a un elemento en función de si tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="01e49-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="01e49-124">Si un elemento tiene elementos secundarios, obtiene una imagen que representa una carpeta cerrada.</span><span class="sxs-lookup"><span data-stu-id="01e49-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="01e49-125">De lo contrario, obtiene una imagen que representa un documento.</span><span class="sxs-lookup"><span data-stu-id="01e49-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="01e49-126">Un elemento usa la misma imagen tanto para los Estados seleccionados como para los no seleccionados.</span><span class="sxs-lookup"><span data-stu-id="01e49-126">An item uses the same image for both the selected and nonselected states.</span></span>


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="01e49-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01e49-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e49-128">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="01e49-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="01e49-129">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="01e49-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




