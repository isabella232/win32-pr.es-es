---
description: Rectángulos de origen y de destino en representadores de vídeo
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Rectángulos de origen y de destino en representadores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537557"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Rectángulos de origen y de destino en representadores de vídeo

Existen tres tamaños en las estructuras de formato [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)y [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) de los tipos de medios de vídeo. En este artículo se explica lo que son y cómo funcionan.

En primer lugar, hay un tamaño en el miembro **bmiHeader** de estas estructuras. El miembro **bmiHeader** es una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) con sus propios miembros de ancho y alto, **BmiHeader. biwidth** y **bmiHeader. biheight**.

En segundo lugar, hay un rectángulo en el miembro **rcSource** de estas estructuras; y por último, hay un rectángulo en el miembro **rcTarget** de estas estructuras.

Suponga que tiene dos filtros, A y B, y que estos filtros están conectados entre sí (a a la izquierda, o ascendente y B a la derecha o descendente) con un determinado tipo de medio de vídeo.

Los búferes que pasan entre los filtros A y B tienen el tamaño (**bmiHeader. biwidth**, **BmiHeader. biheight**). El filtro A debe tomar una parte de su vídeo de entrada determinado por **rcSource** y ajustar el vídeo para rellenar la parte **rcTarget** del búfer. La parte del vídeo de entrada que se va a usar se basa en el modo en que **rcSource** se compara con el tamaño (**biwidth**, **biheight**) del tipo de medio que filtra a y B conectado originalmente con. Si **rcSource** está vacío, el filtro A usa todo el vídeo de entrada. Si **rcTarget** está vacío, el filtro A llena todo el búfer de salida.

Por ejemplo, suponga que el filtro A está recibiendo datos de vídeo de 160 x 120 píxeles. Supongamos también que el filtro a está conectado al filtro B con el siguiente tipo de medio.

-   (**biwidth**, **biheight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget**: (0, 0, 0, 0)

Esto significa que el filtro A ajustará el vídeo que recibe en 2 en las direcciones x e y, y rellenará un búfer de salida 320 x 240.

Como otro ejemplo, suponga que el filtro A está recibiendo datos de vídeo 160 x 120 y que está conectado al filtro B con el siguiente tipo de medio.

-   (**biwidth**, **biheight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget**: (0, 0, 0, 0)

El miembro **rcSource** es relativo al tamaño del búfer conectado de 320, 240. Dado que el valor de **rcSource** especificado (0, 0, 160, 240) es la mitad izquierda del búfer, el filtro A tomará la mitad izquierda de su vídeo de entrada o la parte (0, 0, 80, 120) y extenderá el vídeo a un tamaño de (320, 240) (en 4 en la dirección x y 2 en la dirección y) y rellenando el búfer de salida 320 x 240.

Ahora Supongamos que el filtro A llama a [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md)y que el ejemplo multimedia devuelto tiene un tipo de archivo multimedia adjunto, lo que significa que el filtro B desea que el filtro a proporcione un tamaño o tipo de vídeo diferente del que ha proporcionado anteriormente. Supongamos que el nuevo tipo de medio es:

-   (**biwidth**, **biheight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget**: (0, 0, 80, 60)

Esto significa que el ejemplo multimedia tiene un búfer con un tamaño de 640 x 480. El miembro **rcSource** es relativo al tipo de medio conectado original (320, 240) al nuevo tipo de medio (640, 480), por lo que **rcSource** especifica que la esquina superior izquierda (25%) del vídeo de entrada que se va a usar. Esta parte del vídeo de entrada se coloca en los píxeles superior izquierdo (80, 60) del búfer de salida 640 x 480, según se especifica en **rcTarget** de (0, 0, 80, 60). Dado que el filtro A recibe el vídeo 160 x 120, la esquina superior izquierda del vídeo de entrada es una pieza (80, 60), el mismo tamaño del mapa de bits de salida y no se requiere ninguna ampliación.

El filtro A no colocará ningún dato en los demás píxeles del búfer de salida y dejará esos bits intactos. El miembro **rcSource** está limitado por el **ancho** y el **bialto** del tipo de medio conectado original entre los filtros A y B, y **RcTarget** está limitado por el nuevo **biwidth** y el **alto** de la muestra multimedia. En el ejemplo anterior, **rcSource** no pudo superar los límites de (0, 0, 320, 240) y **rcTarget** no pudo superar los límites de (0,0, 640, 480).

 

 



