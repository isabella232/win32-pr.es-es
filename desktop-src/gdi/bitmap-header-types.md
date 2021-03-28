---
description: Tipos de encabezado de mapa de bits
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Tipos de encabezado de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b0fb5be1166e807db1f3362186a206abc2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908510"
---
# <a name="bitmap-header-types"></a>Tipos de encabezado de mapa de bits

El mapa de bits tiene cuatro tipos de encabezado básicos:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Los cuatro tipos de encabezados de mapa de bits se diferencian por el miembro de **tamaño** , que es el primer **valor DWORD** de cada una de las estructuras.

La estructura [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) es una estructura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) extendida, que es una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) extendida. Sin embargo, **BITMAPINFOHEADER** y [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) solo tienen el miembro de **tamaño** en común con otras estructuras de encabezado de mapa de bits.

Los formatos [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) y [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) se han sustituido por los formatos [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) y [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) , respectivamente. Los formatos **BITMAPCOREHEADER** y **BITMAPV4HEADER** se presentan por integridad y compatibilidad con versiones anteriores.

El formato de un DIB es el siguiente (para obtener más información, consulte [almacenamiento de mapas de bits](bitmap-storage.md) ):

-   una estructura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   una estructura [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .
-   una tabla de colores opcional, que es un conjunto de estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) o un conjunto de estructuras [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) .
-   los datos de mapa de bits
-   datos de perfil opcionales

Una tabla de colores describe cómo se corresponden los valores de píxeles con los valores de color RGB. RGB es un modelo para describir los colores producidos por la emisión de luz.

Los *datos del perfil* hacen referencia al nombre del archivo de perfil (perfil vinculado) o a los bits de perfil reales (perfil incrustado). El formato de archivo coloca los datos del perfil al final del archivo. Los datos del perfil se colocan justo después de la tabla de colores (si está presente). Sin embargo, si la función recibe un DIB empaquetado, los datos del perfil vienen después de los bits de mapa de bits, como en el formato de archivo.

Los datos del perfil solo existirán para las estructuras [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) donde **bV5CSType** está vinculado a un perfil o se ha \_ \_ incrustado el perfil. En el caso de las funciones que reciben DIB empaquetados, los datos del perfil vienen después de los datos de mapa de bits.

Un dispositivo de paleta es cualquier dispositivo que use paletas para asignar colores. El ejemplo clásico de un dispositivo de paleta es una pantalla que se ejecuta en una profundidad de color de 8 bits (es decir, 256 colores). La presentación en este modo utiliza una tabla de colores pequeña para asignar los colores a un mapa de bits. Los colores de un mapa de bits se asignan al color más cercano de la paleta que usa el dispositivo. El dispositivo de paleta no crea una paleta óptima para mostrar el mapa de bits; simplemente usa todo lo que se encuentra en la paleta actual. Las aplicaciones son responsables de crear una paleta y seleccionarla en el sistema. En general, los mapas de bits de 16, 24 y 32 bits por píxel (BPP) no contienen tablas de colores (también conocido como paletas óptimas para el mapa de bits); en este caso, la aplicación es responsable de generar una paleta óptima. Sin embargo, los mapas de bits de 16, 24 y 32-bpp pueden contener tablas de color óptimas para su visualización en dispositivos de paleta. en este caso, la aplicación solo necesita crear una paleta basada en la tabla de colores presente en el archivo de mapa de bits.

Los mapas de bits que son 1, 4 u 8 BPP deben tener una tabla de colores con un tamaño máximo basado en BPP. El tamaño máximo de los mapas de bits de 1, 4 y 8 BPP es 2 para la potencia de BPP. Por lo tanto, un mapa de bits 1 BPP tiene un máximo de dos colores, el mapa de bits de 4 BPP tiene un máximo de 16 colores y el mapa de bits de 8 BPP tiene un máximo de 256 colores.

Los mapas de bits de 16, 24 o 32-bpp no requieren tablas de color, pero pueden especificar los colores de los dispositivos de paleta. Si hay una tabla de colores para un mapa de bits de 16, 24 o 32-bpp, el miembro **biClrUsed** especifica el tamaño de la tabla de colores y la tabla de colores debe tener muchos colores. Si **biClrUsed** es cero, no hay ninguna tabla de colores.

Las máscaras de mapa de bits rojo, verde y azul para los mapas de bits de un campo de bits de BI \_ siguen inmediatamente a las estructuras [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)y [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Las estructuras **BITMAPV4HEADER** y **BITMAPV5HEADER** contienen miembros adicionales para las máscaras rojo, verde y azul como se indica a continuación.



| Miembro        | Significado                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Máscara de color que especifica el componente rojo de cada píxel, solo es válido si el miembro de **compresión** se establece en campos de campos de BI \_ .   |
| **GreenMask** | Máscara de color que especifica el componente verde de cada píxel, solo es válido si el miembro de **compresión** se establece en campos de campos de BI \_ . |
| **BlueMask**  | Máscara de color que especifica el componente azul de cada píxel, solo es válido si el miembro de **compresión** se establece en campos de campos de BI \_ .  |



 

Cuando el miembro **bicompression** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) se establece en \_ campos de tipos de BI y la función recibe un argumento de tipo **LPBITMAPINFO**, las máscaras de color seguirán inmediatamente al encabezado. La tabla de colores, si está presente, seguirá las máscaras de color. Los mapas de bits de [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) no admiten máscaras de color.

De forma predeterminada, los datos de mapa de bits están en su formato. Ascendente significa que la primera línea de exploración de los datos de mapa de bits es la última que se va a mostrar. Por ejemplo, el píxel 0 de la línea de<sup>exploración 0 de</sup> los datos de mapa de bits de un mapa de bits de 10 píxeles por 10 píxeles será<sup>el píxel 0</sup> de la<sup></sup> línea<sup>de exploración 9</sup> de la imagen mostrada o impresa. Los mapas de bits de formato de longitud de ejecución (RLE) y los mapas de bits de [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) no pueden ser mapas de bits de arriba abajo. Las líneas de recorrido están alineadas con **DWORD** , excepto en el caso de los mapas de bits comprimidos por RLE. Se deben rellenar para los anchos de línea de digitalización, en bytes, que no se pueden dividir uniformemente por cuatro, excepto para los mapas de bits comprimidos RLE. Por ejemplo, un mapa de bits de 10 x 10 píxeles de 24 píxeles tendrá dos bytes de relleno al final de cada línea de exploración.

 

 
