---
description: En esta sección se enumeran los códigos de operación de trama binaria utilizados por las funciones GetROP2 y SetROP2. Los códigos de operación de trama definen cómo combina GDI los bits del lápiz seleccionado con los bits en el mapa de bits de destino.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operaciones de trama binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155701"
---
# <a name="binary-raster-operations"></a>Operaciones de trama binaria

En esta sección se enumeran los códigos de operación de trama binaria utilizados por las funciones [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) y [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) . Los códigos de operación de trama definen cómo combina GDI los bits del lápiz seleccionado con los bits en el mapa de bits de destino.

Cada código de operación de trama representa una operación booleana en la que se combinan los valores de los píxeles del lápiz seleccionado y el mapa de bits de destino. A continuación se muestran los dos operandos utilizados en estas operaciones.



| Operando | Significado            |
|---------|--------------------|
| P       | Pluma seleccionada       |
| D       | Mapa de bits de destino |



 

A continuación se indican los operadores booleanos que se usan en estas operaciones.



| Operator | Significado                    |
|----------|----------------------------|
| a        | AND bit a bit                |
| n        | NOT bit a bit (inversa)      |
| o        | OR bit a bit                 |
| x        | Or exclusivo bit a bit (XOR) |



 

Todas las operaciones booleanas se presentan en notación Polaco inversa. Por ejemplo, la siguiente operación reemplaza los valores de los píxeles en el mapa de bits de destino por una combinación de los valores de píxeles del lápiz y del pincel seleccionado:


```C++
DPo 
```



Cada código de operación de trama es un entero de 32 bits cuya palabra de orden superior es un índice de operación booleano y cuya palabra de orden inferior es el código de operación. El índice de operación de 16 bits es un valor de 8 bits extendido con ceros que representa todos los resultados posibles que se derivan de la operación booleana con dos parámetros (en este caso, los valores de lápiz y destino). Por ejemplo, los índices de operación de las operaciones DPo y DPan se muestran en la lista siguiente.



| P   | D   | DPo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

En la siguiente lista se describen los modos de dibujo y las operaciones booleanas que representan.



| Operación de trama | Operación booleana |
|------------------|-------------------|
| R2 \_ negro        | 0                 |
| \_COPYPEN R2      | P                 |
| \_MASKNOTPEN R2   | DPna              |
| \_MASKPEN R2      | DPa               |
| \_MASKPENNOT R2   | PDna              |
| \_MERGENOTPEN R2  | DPno              |
| \_MERGEPEN R2     | DPo               |
| \_MERGEPENNOT R2  | PDno              |
| NOP de R2 \_          | D                 |
| R2 \_ no          | Dn                |
| \_NOTCOPYPEN R2   | VPN                |
| \_NOTMASKPEN R2   | DPan              |
| \_NOTMERGEPEN R2  | DPon              |
| \_NOTXORPEN R2    | DPxn              |
| R2 \_ blanco        | 1                 |
| \_XORPEN R2       | DPx               |



 

Para un dispositivo monocromo, GDI asigna el valor cero a negro y el valor 1 a blanco. Si una aplicación intenta dibujar con un lápiz negro en un destino blanco mediante las operaciones de trama binaria disponibles, se producen los siguientes resultados.



| Operación de trama | Resultado             |
|------------------|--------------------|
| R2 \_ negro        | Línea negra visible |
| \_COPYPEN R2      | Línea negra visible |
| \_MASKNOTPEN R2   | No hay ninguna línea visible    |
| \_MASKPEN R2      | Línea negra visible |
| \_MASKPENNOT R2   | Línea negra visible |
| \_MERGENOTPEN R2  | No hay ninguna línea visible    |
| \_MERGEPEN R2     | Línea negra visible |
| \_MERGEPENNOT R2  | Línea negra visible |
| NOP de R2 \_          | No hay ninguna línea visible    |
| R2 \_ no          | Línea negra visible |
| \_NOTCOPYPEN R2   | No hay ninguna línea visible    |
| \_NOTMASKPEN R2   | No hay ninguna línea visible    |
| \_NOTMERGEPEN R2  | Línea negra visible |
| \_NOTXORPEN R2    | Línea negra visible |
| R2 \_ blanco        | No hay ninguna línea visible    |
| \_XORPEN R2       | No hay ninguna línea visible    |



 

Para un dispositivo de color, GDI usa valores RGB para representar los colores del lápiz y el destino. Un valor de color RGB es un entero largo que contiene un campo de color rojo, verde y azul, cada uno de los cuales especifica la intensidad del color especificado. La intensidad oscila entre 0 y 255. Los valores se empaquetan en los tres bytes de orden inferior del entero largo. El color de un lápiz siempre es un color sólido, pero el color del destino puede ser una combinación de dos o tres colores. Si una aplicación intenta dibujar con un lápiz blanco en un destino azul mediante las operaciones binarias de tramas disponibles, se producirán los resultados siguientes.



| Operación de trama | Resultado                 |
|------------------|------------------------|
| R2 \_ negro        | Línea negra visible     |
| \_COPYPEN R2      | Línea blanca visible     |
| \_MASKNOTPEN R2   | Línea negra visible     |
| \_MASKPEN R2      | Línea azul invisible    |
| \_MASKPENNOT R2   | Línea visible de rojo/verde |
| \_MERGENOTPEN R2  | Línea azul invisible    |
| \_MERGEPEN R2     | Línea blanca visible     |
| \_MERGEPENNOT R2  | Línea blanca visible     |
| NOP de R2 \_          | Línea azul invisible    |
| R2 \_ no          | Línea visible de rojo/verde |
| \_NOTCOPYPEN R2   | Línea negra visible     |
| \_NOTMASKPEN R2   | Línea visible de rojo/verde |
| \_NOTMERGEPEN R2  | Línea negra visible     |
| \_NOTXORPEN R2    | Línea azul invisible    |
| R2 \_ blanco        | Línea blanca visible     |
| \_XORPEN R2       | Línea visible de rojo/verde |



 

 

 



