---
title: Examinar el formato de píxel actual de los contextos de dispositivo
description: Use las funciones GetPixelFormat y DescribePixelFormat para examinar el formato de píxel actual de un contexto de dispositivo, como se muestra en el fragmento de código siguiente.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL en Windows,píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea36f0f25b2cf76a6fb2ffb3159a4f2763a95af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473681"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Examinar el formato de píxel actual de los contextos de dispositivo

Use las [**funciones GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) y [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) para examinar el formato de píxel actual de un contexto de dispositivo, como se muestra en el fragmento de código siguiente.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




