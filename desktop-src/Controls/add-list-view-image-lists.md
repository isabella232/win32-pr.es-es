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
# <a name="how-to-add-list-view-image-lists"></a>Cómo agregar List-View listas de imágenes

En este tema se muestra cómo agregar listas de imágenes a un control de vista de lista.

Solo creará las listas de imágenes que utiliza el control. Por ejemplo, si la aplicación no permite al usuario cambiar a la vista de iconos, no es necesario crear y asignar una lista de iconos grandes. Si crea listas de imágenes grandes y pequeñas, deben contener las mismas imágenes en el mismo orden, ya que se usa un solo valor para identificar el icono de un elemento de vista de lista en ambas listas de imágenes.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Para mostrar imágenes de elementos, debe asignar una lista de imágenes al control de vista de lista. Para ello, use el mensaje [**LVM \_ SETIMAGELIST**](lvm-setimagelist.md) o la macro ListView correspondiente [**\_ SETIMAGELIST**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), especificando si la lista de imágenes contiene iconos de tamaño completo, iconos pequeños o imágenes de estado. Para recuperar el identificador de una lista de imágenes asignada actualmente a un control de vista de lista, use el mensaje [**\_ GETIMAGELIST de LVM**](lvm-getimagelist.md) . Puede usar la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar las dimensiones adecuadas para los iconos pequeños y de tamaño completo.

En el siguiente ejemplo de código de C++, la función definida por la aplicación crea primero listas de imágenes y, a continuación, las asigna a un control de vista de lista.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de vista de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

 