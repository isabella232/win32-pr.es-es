---
title: Dibujar con búferes dobles
description: Los búferes dobles suavizan la transición entre una imagen y otra en la pantalla.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL en Windows, búferes dobles
- búferes dobles OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357620"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="feeb3-105">Dibujar con búferes dobles</span><span class="sxs-lookup"><span data-stu-id="feeb3-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="feeb3-106">Los búferes dobles suavizan la transición entre una imagen y otra en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="feeb3-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="feeb3-107">Normalmente, los búferes de intercambio se incluyen al final de una secuencia de comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="feeb3-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="feeb3-108">De forma predeterminada, la implementación de Microsoft de OpenGL en Windows dibuja en el búfer fuera de pantalla; una vez finalizado el dibujo, se llama a la función [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) para copiar el búfer de la pantalla en el búfer en pantalla.</span><span class="sxs-lookup"><span data-stu-id="feeb3-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="feeb3-109">El siguiente ejemplo de código se prepara para dibujar, llama a una función de dibujo y, a continuación, copia la imagen completada en la pantalla si el almacenamiento en búfer doble está disponible.</span><span class="sxs-lookup"><span data-stu-id="feeb3-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


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



<span data-ttu-id="feeb3-110">En el ejemplo de código siguiente se obtiene un contexto de dispositivo de ventana, se representa una escena, se copia la imagen en la pantalla (para mostrar la representación) y, a continuación, se libera el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="feeb3-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




