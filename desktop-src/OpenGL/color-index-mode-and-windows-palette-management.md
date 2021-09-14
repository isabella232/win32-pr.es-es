---
title: Color-Index y administración de Windows paleta de aplicaciones
description: El modo de índice de colores especifica los colores de una paleta lógica con un índice para una entrada de paleta lógica específica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL en Windows, administración de paletas
- OpenGL en Windows, modo de índice de color
- modo de índice de colores OpenGL
- Administración de paletas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161129"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index y administración de Windows paleta de aplicaciones

El modo de índice de colores especifica los colores de una paleta lógica con un índice para una entrada de paleta lógica específica. La mayoría de los programas GDI usan paletas de índices de color, pero el modo RGBA funciona mejor para OpenGL para varios efectos, como sombreado, iluminación, sonido y asignación de textura. Si tener el color más verdadero no es fundamental para la aplicación OpenGL, puede optar por usar el modo de índice de colores (por ejemplo, para un mapa topográfico que usa "color falso" para resaltar el degradado de elevación).

## <a name="color-index-mode-palette-sample"></a>Color-Index de paleta de modo de mantenimiento

El código siguiente configura una [**estructura PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) que establece la marca del miembro **iPixelType** en PFD \_ TYPE \_ COLORINDEX. Esto especifica que la aplicación usa una paleta de índices de color.


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




