---
description: Las siguientes funciones se usan con los mapas de bits.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Funciones de mapa de bits (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997433"
---
# <a name="bitmap-functions-windows-gdi"></a>Funciones de mapa de bits (Windows GDI)

Las siguientes funciones se usan con los mapas de bits.



| Función                                                 | Descripción                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Muestra un mapa de bits con píxeles transparentes o semitransparentes.  |
| [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Realiza una transferencia de bloque de bits.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Crea un mapa de bits.                                              |
| [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Crea un mapa de bits.                                              |
| [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Crea un mapa de bits compatible con un dispositivo.                     |
| [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Crea un mapa de bits dependiente del dispositivo (DDB) a partir de un DIB.            |
| [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Crea un DIB en el que las aplicaciones pueden escribir directamente.         |
| [**ExtFloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Rellena un área de la superficie de presentación con el pincel actual.   |
| [**GetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Obtiene las dimensiones de un mapa de bits.                               |
| [**GetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Recupera los valores de color RGB de un mapa de bits de sección DIB.          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Copia un mapa de bits en un búfer.                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Obtiene el valor de color RGB del píxel en una coordenada especificada.   |
| [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Obtiene el modo de ajuste actual.                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Rellena las estructuras de rectángulos y triángulos.                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Carga un mapa de bits desde el archivo ejecutable de un módulo.                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Combina los datos de color de los mapas de bits de origen y de destino. |
| [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Realiza una transferencia de bloque de bits.                                 |
| [**SetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Establece las dimensiones preferidas en un mapa de bits.                     |
| [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Establece valores RGB en un DIB.                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Establece los píxeles de un mapa de bits utilizando los datos de color de un DIB.       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Establece los píxeles de un rectángulo utilizando los datos de color de un DIB.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Establece el color de un píxel.                                    |
| [**SetPixelV**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Establece un píxel en la mejor aproximación de un color.             |
| [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Establece el modo de ajuste de mapa de bits.                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Copia un mapa de bits y lo expande o comprime.                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Copia los datos de color de un DIB.                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Realiza una transferencia de bloque de bits de datos de color.                   |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Las siguientes funciones solo se proporcionan por compatibilidad con las versiones de 16 bits de Microsoft Windows:

-   [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**GetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**SetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



