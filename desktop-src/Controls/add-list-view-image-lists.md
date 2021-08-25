---
title: Cómo agregar listas List-View imágenes
description: En este tema se muestra cómo agregar listas de imágenes a un control list-view.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8875573634cd47fb5ccb271c3dabfca99daf9061469e31c1178b3e4ed938347e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922065"
---
# <a name="how-to-add-list-view-image-lists"></a>Cómo agregar listas List-View imágenes

En este tema se muestra cómo agregar listas de imágenes a un control list-view.

Solo se crean las listas de imágenes que usa el control. Por ejemplo, si la aplicación no permite al usuario cambiar a la vista de iconos, no es necesario crear ni asignar una lista grande de iconos. Si crea listas de imágenes grandes y pequeñas, deben contener las mismas imágenes en el mismo orden, ya que se usa un valor único para identificar el icono de un elemento de vista de lista en ambas listas de imágenes.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para mostrar imágenes de elementos, debe asignar una lista de imágenes al control list-view. Para ello, use el mensaje [**\_ SETIMAGELIST**](lvm-setimagelist.md) de LVM o la macro [**correspondiente ListView \_ SetImageList,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)especificando si la lista de imágenes contiene iconos de tamaño completo, iconos pequeños o imágenes de estado. Para recuperar el identificador de una lista de imágenes que está asignada actualmente a un control de vista de lista, use el mensaje [**\_ LVM GETIMAGELIST.**](lvm-getimagelist.md) Puede usar la [**función GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar las dimensiones adecuadas para los iconos pequeños y de tamaño completo.

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

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 