---
description: Un mapa de bits independiente del dispositivo (DIB) contiene una tabla de colores.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569220"
---
# <a name="device-independent-bitmaps"></a>Device-Independent mapa de bits

Un mapa de bits independiente del dispositivo (DIB) contiene una *tabla de colores*. Una tabla de colores describe cómo se corresponden los valores de píxel con los valores de color *RGB,* que describen los colores que se generan mediante la emisión de luz. Por lo tanto, una DIB puede lograr la combinación de colores adecuada en cualquier dispositivo. Una DIB contiene la siguiente información de color y dimensión:

-   Formato de color del dispositivo en el que se creó la imagen rectangular.
-   Resolución del dispositivo en el que se creó la imagen rectangular.
-   Paleta del dispositivo en el que se creó la imagen.
-   Matriz de bits que asigna triplets rojo, verde, azul [**(RGB)**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) a píxeles en la imagen rectangular.
-   Identificador de compresión de datos que indica el esquema de compresión de datos (si hay alguno) usado para reducir el tamaño de la matriz de bits.

La información de color y dimensión se almacena en una estructura [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que consta de una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) seguida de dos o más estructuras [**RGBQUAD.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) La **estructura BITMAPINFOHEADER** especifica las dimensiones del rectángulo de píxeles, describe la tecnología de color del dispositivo e identifica los esquemas de compresión utilizados para reducir el tamaño del mapa de bits. Las **estructuras RGBQUAD** identifican los colores que aparecen en el rectángulo de píxeles.

Hay dos variedades de DIB:

-   DIB de abajo arriba, en el que el origen se encuentra en la esquina inferior izquierda.
-   DIB de arriba abajo, en el que el origen se encuentra en la esquina superior izquierda.

Si el alto de una DIB, como indica el miembro **Height** de la estructura de encabezado de información de mapa de bits, es un valor positivo, es una DIB de abajo hacia arriba; si el alto es un valor negativo, es una DIB de arriba abajo. Las DIB de arriba abajo no se pueden comprimir.

El formato de color se especifica en términos de un recuento de planos de color y bits de color. El recuento de planos de color siempre es 1; el recuento de bits de color es 1 para mapas de bits monocromáticos, 4 para mapas de bits VGA y 8, 16, 24 o 32 para mapas de bits en otros dispositivos de color. Una aplicación recupera el número de bits de color que usa una pantalla (o impresora) determinada llamando a la función [**GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) especificando BITSPIXEL como segundo argumento.

La resolución de un dispositivo de pantalla se especifica en píxeles por medidor. Una aplicación puede recuperar la resolución horizontal de una pantalla de vídeo o impresora siguiendo este proceso de tres pasos.

1.  Llame a [**la función GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique HORZRES como segundo argumento.
2.  Llame [**a GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) una segunda vez y especifique HORZSIZE como segundo argumento.
3.  Divida el primer valor devuelto por el segundo valor devuelto.

La aplicación puede recuperar la resolución vertical mediante el mismo proceso de tres pasos con parámetros diferentes: VERTRES en lugar de HORZRES y VERTSIZE en lugar de HORZSIZE.

La paleta se representa mediante una matriz de estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que especifican los componentes de intensidad rojo, verde y azul para cada color de la paleta de colores de un dispositivo de visualización. Cada índice de color de la matriz de paleta se asigna a un píxel específico de la región rectangular asociada al mapa de bits. El tamaño de esta matriz, en bits, es equivalente al ancho del rectángulo, en píxeles, multiplicado por el alto del rectángulo, en píxeles, multiplicado por el recuento de bits de color para el dispositivo. Una aplicación puede recuperar el tamaño de la paleta del dispositivo llamando a la función [**GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) especificando NUMCOLORS como segundo argumento.

Windows admite la compresión de la matriz de paleta para dibs de abajo arriba de 8 bpp y 4 bpp. Estas matrices se pueden comprimir mediante el esquema de codificación de longitud de ejecución (RLE). El esquema RLE usa valores de 2 bytes, el primer byte especifica el número de píxeles consecutivos que usan un índice de color y el segundo byte que especifica el índice. Para obtener más información sobre la compresión de mapa de bits, vea la descripción de las estructuras [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)y [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Una aplicación puede crear una DIB a partir de una DDB inicializando las estructuras necesarias y llamando a la [**función GetDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) Para determinar si un dispositivo admite esta función, llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique RC DI BITMAP como \_ \_ marca RASTERCAPS.

Una aplicación que necesita copiar un mapa de bits puede usar [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) para copiar todos los píxeles de un mapa de bits de origen en un mapa de bits de destino, excepto los píxeles que coinciden con el color transparente.

Una aplicación puede usar un DIB para establecer píxeles en el dispositivo de presentación mediante una llamada a [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) o a [**la función StretchDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) Para determinar si un dispositivo admite la función **SetDIBitsToDevice,** llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique RC DIBTODEV como marca \_ RASTERCAPS. Especifique RC \_ STRETCHDIB como marca RASTERCAPS para determinar si el dispositivo admite **StretchDIBits.**

Una aplicación que simplemente necesita mostrar una DIB existente puede usar la [**función SetDIBitsToDevice.**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) Por ejemplo, una aplicación de hoja de cálculo puede abrir gráficos existentes y mostrarlos en una ventana mediante la **función SetDIBitsToDevice.** Sin embargo, para volver a dibujar repetidamente un mapa de bits en una ventana, la aplicación debe usar la [**función BitBlt.**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) Por ejemplo, una aplicación multimedia que combina gráficos animados con sonido se beneficiaría de llamar a la función **BitBlt** porque se ejecuta más rápido que **SetDIBitsToDevice**.

 

 
