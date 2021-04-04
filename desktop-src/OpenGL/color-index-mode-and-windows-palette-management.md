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
# <a name="color-index-mode-and-windows-palette-management"></a><span data-ttu-id="2f8d4-107">Modo de Color-Index y administración de la paleta de Windows</span><span class="sxs-lookup"><span data-stu-id="2f8d4-107">Color-Index Mode and Windows Palette Management</span></span>

<span data-ttu-id="2f8d4-108">El modo de índice de color especifica los colores de una paleta lógica con un índice para una entrada específica de la paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-108">The color-index mode specifies colors in a logical palette with an index to a specific logical-palette entry.</span></span> <span data-ttu-id="2f8d4-109">La mayoría de los programas GDI usan las paletas de índice de color, pero el modo RGBA funciona mejor para OpenGL en varios efectos, como el sombreado, la iluminación, la niebla y la asignación de textura.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-109">Most GDI programs use color-index palettes, but the RGBA mode works better for OpenGL for several effects, such as shading, lighting, fog, and texture mapping.</span></span> <span data-ttu-id="2f8d4-110">Si el color más verdadero no es crítico para la aplicación de OpenGL, puede optar por usar el modo de índice de color (por ejemplo, para un mapa topográfico que use "false color" para enfatizar el degradado de elevación).</span><span class="sxs-lookup"><span data-stu-id="2f8d4-110">If having the truest color isn't critical for your OpenGL application, you might choose to use the color-index mode (for example, for a topographic map that uses "false color" to emphasize the elevation gradient).</span></span>

## <a name="color-index-mode-palette-sample"></a><span data-ttu-id="2f8d4-111">Ejemplo de paleta modo de Color-Index</span><span class="sxs-lookup"><span data-stu-id="2f8d4-111">Color-Index Mode Palette Sample</span></span>

<span data-ttu-id="2f8d4-112">En el código siguiente se configura una estructura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) que establece la marca del miembro **iPixelType** en PFD \_ Type \_ COLORINDEX.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-112">The following code sets up a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure that sets the flag of the **iPixelType** member to PFD\_TYPE\_COLORINDEX.</span></span> <span data-ttu-id="2f8d4-113">Esto especifica que la aplicación usa una paleta de índice de color.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-113">This specifies that the application use a color-index palette.</span></span>


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



 

 




