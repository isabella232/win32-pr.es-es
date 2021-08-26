---
title: Ejemplo de código de contexto de representación de GLX
description: En el ejemplo de código siguiente se muestra cómo un programa OpenGL del sistema de ventanas X usa funciones de contexto de representación glx.
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- representar contextos
- porte a OpenGL, representación de contextos
- Porte de OpenGL, representación de contextos
- Sistema de ventanas X, contextos de representación
- Funciones GLX, contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15ef1c1e1eddba86da56f8036adfa0724d8c997ba5f4c262f3d14446e86441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035275"
---
# <a name="glx-rendering-context-code-sample"></a>Ejemplo de código de contexto de representación de GLX

En el ejemplo de código siguiente se muestra cómo un programa OpenGL del sistema de ventanas X usa funciones de contexto de representación glx.


```C++
Display *dpy;             /* display variable */ 
XVisualInfo *vi;          /* visual variable */ 
Window win;               /* window variable */ 
GLXDrawable drawable;     /* drawable variable */ 
GLXContext cx, cxTemp;    /* rendering context variables */ 
 
/* Code to open a display and get a visual. */ 
        
/* Create a GLX context. */ 
cx = glXCreateContext(dpy, vi, 0, GL_FALSE); 
if (!cx) { 
    fprintf(stderr, "Cannot create context.\n"); 
    exit(-1); 
} 
        
        .    
/* Connect the context to the window. */ 
glXMakeCurrent(dpy, win, cx); 
        
        .    
/* When it's time to destroy the rendering context. . . */ 
cx = glXGetCurrentContext; 
glXDestroyContext(dpy, cx);
```



 

 




