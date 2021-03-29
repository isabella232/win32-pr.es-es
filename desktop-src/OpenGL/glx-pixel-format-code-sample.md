---
title: GLX ejemplo de código de formato de píxeles
description: En el ejemplo de código siguiente se muestra cómo un programa OpenGL de sistema de ventana X usa funciones de formato visual/píxel de GLX.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- trasladar a OpenGL, píxeles
- Portabilidad de OpenGL, píxeles
- Sistema X ventana, píxeles
- GLX funciones, píxeles
- pixels, ejemplo GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0ab6464d54e696c136a6c987b94124f52b0ee2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773351"
---
# <a name="glx-pixel-format-code-sample"></a><span data-ttu-id="d8d38-108">GLX ejemplo de código de formato de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8d38-108">GLX Pixel Format Code Sample</span></span>

<span data-ttu-id="d8d38-109">En el ejemplo de código siguiente se muestra cómo un programa OpenGL de sistema de ventana X usa funciones de formato visual/píxel de GLX.</span><span class="sxs-lookup"><span data-stu-id="d8d38-109">The code sample below shows how an X Window System OpenGL program uses GLX visual/pixel formatting functions.</span></span>


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



<span data-ttu-id="d8d38-110">El visual se puede usar para crear una ventana y un contexto de representación.</span><span class="sxs-lookup"><span data-stu-id="d8d38-110">The Visual can be used to create a window and a rendering context.</span></span>

 

 




