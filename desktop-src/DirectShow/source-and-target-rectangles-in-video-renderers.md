---
description: Rectángulos de origen y destino en representadores de vídeo
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Rectángulos de origen y destino en representadores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275156"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Rectángulos de origen y destino en representadores de vídeo

Hay tres tamaños que se encuentran en las estructuras de formato [**VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)y [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) de tipos de medios de vídeo. En este artículo se explica qué son y cómo funcionan.

En primer lugar, hay un tamaño en el **miembro bmiHeader** de estas estructuras. El **miembro bmiHeader** es una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) con sus propios miembros de ancho y alto, **bmiHeader.biWidth** **y bmiHeader.biHeight.**

En segundo lugar, hay un rectángulo en el **miembro rcSource** de estas estructuras; y, por último, hay un rectángulo en el **miembro rcTarget** de estas estructuras.

Suponga que tiene dos filtros, A y B, y que estos filtros están conectados entre sí (A a la izquierda, o ascendente, y B a la derecha o descendente) con un determinado tipo de medio de vídeo.

Los búferes que pasan entre los filtros A y B tienen el tamaño (**bmiHeader.biWidth**, **bmiHeader.biHeight**). El filtro A debe tomar una parte de su vídeo de entrada determinado por **rcSource** y extender ese vídeo para rellenar **la parte rcTarget** del búfer. La parte del vídeo de entrada que se va a usar se basa en cómo **rcSource** se compara con el tamaño **(biWidth**, **biHeight)** del tipo de medio con el que se filtran A y B conectados originalmente. Si **rcSource** está vacío, el filtro A usa todo su vídeo de entrada. Si **rcTarget** está vacío, el filtro A rellena todo el búfer de salida.

Por ejemplo, suponga que el filtro A recibe datos de vídeo de 160 x 120 píxeles. Supongamos también que el filtro A está conectado al filtro B con el siguiente tipo de medio.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget:**(0, 0, 0, 0)

Esto significa que el filtro A extenderá el vídeo que recibe en 2 en las direcciones x e y, y rellenará un búfer de salida de 320 x 240.

Como otro ejemplo, suponga que el filtro A recibe datos de vídeo de 160 x 120 y que está conectado al filtro B con el siguiente tipo de medio.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget:**(0, 0, 0, 0)

El **miembro rcSource** es relativo al tamaño de búfer conectado de 320, 240. Dado que el **rcSource especificado** (0, 0, 160, 240) es la mitad izquierda del búfer, el filtro A tomará la mitad izquierda del vídeo de entrada o la parte (0, 0, 80, 120) y extenderá el vídeo a un tamaño de (320, 240) (por 4 en la dirección x y 2 en la dirección y) y rellenar el búfer de salida de 320 x 240.

Ahora suponga que el filtro A llama a [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md)y el ejemplo de medio devuelto tiene un tipo de medio asociado, lo que significa que el filtro B quiere filtrar A para proporcionar un tamaño o tipo de vídeo diferente al que se ha estado proporcionando anteriormente. Supongamos que el nuevo tipo de medio es:

-   (**biWidth**, **biHeight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget:**(0, 0, 80, 60)

Esto significa que el ejemplo multimedia tiene un búfer de 640 x 480 de tamaño. El **miembro rcSource** es relativo al tipo de medio conectado original (320, 240) no al nuevo tipo de medio de (640, 480), por lo que **rcSource** especifica que se usará la esquina superior izquierda (25 %) del vídeo de entrada. Esta parte del vídeo de entrada se coloca en los píxeles superior izquierdo (80, 60) del búfer de salida de 640 x 480, tal y como especifica **rcTarget** de (0, 0, 80, 60). Dado que el filtro A recibe vídeo de 160 x 120, la esquina superior izquierda del vídeo de entrada es una pieza (80, 60), el mismo tamaño del mapa de bits de salida y no se requiere ningún stretching.

El filtro A no colocará datos en los otros píxeles del búfer de salida y dejará esos bits intactos. El **miembro rcSource** está enlazado por biWidth y **biHeight** del tipo de medio conectado original entre los filtros A y B, y **rcTarget** está limitado por el nuevo **biWidth** y **biHeight** del ejemplo multimedia.  En el ejemplo anterior, **rcSource** no podía salir de los límites de (0, 0, 320, 240) y **rcTarget** no podía salir de los límites de (0, 0, 640, 480).

 

 



