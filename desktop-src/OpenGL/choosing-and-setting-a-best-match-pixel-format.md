---
title: Elegir y establecer un formato Best-Match píxeles
description: En este tema se explica el procedimiento para hacer coincidir un contexto de dispositivo con un formato de píxel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL en Windows,píxeles
- formato de píxel de coincidencia más adecuado de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161133"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>Elegir y establecer un formato Best-Match píxeles

En este tema se explica el procedimiento para hacer coincidir un contexto de dispositivo con un formato de píxel.

**Para obtener la mejor coincidencia de un contexto de dispositivo con un formato de píxel**

1.  Especifique el formato de píxel deseado en una [**estructura PIXELFORMATDESCRIPTOR.**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
2.  Llame [**a ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)

    La **función ChoosePixelFormat** devuelve un índice de formato de píxel, que luego puede pasar a [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) para establecer la mejor coincidencia de formato de píxel como formato de píxel actual del contexto del dispositivo.

En el ejemplo de código siguiente se muestra cómo llevar a cabo los pasos anteriores.


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




