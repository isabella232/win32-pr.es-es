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
# <a name="how-to-add-tree-view-items"></a>Cómo agregar elementos de Tree-View

Un elemento se agrega a un control de vista de árbol mediante el envío del mensaje de la [**\_ INSERTITEM de TVM**](tvm-insertitem.md) al control. El mensaje incluye la dirección de una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , especificando el elemento primario, el elemento después del cual se inserta el nuevo elemento y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define los atributos del elemento. Los atributos incluyen la etiqueta del elemento, sus imágenes seleccionadas y no seleccionadas y un valor definido por la aplicación de 32 bits.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="add-items-to-the-tree-view"></a>Agregar elementos al Tree-View

En el ejemplo de esta sección se muestra cómo crear una tabla de contenido basada en la información de encabezado del documento que se proporciona en una matriz definida por la aplicación. Cada elemento de matriz consta de una cadena de encabezado y un entero que indica el nivel de encabezado. El ejemplo admite tres niveles de encabezado (1, 2 y 3).

En el ejemplo se incluyen dos funciones. La primera función extrae cada encabezado y el nivel de encabezado adjunto y, a continuación, los pasa a la segunda función.

La segunda función agrega un elemento a un control de vista de árbol. Usa el texto del encabezado como etiqueta del elemento y usa el nivel de encabezado para determinar el elemento primario del nuevo elemento. Se agrega un encabezado de nivel uno a la raíz del control de vista de árbol, se agrega un encabezado de nivel dos como elemento secundario del nivel anterior un elemento, y así sucesivamente. La función asigna una imagen a un elemento en función de si tiene elementos secundarios. Si un elemento tiene elementos secundarios, obtiene una imagen que representa una carpeta cerrada. De lo contrario, obtiene una imagen que representa un documento. Un elemento usa la misma imagen tanto para los Estados seleccionados como para los no seleccionados.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Tree-View](using-treeview.md)
</dt> <dt>

[En el ejemplo CustDTv se muestra el dibujo personalizado en un control Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




