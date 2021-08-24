---
description: Todas las fuentes usan un juego de caracteres. Un juego de caracteres contiene signos de puntuación, números, letras mayúsculas y minúsculas, y todos los demás caracteres imprimibles. Cada elemento de un juego de caracteres se identifica mediante un número.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Juegos de caracteres usados por fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ec30a82c08a0b9ac1162034b6308bb68ff7dc1c6469e5e73bad2838b528eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779365"
---
# <a name="character-sets-used-by-fonts"></a>Juegos de caracteres usados por fuentes

Todas las fuentes usan un juego de caracteres. Un juego de caracteres contiene signos de puntuación, números, letras mayúsculas y minúsculas, y todos los demás caracteres imprimibles. Cada elemento de un juego de caracteres se identifica mediante un número.

La mayoría de los juegos de caracteres en uso son superconjuntos del juego de caracteres ASCII de EE. UU., que define caracteres para los 96 valores numéricos de 32 a 127. Hay cinco grupos principales de juegos de caracteres:

-   Windows
-   Unicode
-   OEM (fabricante de equipo original)
-   Símbolo
-   Específico del proveedor

## <a name="windows-character-set"></a>Windows Juego de caracteres

El Windows juego de caracteres es el juego de caracteres que se usa con más frecuencia. Es básicamente equivalente al juego de caracteres ANSI. El carácter en blanco es el primer carácter del Windows juego de caracteres. Tiene un valor hexadecimal de 0x20 (decimal 32). El último carácter del Windows juego de caracteres tiene un valor hexadecimal de 0xFF (decimal 255).

Muchas fuentes especifican un carácter predeterminado. Siempre que se realiza una solicitud para un carácter que no está en la fuente, el sistema proporciona este carácter predeterminado. Muchas fuentes que usan Windows juego de caracteres especifican el punto (.) como carácter predeterminado. Las fuentes TrueType y OpenType suelen usar un cuadro abierto como carácter predeterminado.

Las fuentes usan un carácter de interrupción denominado cuadrándular para separar palabras y justificar el texto. La mayoría de las fuentes que Windows juego de caracteres especifican que el carácter en blanco actuará como carácter de interrupción.

## <a name="unicode-character-set"></a>Juego de caracteres Unicode

El Windows de caracteres usa 8 bits para representar cada carácter; Por lo tanto, el número máximo de caracteres que se pueden expresar con 8 bits es 256 (2^8). Esto suele ser suficiente para los idiomas occidental, incluidas las marcas diacríticas usadas en francés, alemán, español y otros idiomas. Sin embargo, los idiomas orientales emplean miles de caracteres independientes, que no se pueden codificar mediante un esquema de codificación de un solo byte. Con la proliferación del comercio informático, se desarrollaron esquemas de codificación de doble byte para que los caracteres se pudieran representar en secuencias de 8 bits, 16 bits, 24 o 32 bits. Esto requiere algoritmos de paso complicados; aun así, el uso de conjuntos de código diferentes podría producir resultados completamente diferentes en dos equipos diferentes.

Para solucionar el problema de varios esquemas de codificación, se desarrolló el estándar Unicode para la representación de datos. Un esquema de codificación de caracteres de 16 bits, Unicode puede representar 65 536 (2^16) caracteres, lo que es suficiente para incluir todos los idiomas del comercio informático en la actualidad, así como signos de puntuación, símbolos matemáticos y espacio para la expansión. Unicode establece un código único para cada carácter para asegurarse de que la traducción de caracteres siempre es precisa.

## <a name="oem-character-set"></a>Juego de caracteres oem

El juego de caracteres OEM se usa normalmente en sesiones de MS-DOS de pantalla completa para la presentación en pantalla. Los caracteres del 32 al 127 suelen ser los mismos en el OEM, ASCII de EE. UU. y Windows juegos de caracteres. Los demás caracteres del juego de caracteres OEM (de 0 a 31 y de 128 a 255) corresponden a los caracteres que se pueden mostrar en una sesión de MS-DOS a pantalla completa. Estos caracteres suelen ser diferentes de los Windows caracteres.

## <a name="symbol-character-set"></a>Juego de caracteres de símbolos

El juego de caracteres Symbol contiene caracteres especiales que normalmente se usan para representar fórmulas matemáticas y científicas.

## <a name="vendor-specific-character-sets"></a>Juegos de caracteres específicos del proveedor

Muchas impresoras y otros dispositivos de salida proporcionan fuentes basadas en juegos de caracteres que difieren de los conjuntos de Windows y OEM, por ejemplo, el juego de caracteres Extended Binary Coded Decimal Interchange Code (EBCDIC). Para usar uno de estos juegos de caracteres, el controlador de impresora se traduce Windows juego de caracteres al juego de caracteres específico del proveedor.

 

 



