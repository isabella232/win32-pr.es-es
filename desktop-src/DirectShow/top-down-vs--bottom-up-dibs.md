---
description: Top-Down frente a
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down frente a Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667646"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down frente a Bottom-Up DIB

Si no está familiarizado con la programación de gráficos, puede esperar que un mapa de bits se organice en memoria para que la fila superior de la imagen aparezca al principio del búfer, seguida de la siguiente fila, etc. Sin embargo, esto no es necesariamente así. En Windows, los mapas de bits independientes del dispositivo (DIB) se pueden colocar en memoria en dos orientaciones diferentes, de arriba abajo y de arriba abajo.

En un DIB de abajo arriba, el búfer de la imagen comienza con la fila inferior de píxeles, seguida de la siguiente fila, etc. La fila superior de la imagen es la última fila del búfer. Por lo tanto, el primer byte de la memoria es el píxel inferior izquierdo de la imagen. En GDI, todos los DIB están en orden ascendente. En el diagrama siguiente se muestra el diseño físico de un DIB de arriba abajo.

![DIB de abajo arriba](images/pixel-layout-bottomup.png)

En un DIB de arriba abajo, se invierte el orden de las filas. La fila superior de la imagen es la primera fila de la memoria, seguida de la fila siguiente. La fila inferior de la imagen es la última fila del búfer. Con un DIB de arriba abajo, el primer byte de la memoria es el píxel superior izquierdo de la imagen. DirectDraw usa DIB de arriba abajo. En el diagrama siguiente se muestra el diseño físico de un DIB de arriba abajo:

![DIB de arriba abajo](images/pixel-layout-topdown.png)

En el caso de los DIB RGB, la orientación de la imagen se indica mediante el miembro **biheight** de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Si **biheight** es positivo, la imagen estará en orden ascendente. Si el valor de **biheight** es negativo, la imagen es de arriba abajo.

Los DIB en formatos YUV siempre son de arriba abajo y se omite el signo del miembro de **bialtura** . Los descodificadores deben ofrecer formatos YUV con un **bialto** positivo, pero también deben aceptar formatos YUV con una **bialtura** negativa y omitir el signo.

Además, cualquier tipo DIB que use un **FourCC** en el miembro de **bicompression** debe expresar su **biheight** como un número positivo, independientemente de cuál sea su orientación, ya que el propio elemento **FourCC** identifica un esquema de compresión cuya orientación de imagen debe entenderse con cualquier filtro compatible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 



