---
title: Modo de Color-Index y administración de la paleta de Windows
description: El modo de índice de color especifica los colores de una paleta lógica con un índice para una entrada específica de la paleta lógica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL en Windows, administración de paletas
- OpenGL en Windows, modo de índice de color
- modo de índice de color OpenGL
- Administración de paletas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076000"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Modo de Color-Index y administración de la paleta de Windows

El modo de índice de color especifica los colores de una paleta lógica con un índice para una entrada específica de la paleta lógica. La mayoría de los programas GDI usan las paletas de índice de color, pero el modo RGBA funciona mejor para OpenGL en varios efectos, como el sombreado, la iluminación, la niebla y la asignación de textura. Si el color más verdadero no es crítico para la aplicación de OpenGL, puede optar por usar el modo de índice de color (por ejemplo, para un mapa topográfico que use "false color" para enfatizar el degradado de elevación).

## <a name="color-index-mode-palette-sample"></a>Ejemplo de paleta modo de Color-Index

En el código siguiente se configura una estructura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) que establece la marca del miembro **iPixelType** en PFD \_ Type \_ COLORINDEX. Esto especifica que la aplicación usa una paleta de índice de color.


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



 

 




