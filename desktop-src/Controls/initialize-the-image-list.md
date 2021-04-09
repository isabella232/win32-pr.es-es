---
title: Cómo inicializar la lista de imágenes
description: Cada elemento de un control de vista de árbol puede tener dos imágenes asociadas a él.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149096"
---
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="1c688-103">Cómo inicializar la lista de imágenes</span><span class="sxs-lookup"><span data-stu-id="1c688-103">How to Initialize the Image List</span></span>

<span data-ttu-id="1c688-104">Cada elemento de un control de vista de árbol puede tener dos imágenes asociadas a él.</span><span class="sxs-lookup"><span data-stu-id="1c688-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="1c688-105">Un elemento muestra una imagen cuando se selecciona y la otra cuando no lo está.</span><span class="sxs-lookup"><span data-stu-id="1c688-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="1c688-106">Para incluir imágenes con elementos de vista de árbol, use primero las funciones de las [listas de imágenes](image-lists.md) para crear una lista de imágenes y agregarle imágenes.</span><span class="sxs-lookup"><span data-stu-id="1c688-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="1c688-107">A continuación, asocie la lista de imágenes con el control de vista de árbol mediante el mensaje [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="1c688-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1c688-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="1c688-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1c688-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="1c688-109">Technologies</span></span>

-   [<span data-ttu-id="1c688-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="1c688-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1c688-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c688-111">Prerequisites</span></span>

-   <span data-ttu-id="1c688-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="1c688-112">C/C++</span></span>
-   <span data-ttu-id="1c688-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="1c688-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1c688-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="1c688-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="1c688-115">Inicialización de la lista de imágenes</span><span class="sxs-lookup"><span data-stu-id="1c688-115">Initialize the Image List</span></span>

<span data-ttu-id="1c688-116">En el ejemplo siguiente se crea una lista de imágenes, se agregan tres mapas de bits a la lista y se asocia la lista de imágenes con un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="1c688-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="1c688-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c688-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c688-118">Usar controles Tree-View</span><span class="sxs-lookup"><span data-stu-id="1c688-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="1c688-119">En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View</span><span class="sxs-lookup"><span data-stu-id="1c688-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




