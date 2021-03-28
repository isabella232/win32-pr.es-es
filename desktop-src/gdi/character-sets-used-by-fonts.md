---
description: Todas las fuentes utilizan un juego de caracteres. Un juego de caracteres contiene signos de puntuación, números, letras mayúsculas y minúsculas, y todos los demás caracteres imprimibles. Cada elemento de un juego de caracteres se identifica mediante un número.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Juegos de caracteres usados por fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985059"
---
# <a name="character-sets-used-by-fonts"></a>Juegos de caracteres usados por fuentes

Todas las fuentes utilizan un juego de caracteres. Un juego de caracteres contiene signos de puntuación, números, letras mayúsculas y minúsculas, y todos los demás caracteres imprimibles. Cada elemento de un juego de caracteres se identifica mediante un número.

La mayoría de los juegos de caracteres en uso son superconjuntos del juego de caracteres ASCII de EE. UU., que define los caracteres de los valores numéricos 96 de 32 a 127. Hay cinco grupos principales de juegos de caracteres:

-   Windows
-   Unicode
-   OEM (fabricante de equipo original)
-   Símbolo
-   Específico del proveedor

## <a name="windows-character-set"></a>Juego de caracteres de Windows

El juego de caracteres de Windows es el juego de caracteres que se usa con más frecuencia. Esencialmente, es equivalente al Juego de caracteres ANSI. El carácter en blanco es el primer carácter del juego de caracteres de Windows. Tiene un valor hexadecimal de 0x20 (decimal 32). El último carácter del juego de caracteres de Windows tiene un valor hexadecimal de 0xFF (decimal 255).

Muchas fuentes especifican un carácter predeterminado. Siempre que se realiza una solicitud para un carácter que no está en la fuente, el sistema proporciona este carácter predeterminado. Muchas fuentes que utilizan el juego de caracteres de Windows especifican el punto (.) como el carácter predeterminado. Las fuentes TrueType y OpenType suelen usar un cuadro abierto como carácter predeterminado.

Las fuentes usan un carácter de salto denominado cuádruple para separar palabras y justificar texto. La mayoría de las fuentes que utilizan el juego de caracteres de Windows especifican que el carácter en blanco servirá como carácter de salto.

## <a name="unicode-character-set"></a>Juego de caracteres Unicode

El juego de caracteres de Windows usa 8 bits para representar cada carácter; por lo tanto, el número máximo de caracteres que se pueden expresar con 8 bits es 256 (2 ^ 8). Esto suele ser suficiente para los idiomas occidentales, incluidas las marcas diacríticas usadas en francés, alemán, español y otros idiomas. Sin embargo, los idiomas orientales emplean miles de caracteres independientes, que no se pueden codificar mediante un esquema de codificación de un solo byte. Con la proliferación de comercio de equipos, los esquemas de codificación de doble byte se desarrollaron para que los caracteres se pudieran representar en secuencias de 8 bits, de 16 bits, de 24 bits o de 32 bits. Esto requiere algoritmos de paso complicados; aun así, el uso de conjuntos de código diferentes podría producir resultados totalmente diferentes en dos equipos diferentes.

Para solucionar el problema de varios esquemas de codificación, se desarrolló el estándar Unicode para la representación de datos. Un esquema de codificación de caracteres de 16 bits, Unicode puede representar 65.536 (2 ^ 16) caracteres, que es suficiente para incluir todos los idiomas en el comercio de equipos, así como signos de puntuación, símbolos matemáticos y espacio para la expansión. Unicode establece un código único para cada carácter con el fin de garantizar que la traducción de caracteres sea siempre precisa.

## <a name="oem-character-set"></a>Juego de caracteres OEM

El juego de caracteres OEM se usa normalmente en las sesiones de MS-DOS de pantalla completa para la presentación en pantalla. Los caracteres de 32 a 127 suelen ser los mismos en los juegos de caracteres OEM, ASCII estadounidense y Windows. Los demás caracteres del juego de caracteres OEM (de 0 a 31 y de 128 a 255) corresponden a los caracteres que se pueden mostrar en una sesión de MS-DOS de pantalla completa. Estos caracteres suelen ser diferentes de los caracteres de Windows.

## <a name="symbol-character-set"></a>Juego de caracteres de símbolos

El juego de caracteres de símbolos contiene caracteres especiales que se suelen usar para representar fórmulas matemáticas y científicas.

## <a name="vendor-specific-character-sets"></a>Juegos de caracteres específicos del proveedor

Muchas impresoras y otros dispositivos de salida proporcionan fuentes basadas en juegos de caracteres que difieren del ejemplo de Windows y OEM setsfor, el juego de caracteres Extended Binary Coded Decimal Interchange Code (EBCDIC). Para usar uno de estos juegos de caracteres, el controlador de impresora se traduce del juego de caracteres de Windows al Juego de caracteres específico del proveedor.

 

 



