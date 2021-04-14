---
title: Cómo agregar List-View listas de imágenes
description: En este tema se muestra cómo agregar listas de imágenes a un control de vista de lista.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359523"
---
# <a name="how-to-add-list-view-image-lists"></a><span data-ttu-id="1b5d8-103">Cómo agregar List-View listas de imágenes</span><span class="sxs-lookup"><span data-stu-id="1b5d8-103">How to Add List-View Image Lists</span></span>

<span data-ttu-id="1b5d8-104">En este tema se muestra cómo agregar listas de imágenes a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-104">This topic demonstrates how to add image lists to a list-view control.</span></span>

<span data-ttu-id="1b5d8-105">Solo creará las listas de imágenes que utiliza el control.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-105">You create only the image lists that the control uses.</span></span> <span data-ttu-id="1b5d8-106">Por ejemplo, si la aplicación no permite al usuario cambiar a la vista de iconos, no es necesario crear y asignar una lista de iconos grandes.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-106">For example, if your application does not allow the user to switch to icon view, you do not need to create and assign a large icon list.</span></span> <span data-ttu-id="1b5d8-107">Si crea listas de imágenes grandes y pequeñas, deben contener las mismas imágenes en el mismo orden, ya que se usa un solo valor para identificar el icono de un elemento de vista de lista en ambas listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-107">If you create both large and small image lists, they must contain the same images in the same order, because a single value is used to identify a list-view item's icon in both image lists.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1b5d8-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="1b5d8-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1b5d8-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="1b5d8-109">Technologies</span></span>

-   [<span data-ttu-id="1b5d8-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="1b5d8-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1b5d8-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1b5d8-111">Prerequisites</span></span>

-   <span data-ttu-id="1b5d8-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="1b5d8-112">C/C++</span></span>
-   <span data-ttu-id="1b5d8-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="1b5d8-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1b5d8-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="1b5d8-114">Instructions</span></span>


<span data-ttu-id="1b5d8-115">Para mostrar imágenes de elementos, debe asignar una lista de imágenes al control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-115">To display item images, you must assign an image list to the list-view control.</span></span> <span data-ttu-id="1b5d8-116">Para ello, use el mensaje [**LVM \_ SETIMAGELIST**](lvm-setimagelist.md) o la macro ListView correspondiente [**\_ SETIMAGELIST**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), especificando si la lista de imágenes contiene iconos de tamaño completo, iconos pequeños o imágenes de estado.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-116">To do this, use the [**LVM\_SETIMAGELIST**](lvm-setimagelist.md) message or the corresponding macro [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), specifying whether the image list contains full-sized icons, small icons, or state images.</span></span> <span data-ttu-id="1b5d8-117">Para recuperar el identificador de una lista de imágenes asignada actualmente a un control de vista de lista, use el mensaje [**\_ GETIMAGELIST de LVM**](lvm-getimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="1b5d8-117">To retrieve the handle to an image list that is currently assigned to a list-view control, use the [**LVM\_GETIMAGELIST**](lvm-getimagelist.md) message.</span></span> <span data-ttu-id="1b5d8-118">Puede usar la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar las dimensiones adecuadas para los iconos pequeños y de tamaño completo.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-118">You can use the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to determine appropriate dimensions for the full-sized and small icons.</span></span>

<span data-ttu-id="1b5d8-119">En el siguiente ejemplo de código de C++, la función definida por la aplicación crea primero listas de imágenes y, a continuación, las asigna a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1b5d8-119">In the following C++ code example, the application-defined function first creates image lists and then assigns them to a list-view control.</span></span>


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="1b5d8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b5d8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b5d8-121">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="1b5d8-121">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1b5d8-122">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="1b5d8-122">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="1b5d8-123">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="1b5d8-123">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 