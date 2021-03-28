---
description: Un mapa de bits independiente del dispositivo (DIB) contiene una tabla de colores.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Mapas de bits Device-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155645"
---
# <a name="device-independent-bitmaps"></a>Mapas de bits Device-Independent

Un mapa de bits independiente del dispositivo (DIB) contiene una *tabla de colores*. Una tabla de colores describe cómo se corresponden los valores de píxeles con los valores de color *RGB* , que describen los colores que se producen al emitir la luz. Por lo tanto, un DIB puede lograr la combinación de colores adecuada en cualquier dispositivo. Un DIB contiene la siguiente información sobre el color y la dimensión:

-   El formato de color del dispositivo en el que se creó la imagen rectangular.
-   La resolución del dispositivo en el que se creó la imagen rectangular.
-   Paleta del dispositivo en el que se creó la imagen.
-   Matriz de bits que asigna los triples rojo, verde y azul ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) a los píxeles de la imagen rectangular.
-   Identificador de compresión de datos que indica el esquema de compresión de datos (si existe) que se usa para reducir el tamaño de la matriz de bits.

La información de color y dimensión se almacena en una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , que consta de una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) seguida de dos o más estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . La estructura **BITMAPINFOHEADER** especifica las dimensiones del rectángulo de píxeles, describe la tecnología de color del dispositivo e identifica los esquemas de compresión usados para reducir el tamaño del mapa de bits. Las estructuras **RGBQUAD** identifican los colores que aparecen en el rectángulo de píxeles.

Hay dos tipos de DIB:

-   Un DIB de nivel inferior, en el que el origen se encuentra en la esquina inferior izquierda.
-   Un DIB de arriba abajo, en el que el origen se encuentra en la esquina superior izquierda.

Si el alto de un DIB, como indica el miembro **height** de la estructura del encabezado de información de mapa de bits, es un valor positivo, se trata de un DIB ascendente; Si el alto es un valor negativo, es un DIB de arriba abajo. Los DIB de arriba abajo no se pueden comprimir.

El formato de color se especifica en términos de recuento de planos de color y bits de color. El recuento de planos de color siempre es 1; el recuento de bits de color es 1 para los mapas de bits monocromáticos, 4 para los mapas de bits VGA y 8, 16, 24 o 32 para los mapas de bits en otros dispositivos de color. Una aplicación recupera el número de bits de color que usa una determinada pantalla (o impresora) mediante una llamada a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando BITSPIXEL como segundo argumento.

La resolución de un dispositivo de pantalla se especifica en píxeles por metro. Una aplicación puede recuperar la resolución horizontal de una pantalla de vídeo, o impresora, siguiendo este proceso de tres pasos.

1.  Llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando HORZRES como segundo argumento.
2.  Llame a [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) una segunda vez, especificando HORZSIZE como segundo argumento.
3.  Divide el primer valor devuelto por el segundo valor devuelto.

La aplicación puede recuperar la resolución vertical mediante el mismo proceso de tres pasos con distintos parámetros: VERTRES en lugar de HORZRES y VERTSIZE en lugar de HORZSIZE.

La paleta está representada por una matriz de estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que especifican los componentes de intensidad rojo, verde y azul para cada color de la paleta de colores de un dispositivo de pantalla. Cada índice de color de la matriz de la paleta se asigna a un píxel específico de la región rectangular asociada al mapa de bits. El tamaño de esta matriz, en bits, es equivalente al ancho del rectángulo, en píxeles, multiplicado por el alto del rectángulo, en píxeles, multiplicado por el número de bits de color para el dispositivo. Una aplicación puede recuperar el tamaño de la paleta del dispositivo llamando a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especificando NUMCOLORS como segundo argumento.

Windows admite la compresión de la matriz de paleta para los DIB de preorden de 8 y 4 BPP. Estas matrices se pueden comprimir mediante el esquema de codificación de longitud de ejecución (RLE). El esquema RLE utiliza valores de 2 bytes, el primer byte que especifica el número de píxeles consecutivos que usan un índice de color y el segundo byte que especifica el índice. Para obtener más información sobre la compresión de mapas de bits, vea la descripción de las estructuras [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)y [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .

Una aplicación puede crear un DIB a partir de un DDB Inicializando las estructuras necesarias y llamando a la función [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) . Para determinar si un dispositivo admite esta función, llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y especifique RC \_ di \_ Bitmap como la marca RASTERCAPS.

Una aplicación que necesita copiar un mapa de bits puede usar [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) para copiar todos los píxeles de un mapa de bits de origen en un mapa de bits de destino, excepto los píxeles que coinciden con el color transparente.

Una aplicación puede usar un DIB para establecer píxeles en el dispositivo de pantalla mediante una llamada a la función [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) . Para determinar si un dispositivo admite la función **SetDIBitsToDevice** , llame a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando RC \_ DIBTODEV como marca RASTERCAPS. Especifique RC \_ STRETCHDIB como la marca RASTERCAPS para determinar si el dispositivo admite **StretchDIBits**.

Una aplicación que simplemente necesita mostrar un DIB existente previamente puede usar la función [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) . Por ejemplo, una aplicación de hoja de cálculo puede abrir los gráficos existentes y mostrarlos en una ventana mediante la función **SetDIBitsToDevice** . Sin embargo, para volver a dibujar repetidamente un mapa de bits en una ventana, la aplicación debe utilizar la función [**bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) . Por ejemplo, una aplicación multimedia que combina gráficos animados con sonido se beneficiaría de la llamada a la función **bitblt** porque se ejecuta más rápido que **SetDIBitsToDevice**.

 

 
