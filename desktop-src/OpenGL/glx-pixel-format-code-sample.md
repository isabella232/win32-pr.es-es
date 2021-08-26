---
title: Ejemplo de código de formato de píxel GLX
description: En el ejemplo de código siguiente se muestra cómo un programa OpenGL del sistema de ventanas X usa funciones de formato visual/píxel de GLX.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- porting to OpenGL,pixels
- Porte de OpenGL, píxeles
- X Window System,pixels
- Funciones GLX, píxeles
- píxeles, ejemplo GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035395"
---
# <a name="glx-pixel-format-code-sample"></a>Ejemplo de código de formato de píxel GLX

En el ejemplo de código siguiente se muestra cómo un programa OpenGL del sistema de ventanas X usa funciones de formato visual/píxel de GLX.


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



El objeto visual se puede usar para crear una ventana y un contexto de representación.

 

 




