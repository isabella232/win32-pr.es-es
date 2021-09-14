---
title: Eliminación de un contexto de representación
description: En el ejemplo de código siguiente se muestra cómo eliminar un contexto de representación de OpenGL cuando se cierra una ventana de OpenGL. Es una continuación del escenario utilizado en Crear un contexto de representación y Hacer que sea actual.
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621abd0de46c874f40568f8361191b25df329f0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260279"
---
# <a name="deleting-a-rendering-context"></a>Eliminación de un contexto de representación

En el ejemplo de código siguiente se muestra cómo eliminar un contexto de representación de OpenGL cuando se cierra una ventana de OpenGL. Es una continuación del escenario utilizado en Crear [un contexto de representación y Hacer que sea actual.](creating-a-rendering-context-and-making-it-current.md)


```C++
// a window is about to be destroyed  
case WM_DESTROY: 
    { 
    // local variables  
    HGLRC    hglrc; 
    HDC      hdc ; 
 
    // if the thread has a current rendering context ...  
    if(hglrc = wglGetCurrentContext()) { 
 
        // obtain its associated device context  
        hdc = wglGetCurrentDC() ; 
 
        // make the rendering context not current  
        wglMakeCurrent(NULL, NULL) ; 
 
        // release the device context  
        ReleaseDC (hwnd, hdc) ; 
 
        // delete the rendering context  
        wglDeleteContext(hglrc); 
 
        }
```



 

 




