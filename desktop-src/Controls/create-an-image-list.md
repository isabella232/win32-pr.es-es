---
title: Cómo crear una lista de imágenes
description: En este tema se muestra cómo usar la función ImageList \_ Create para crear una lista de imágenes.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04e3e22894546e887e1a4ca5348518b4e4a35c45f4a26b5b6125b81f9323bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826485"
---
# <a name="how-to-create-an-image-list"></a>Cómo crear una lista de imágenes

En este tema se muestra cómo usar la [**función ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para crear una lista de imágenes.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para crear una lista de imágenes, llame a [**la función ImageList \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) Los parámetros incluyen el tipo de lista de imágenes que se va a crear, las dimensiones de cada imagen y el número de imágenes que se pretende agregar a la lista.

En el ejemplo siguiente se crea una lista de imágenes enmascaradas y se usa la macro [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) para agregar dos iconos a la lista.



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de listas de imágenes](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Acerca de las listas de imágenes](image-lists.md)
</dt> <dt>

[Usar listas de imágenes](using-image-lists.md)
</dt> </dl>

 

 




