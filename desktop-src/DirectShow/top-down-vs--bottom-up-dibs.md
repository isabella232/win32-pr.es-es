---
description: Top-Down frente a
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down frente a Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff1d525423ef8590a3656a5e63f7541be180e2dcc5c70307f93298eb9ce991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951577"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down frente a Bottom-Up DIB

Si no está de acuerdo con la programación de gráficos, puede esperar que un mapa de bits se organizará en memoria para que la fila superior de la imagen apareciera al principio del búfer, seguida de la fila siguiente, etc. Sin embargo, este no es necesariamente el caso. En Windows, los mapas de bits independientes del dispositivo (DIB) se pueden colocar en la memoria en dos orientaciones diferentes, de abajo arriba y de arriba abajo.

En una DIB de abajo hacia arriba, el búfer de imagen comienza con la fila inferior de píxeles, seguida de la siguiente fila hacia arriba, etc. La fila superior de la imagen es la última fila del búfer. Por lo tanto, el primer byte de la memoria es el píxel inferior izquierdo de la imagen. En GDI, todas las DIB están de abajo hacia arriba. En el diagrama siguiente se muestra el diseño físico de una DIB de abajo hacia arriba.

![dib de abajo hacia arriba](images/pixel-layout-bottomup.png)

En una DIB de arriba abajo, se invierte el orden de las filas. La fila superior de la imagen es la primera fila en memoria, seguida de la siguiente fila hacia abajo. La fila inferior de la imagen es la última fila del búfer. Con una DIB de arriba abajo, el primer byte de la memoria es el píxel superior izquierdo de la imagen. DirectDraw usa DIB de arriba a abajo. En el diagrama siguiente se muestra el diseño físico de una DIB de arriba a abajo:

![dib de arriba a abajo](images/pixel-layout-topdown.png)

Para las DIB RGB, la orientación de la imagen se indica mediante el **miembro biHeight** de la [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Si **biHeight es** positivo, la imagen está de abajo hacia arriba. Si **biHeight es** negativo, la imagen está de arriba abajo.

Las DIB en formatos YUV siempre están de arriba abajo y se omite el signo del **miembro biHeight.** Los descodificadores deben ofrecer formatos YUV con **biHeight** positivo, pero también deben aceptar formatos YUV con **biHeight** negativo y omitir el signo.

Además, cualquier tipo DIB que use **un FOURCC** en el miembro **biCompression** debe expresar **su valor biHeight** como un número positivo independientemente de cuál sea su orientación, ya que **el propio FOURCC** identifica un esquema de compresión cuya orientación de imagen debe entenderse mediante cualquier filtro compatible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con fotogramas de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 



