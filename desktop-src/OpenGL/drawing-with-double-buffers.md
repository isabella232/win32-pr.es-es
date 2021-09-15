---
title: Dibujo con búferes dobles
description: Los búferes dobles suavizan la transición entre una imagen y otra en la pantalla.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL en Windows, búferes dobles
- double buffers OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473690"
---
# <a name="drawing-with-double-buffers"></a>Dibujo con búferes dobles

Los búferes dobles suavizan la transición entre una imagen y otra en la pantalla. El intercambio de búferes normalmente se produce al final de una secuencia de comandos de dibujo. De forma predeterminada, la implementación de Microsoft de OpenGL Windows dibuja en el búfer fuera de la pantalla; Una vez completado el dibujo, se llama a la [**función SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) para copiar el búfer fuera de pantalla en el búfer en pantalla. El ejemplo de código siguiente se prepara para dibujar, llama a una función de dibujo y, a continuación, copia la imagen completa en la pantalla si el almacenamiento en búfer doble está disponible.


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



El ejemplo de código siguiente obtiene un contexto de dispositivo de ventana, representa una escena, copia la imagen en la pantalla (para mostrar la representación) y, a continuación, libera el contexto del dispositivo.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




