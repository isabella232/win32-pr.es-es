---
description: Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel. La compresión reduce el disco y el almacenamiento de memoria necesarios para el mapa de bits.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compresión de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefec93bb5583ba066e35d5143410d1c249bb09
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812851"
---
# <a name="bitmap-compression"></a>Compresión de mapa de bits

Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel. La compresión reduce el disco y el almacenamiento de memoria necesarios para el mapa de bits.

Cuando el **miembro Compression** de la estructura del encabezado de información de mapa de bits es BI RLE8, se usa un formato de codificación de longitud de ejecución (RLE) para comprimir un mapa de bits de \_ 8 bits. Este formato se puede comprimir en modos codificados o absolutos. Ambos modos pueden producirse en cualquier lugar del mismo mapa de bits:

-   *El modo codificado* consta de dos bytes: el primer byte especifica el número de píxeles consecutivos que se dibujarán mediante el índice de color contenido en el segundo byte. Además, el primer byte del par se puede establecer en cero para indicar un carácter de escape que denota el final de una línea, el final de un mapa de bits o una diferencia, según el valor del segundo byte. La interpretación del escape depende del valor del segundo byte del par, que puede ser uno de los valores siguientes.



| Valor | Significado                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Final de línea.                                                                                                                                                |
| 1     | Final del mapa de bits.                                                                                                                                              |
| 2     | Delta. Los 2 bytes siguientes al escape contienen valores sin signo que indican los desplazamientos horizontal y vertical del píxel siguiente desde la posición actual. |



 

-   En *modo absoluto*, el primer byte es cero y el segundo byte es un valor en el intervalo de 03H a FFH. El segundo byte representa el número de bytes siguientes, cada uno de los cuales contiene el índice de color de un solo píxel. Cuando el segundo byte es dos o menos, el escape tiene el mismo significado que el modo codificado. En modo absoluto, cada ejecución debe agregarse sin relleno para terminar en un límite de palabras de 16 bits.

En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 8 bits:


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



El mapa de bits se expande de la siguiente manera (los valores de dos dígitos representan un índice de color para un solo píxel):


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



Cuando el **miembro Compression** es BI RLE4, el mapa de bits se comprime mediante un formato de codificación de longitud de ejecución para un mapa de bits de 4 bits, que también usa modos codificados y \_ absolutos:

-   En el modo codificado, el primer byte del par contiene el número de píxeles que se dibujarán mediante los índices de color del segundo byte. El segundo byte contiene dos índices de color, uno en su orden alto de 4 bits y otro en su orden inferior de 4 bits. El primero de los píxeles se dibuja con el color especificado por los 4 bits de orden superior, el segundo se dibuja con el color de 4 bits de orden inferior, el tercero se dibuja con el color de 4 bits de orden superior, y así sucesivamente, hasta que se han dibujado todos los píxeles especificados por el primer byte.
-   En modo absoluto, el primer byte es cero. El segundo byte contiene el número de índices de color siguientes. Los bytes posteriores contienen índices de color en sus 4 bits de orden alto y bajo, un índice de color para cada píxel. En modo absoluto, cada ejecución debe alinearse en un límite de palabras. Los escapes delta, de fin de línea y de fin de mapa de bits descritos para BI RLE8 también se aplican a la compresión \_ \_ BI RLE4.

En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 4 bits:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



El mapa de bits se expande de la siguiente manera (los valores de un solo dígito representan un índice de color para un solo píxel):


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



 

 



