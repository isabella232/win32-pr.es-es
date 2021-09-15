---
title: Examinar formatos de píxeles compatibles con dispositivos
description: La función DescribePixelFormat obtiene datos de formato de píxel para un contexto de dispositivo.
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- OpenGL en Windows,píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee45212111354d79b7a23fd35490a08f0aead4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473680"
---
# <a name="examining-a-devices-supported-pixel-formats"></a>Examinar formatos de píxeles compatibles con dispositivos

La [**función DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) obtiene datos de formato de píxel para un contexto de dispositivo. También devuelve un entero que es el índice de formato de píxel máximo para el contexto del dispositivo. En el ejemplo de código siguiente se muestra cómo usar ese resultado para examinar los formatos de píxel admitidos por un dispositivo:


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



 

 




