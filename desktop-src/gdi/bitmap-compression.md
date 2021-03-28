---
description: Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel. La compresión reduce el almacenamiento en disco y memoria necesario para el mapa de bits.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compresión de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155700"
---
# <a name="bitmap-compression"></a>Compresión de mapa de bits

Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel. La compresión reduce el almacenamiento en disco y memoria necesario para el mapa de bits.

Cuando el miembro de **compresión** de la estructura de encabezado de información de mapa de bits es bi \_ RLE8, se usa un formato de codificación de longitud de ejecución (RLE) para comprimir un mapa de bits de 8 bits. Este formato se puede comprimir en los modos codificado o absoluto. Ambos modos pueden aparecer en cualquier lugar del mismo mapa de bits:

-   El *modo codificado* consta de dos bytes: el primer byte especifica el número de píxeles consecutivos que se van a dibujar utilizando el índice de color contenido en el segundo byte. Además, el primer byte del par se puede establecer en cero para indicar un carácter de escape que denota el final de una línea, el final de un mapa de bits o un delta, dependiendo del valor del segundo byte. La interpretación del escape depende del valor del segundo byte del par, que puede ser uno de los valores siguientes.



| Value | Significado                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fin de línea.                                                                                                                                                |
| 1     | Fin del mapa de bits.                                                                                                                                              |
| 2     | Paragua. Los 2 bytes que siguen al escape contienen valores sin signo que indican los desplazamientos horizontal y vertical del siguiente píxel desde la posición actual. |



 

-   En el *modo absoluto*, el primer byte es cero y el segundo byte es un valor en el intervalo 03h a través de FFH. El segundo byte representa el número de bytes siguientes, cada uno de los cuales contiene el índice de color de un solo píxel. Cuando el segundo byte es dos o menos, el escape tiene el mismo significado que el modo codificado. En el modo absoluto, cada ejecución debe estar alineada en un límite de palabras.

En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 8 bits:


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



El mapa de bits se expande de la manera siguiente (los valores de dos dígitos representan un índice de color para un solo píxel):


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Cuando el miembro de **compresión** es bi \_ RLE4, el mapa de bits se comprime con un formato de codificación de longitud de ejecución para un mapa de bits de 4 bits, que también usa los modos codificado y absoluto:

-   En el modo codificado, el primer byte del par contiene el número de píxeles que se van a dibujar utilizando los índices de color del segundo byte. El segundo byte contiene dos índices de color, uno en sus 4 bits de orden superior y otro en sus 4 bits de orden inferior. El primero de los píxeles se dibuja utilizando el color especificado por los 4 bits de orden superior, el segundo se dibuja con el color de los 4 bits de orden inferior, el tercero se dibuja usando el color de los 4 bits de orden superior, y así sucesivamente, hasta que se dibujen todos los píxeles especificados por el primer byte.
-   En el modo absoluto, el primer byte es cero. El segundo byte contiene el número de índices de color que siguen. Los bytes siguientes contienen índices de color en sus 4 bits de orden superior y mínimo, un índice de color para cada píxel. En el modo absoluto, cada ejecución debe estar alineada en un límite de palabras. Los escapes de fin de línea, final de mapa de bits y Delta descritos para RLE8 de BI \_ también se aplican a la \_ compresión RLE4 de BI.

En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 4 bits:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



El mapa de bits se expande de la manera siguiente (los valores de un solo dígito representan un índice de color para un solo píxel):


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



