---
title: Examinar los formatos de píxeles compatibles con los dispositivos
description: La función DescribePixelFormat obtiene los datos de formato de píxel para un contexto de dispositivo.
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- OpenGL en Windows, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee45212111354d79b7a23fd35490a08f0aead4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419026"
---
# <a name="examining-a-devices-supported-pixel-formats"></a><span data-ttu-id="84fb2-104">Examinar los formatos de píxeles compatibles con los dispositivos</span><span class="sxs-lookup"><span data-stu-id="84fb2-104">Examining a Devices Supported Pixel Formats</span></span>

<span data-ttu-id="84fb2-105">La función [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) obtiene los datos de formato de píxel para un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84fb2-105">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function obtains pixel format data for a device context.</span></span> <span data-ttu-id="84fb2-106">También devuelve un entero que es el índice de formato de píxel máximo para el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84fb2-106">It also returns an integer that is the maximum pixel format index for the device context.</span></span> <span data-ttu-id="84fb2-107">En el ejemplo de código siguiente se muestra cómo usar ese resultado para recorrer y examinar los formatos de píxel admitidos por un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="84fb2-107">The following code sample shows how to use that result to step through and examine the pixel formats supported by a device:</span></span>


```C++
// local variables  
int                      iMax ; 
PIXELFORMATDESCRIPTOR    pfd; 
int                      iPixelFormat ; 
 
// initialize a pixel format index variable  
iPixelFormat = 1; 
 
// keep obtaining and examining pixel format data...  
do { 
    // try to obtain some pixel format data  
    iMax = DescribePixelFormat(hdc, iPixelFormat, sizeof(pfd), &pfd); 
 
    // if there was some problem with that...   
    if (iMax == 0) 
     
        // return indicating failure  
        return(FALSE); 
     
    // we have successfully obtained pixel format data  
 
    // let's examine the pixel format data...  
    myPixelFormatExaminer (&pfd); 
    }  
 
// ...until we've looked at all the device context's pixel formats  
while (++iPixelFormat <= iMax);
```



 

 




