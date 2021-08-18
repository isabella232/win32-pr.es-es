---
description: Los mapas de bits deben guardarse en un archivo que use el formato de archivo de mapa de bits establecido y asignar un nombre con la extensión de .bmp caracteres.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Mapa de bits Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83688f240899ded49227264b716d8c5d1fb609aa747fc358184a78ad18c8d17f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038213"
---
# <a name="bitmap-storage"></a>Mapa de bits Storage

Los mapas de bits deben guardarse en un archivo que use el formato de archivo de mapa de bits establecido y asignar un nombre con la extensión de .bmp caracteres. El formato de archivo de mapa de bits establecido consta de una estructura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) seguida de una estructura [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) Una matriz de [**estructuras RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (también denominada tabla de colores) sigue la estructura del encabezado de información de mapa de bits. La tabla de colores va seguida de una segunda matriz de índices en la tabla de colores (los datos de mapa de bits reales).

El formato de archivo de mapa de bits se muestra en la ilustración siguiente.

![diagrama del formato de archivo de mapa de bits, que muestra la matriz bitmapfileheader, bitmapinfoheader, rgbquad y color-index](images/csbmp-02.png)

Los miembros de la [**estructura BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identifican el archivo; especifique el tamaño del archivo, en bytes; y especifican el desplazamiento del primer byte del encabezado al primer byte de los datos de mapa de bits. Los miembros de la estructura [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) especifican el ancho y alto del mapa de bits, en píxeles; el formato de color (recuento de planos de color y bits de color por píxel) del dispositivo de visualización en el que se creó el mapa de bits; si los datos de mapa de bits se comprimió antes del almacenamiento y el tipo de compresión utilizado; el número de bytes de datos de mapa de bits; la resolución del dispositivo de visualización en el que se creó el mapa de bits; y el número de colores representados en los datos. Las [**estructuras RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) especifican los valores de intensidad RGB para cada uno de los colores de la paleta del dispositivo.

La matriz de índice de color asocia un color, en forma de índice a una [**estructura RGBQUAD,**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) con cada píxel de un mapa de bits. Por lo tanto, el número de bits de la matriz de índice de color es igual al número de píxeles veces el número de bits necesarios para indexar las estructuras **RGBQUAD.** Por ejemplo, un mapa de bits de 8x8 en blanco y negro tiene una matriz de índice de color de 8 \* 8 \* 1 = 64 bits, porque se necesita un bit para indexar dos colores. El Redbrick.bmp, mencionado en Acerca de [los mapas de](about-bitmaps.md)bits , es un mapa de bits de 32 x 32 con 16 colores; su matriz de índice de color es 32 \* 32 \* 4 = 4096 bits porque cuatro bits indexa 16 colores.

Para crear una matriz de índice de color para un mapa de bits de arriba abajo, comience en la línea superior del mapa de bits. El índice de [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para el color del píxel más a la izquierda es el primer *n* bits de la matriz de índice de color (donde *n* es el número de bits necesarios para indicar todas las estructuras **RGBQUAD).** El color del píxel siguiente a la derecha es el siguiente *n* bits de la matriz, etc. Después de alcanzar el píxel más a la derecha de la línea, continúe con el píxel más a la izquierda en la línea siguiente. Continúe hasta que termine con todo el mapa de bits. Si es un mapa de bits de abajo hacia arriba, comience en la línea inferior del mapa de bits en lugar de en la línea superior, siga yendo de izquierda a derecha y continúe hasta la línea superior del mapa de bits.

La siguiente salida hexadecimal muestra el contenido del archivo Redbrick.bmp.


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



En la tabla siguiente se muestran los bytes de datos asociados a las estructuras de un archivo de mapa de bits.



| Estructura                                    | Bytes correspondientes |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x0E 0x35           |
| [**Matriz RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)             | 0x36 0x75           |
| Matriz de índice de colores                            | 0x76 0x275          |



 

 

 
