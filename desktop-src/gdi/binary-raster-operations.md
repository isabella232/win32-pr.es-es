---
description: En esta sección se enumeran los códigos binarios de operación de trama usados por las funciones GetROP2 y SetROP2. Los códigos de operación de trama definen cómo GDI combina los bits del lápiz seleccionado con los bits del mapa de bits de destino.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operaciones de trama binarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462c07165d7f377f2a536722bf2f728446c308503108474cbb6a585cee6f68e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105814"
---
# <a name="binary-raster-operations"></a>Operaciones de trama binarias

En esta sección se enumeran los códigos binarios de operación de trama usados por las [**funciones GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) [**y SetROP2.**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) Los códigos de operación de trama definen cómo GDI combina los bits del lápiz seleccionado con los bits del mapa de bits de destino.

Cada código de operación de trama representa una operación booleana en la que se combinan los valores de los píxeles del lápiz seleccionado y el mapa de bits de destino. Estos son los dos operandos que se usan en estas operaciones.



| Operando | Significado            |
|---------|--------------------|
| P       | Lápiz seleccionado       |
| D       | Mapa de bits de destino |



 

Los operadores booleanos usados en estas operaciones siguen.



| Operator | Significado                    |
|----------|----------------------------|
| a        | AND bit a bit                |
| n        | NOT bit a bit (inverso)      |
| o        | OR bit a bit                 |
| x        | OR exclusivo bit a bit (XOR) |



 

Todas las operaciones booleanas se presentan en la notación inversa del polaco. Por ejemplo, la siguiente operación reemplaza los valores de los píxeles del mapa de bits de destino por una combinación de los valores de píxel del lápiz y el pincel seleccionado:


```C++
DPo 
```



Cada código de operación de trama es un entero de 32 bits cuya palabra de orden superior es un índice de operación booleano y cuya palabra de orden bajo es el código de operación. El índice de operación de 16 bits es un valor de 8 bits extendido a cero que representa todos los resultados posibles resultantes de la operación booleana en dos parámetros (en este caso, el lápiz y los valores de destino). Por ejemplo, los índices de operación para las operaciones DPo y DPan se muestran en la lista siguiente.



| P   | D   | Dpo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

En la lista siguiente se describen los modos de dibujo y las operaciones booleanas que representan.



| Operación de trama | Operación booleana |
|------------------|-------------------|
| R2 \_ BLACK        | 0                 |
| R2 \_ COPYPEN      | P                 |
| MASKNOTPEN de R2 \_   | DPna              |
| R2 \_ MASKPEN      | Dpa               |
| MASKPENNOT de R2 \_   | PDna              |
| R2 \_ MERGENOTPEN  | DPno              |
| R2 \_ MERGEPEN     | Dpo               |
| R2 \_ MERGEPENNOT  | PDno              |
| R2 \_ NOP          | D                 |
| R2 \_ NOT          | Dn                |
| R2 \_ NOTCOPYPEN   | Pn                |
| R2 \_ NOTMASKPEN   | DPan              |
| R2 \_ NOTMERGEPEN  | DPon              |
| R2 \_ NOTXORPEN    | DPxn              |
| R2 \_ WHITE        | 1                 |
| R2 \_ XORPEN       | Dpx               |



 

Para un dispositivo monocromo, GDI asigna el valor cero a negro y el valor 1 a blanco. Si una aplicación intenta dibujar con un lápiz negro en un destino blanco mediante las operaciones de trama binarias disponibles, se producen los siguientes resultados.



| Operación de trama | Resultado             |
|------------------|--------------------|
| R2 \_ BLACK        | Línea negra visible |
| R2 \_ COPYPEN      | Línea negra visible |
| MASKNOTPEN de R2 \_   | Sin línea visible    |
| R2 \_ MASKPEN      | Línea negra visible |
| MASKPENNOT de R2 \_   | Línea negra visible |
| R2 \_ MERGENOTPEN  | Sin línea visible    |
| R2 \_ MERGEPEN     | Línea negra visible |
| R2 \_ MERGEPENNOT  | Línea negra visible |
| R2 \_ NOP          | Sin línea visible    |
| R2 \_ NOT          | Línea negra visible |
| R2 \_ NOTCOPYPEN   | Sin línea visible    |
| R2 \_ NOTMASKPEN   | Sin línea visible    |
| R2 \_ NOTMERGEPEN  | Línea negra visible |
| R2 \_ NOTXORPEN    | Línea negra visible |
| R2 \_ WHITE        | Sin línea visible    |
| R2 \_ XORPEN       | Sin línea visible    |



 

Para un dispositivo de color, GDI usa valores RGB para representar los colores del lápiz y el destino. Un valor de color RGB es un entero largo que contiene un campo de color rojo, verde y azul, cada uno de los que especifica la intensidad del color especificado. Las intensidades van de 0 a 255. Los valores se empaquetan en los tres bytes de orden bajo del entero largo. El color de un lápiz siempre es un color sólido, pero el color del destino puede ser una mezcla de dos o tres colores cualquiera. Si una aplicación intenta dibujar con un lápiz blanco en un destino azul mediante las operaciones de trama binarias disponibles, se producen los siguientes resultados.



| Operación de trama | Resultado                 |
|------------------|------------------------|
| R2 \_ BLACK        | Línea negra visible     |
| R2 \_ COPYPEN      | Línea blanca visible     |
| MASKNOTPEN de R2 \_   | Línea negra visible     |
| R2 \_ MASKPEN      | Línea azul invisible    |
| MASKPENNOT de R2 \_   | Línea visible de color rojo/verde |
| R2 \_ MERGENOTPEN  | Línea azul invisible    |
| R2 \_ MERGEPEN     | Línea blanca visible     |
| R2 \_ MERGEPENNOT  | Línea blanca visible     |
| R2 \_ NOP          | Línea azul invisible    |
| R2 \_ NOT          | Línea visible de color rojo/verde |
| R2 \_ NOTCOPYPEN   | Línea negra visible     |
| R2 \_ NOTMASKPEN   | Línea visible de color rojo/verde |
| R2 \_ NOTMERGEPEN  | Línea negra visible     |
| R2 \_ NOTXORPEN    | Línea azul invisible    |
| R2 \_ WHITE        | Línea blanca visible     |
| R2 \_ XORPEN       | Línea visible de color rojo/verde |



 

 

 



