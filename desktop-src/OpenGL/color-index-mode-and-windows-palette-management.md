---
title: Color-Index y administración de Windows paleta
description: El modo de índice de colores especifica los colores de una paleta lógica con un índice para una entrada de paleta lógica específica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL on Windows,palette management
- OpenGL en Windows, modo de índice de color
- color-index mode OpenGL
- Administración de paletas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889265"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index y administración de Windows paleta

El modo de índice de colores especifica los colores de una paleta lógica con un índice para una entrada de paleta lógica específica. La mayoría de los programas GDI usan paletas de índices de color, pero el modo RGBA funciona mejor para OpenGL para varios efectos, como sombreado, iluminación, sombra y asignación de textura. Si tener el color más verdadero no es fundamental para la aplicación OpenGL, puede optar por usar el modo de índice de color (por ejemplo, para un mapa topográfico que usa "color falso" para resaltar el degradado de elevación).

## <a name="color-index-mode-palette-sample"></a>ejemplo Color-Index paleta de modo de configuración

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



 

 




