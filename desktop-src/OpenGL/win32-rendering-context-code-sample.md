---
title: Windows Ejemplo de código de contexto de representación
description: En el ejemplo de código siguiente se muestra el aspecto del código contextual de representación de GLX en la sección anterior cuando se ha portado a Windows.
ms.assetid: 12992faa-eb64-4a21-8015-3c73c2914189
keywords:
- representar contextos
- porte a OpenGL, representación de contextos
- Porte de OpenGL, representación de contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0423f7458538f903a339f2f82dbff1c86c0626
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073965"
---
# <a name="windows-rendering-context-code-sample"></a>Windows Ejemplo de código de contexto de representación

En el ejemplo de código siguiente se muestra el aspecto del código contextual de representación de GLX en la sección anterior cuando se ha portado a Windows.


```C++
HGLRC hRC;           // rendering context variable  
 
/* Create and initialize a window */ 
        
/* Window message switch in a window procedure */ 
case WM_CREATE:      // Message when window is created  
{ 
    HDC hDC, hDCTemp;    // device context handles   
 
    /* Get the handle of the windows device context. */ 
    hDC = GetDC(hWnd); 
 
    /* Create a rendering context and make it the current context */  
    hRC = wglCreateContext(hDC); 
    if (!hRC)  
    { 
        MessageBox(NULL, "Cannot create context.", "Error", MB_OK); 
        return FALSE; 
    }  
    wglMakeCurrent(hDC, hRC); 
} 
break; 
        
        .    
case WM_DESTROYED:   // Message when window is destroyed  
{ 
    HGLRC hRC        // rendering context handle  
    HDC   hDC;       // device context handle  
 
    /* Release and free the device context and rendering context. */ 
    hDC = wglGetCurrentDC; 
    hRC = wglGetCurrentContext; 
 
    wglMakeCurrent(NULL, NULL); 
 
    if (hRC) 
        wglDeleteContext(hRC); 
 
    if (hDC) 
        ReleaseDC(hWnd, hDC); 
 
    PostQuitMessage (0); 
} 
break;
```



 

 




