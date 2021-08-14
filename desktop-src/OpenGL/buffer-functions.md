---
title: Funciones de búfer
description: Para copiar el contenido de un búfer fuera de pantalla en un búfer en pantalla, llame a SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funciones WGL,buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618605"
---
# <a name="buffer-functions"></a>Funciones de búfer

Para copiar el contenido de un búfer fuera de pantalla en un búfer en pantalla, llame a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). La **función SwapBuffers** toma un identificador para un contexto de dispositivo. El formato de píxel actual para el contexto de dispositivo especificado debe incluir un búfer de reserva. De forma predeterminada, el búfer de reserva está fuera de la pantalla y el búfer frontal está en pantalla.

> [!Note]  
> La **función SwapBuffers** no intercambia realmente el contenido de los dos búferes, sino que copia el contenido de un búfer a otro. El contenido del búfer fuera de pantalla no está definido después de una llamada a **SwapBuffers**. Por lo tanto, el resultado de dos llamadas **consecutivas a SwapBuffers** es indefinido.

 

En la ilustración siguiente se muestra cómo se copia el contenido de los búferes al llamar a **SwapBuffers**.

![Diagrama que muestra los resultados no definidos de las llamadas consecutivas a la función SwapBuffers.](images/opengl00.png)

Varias funciones principales de OpenGL también administran búferes. La [**función glDrawBuffer**](gldrawbuffer.md) es la más relevante para el almacenamiento en búfer doble; especifica el búfer de fotogramas o búferes en los que se dibuja OpenGL.

Las siguientes funciones también afectan a los búferes:

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 




