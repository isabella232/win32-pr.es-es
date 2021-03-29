---
title: Recortar una imagen
description: Recortar una imagen
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- MCIWndGetSource (macro)
- MCIWndPutSource (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486758"
---
# <a name="cropping-an-image"></a><span data-ttu-id="d025e-105">Recortar una imagen</span><span class="sxs-lookup"><span data-stu-id="d025e-105">Cropping an Image</span></span>

<span data-ttu-id="d025e-106">En el ejemplo siguiente se crea una ventana de MCIWnd y se carga un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="d025e-106">The following example creates an MCIWnd window and loads an AVI file.</span></span> <span data-ttu-id="d025e-107">La ventana incluye un comando de recorte en el menú, que recorta un cuarto del alto o el ancho de cada uno de los cuatro lados del marco.</span><span class="sxs-lookup"><span data-stu-id="d025e-107">The window includes a crop command in the menu, which crops one-quarter of the height or width from each of the four sides of the frame.</span></span> <span data-ttu-id="d025e-108">En el ejemplo se recuperan las dimensiones actuales (iniciales) del rectángulo de origen mediante la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="d025e-108">The example retrieves the current (initial) dimensions of the source rectangle by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span> <span data-ttu-id="d025e-109">El rectángulo de origen modificado es la mitad del alto y el ancho originales y está centrado en el fotograma original.</span><span class="sxs-lookup"><span data-stu-id="d025e-109">The modified source rectangle is half the original height and width and is centered in the original frame.</span></span> <span data-ttu-id="d025e-110">La llamada a la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) vuelve a definir las coordenadas del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="d025e-110">The call to the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro redefines the coordinates of the source rectangle.</span></span>


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




