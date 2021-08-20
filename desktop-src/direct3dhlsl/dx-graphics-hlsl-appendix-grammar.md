---
title: Gramática
description: Las instrucciones HLSL se construyen mediante las reglas siguientes para la gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86549f441752e72fd11a741a061fcaf839eca0140f4766b0932094d74dc78085
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855075"
---
# <a name="grammar"></a>Gramática

Las instrucciones HLSL se construyen mediante las reglas siguientes para la gramática.

-   [Espacio en blanco](#whitespace)
-   [Números de punto flotante](#floating-point-numbers)
-   [Números enteros](#integer-numbers)
-   [Caracteres](#characters)
-   [Cadenas](#strings)
-   [Identificadores](#identifiers)
-   [Operadores](#operators)
-   [Temas relacionados](#related-topics)

## <a name="whitespace"></a>Espacio en blanco

Los caracteres siguientes se reconocen como espacios en blanco.

- SPACE
- TAB
- Eol
- Comentarios de estilo de C (/ \* \* /)
- Comentarios de estilo de C++ (//)

## <a name="floating-point-numbers"></a>Números de punto flotante

Los números de punto flotante se representan en HLSL de la manera siguiente:

-   fractional-constant exponent-part(opt) floating-suffix(opt)

    digit-sequence exponent-part floating-suffix(opt)

-   fractional-constant :

    digit-sequence(opt) . digit-sequence

    digit-sequence .

-   exponent-part :

    e sign(opt) digit-sequence

    E sign(opt) digit-sequence

-   sign : one of

    \+ -

-   digit-sequence :

    digit

    digit-sequence digit

-   floating-suffix : one of

    h H f F l l

    Use el sufijo "L" para especificar un literal de punto flotante de precisión completa de 64 bits. El valor predeterminado es un literal float de 32 bits.

    Por ejemplo, el compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 32 bits y omite los bits inferiores:

    ```
    double x = -0.6473313946860445;
    ```

    

    El compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 64 bits:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Números enteros

Los números enteros se representan en HLSL como se muestra a continuación:

-   integer-constant integer-suffix(opt)
-   integer-constant: uno de

    \# (número decimal)

    0 \# (número octal)

    0x \# (número hexadecimal)

-   integer-suffix puede ser cualquiera de estos:

    u U l L

## <a name="characters"></a>Characters

Los caracteres se representan en HLSL de la siguiente manera:



| Carácter                                          | Descripción                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| "c"                                       | (carácter)                                                     |
| ' \\ a' ' \\ b' ' \\ f' ' \\ b' ' \\ r' \\ ' t' ' \\ v' | (escapes)                                                       |
| '\\\#\#\#'                                | (escape octal, cada \# uno es un dígito octal)                       |
| ' \\ x \# '                                   | (escape hexadecimal, \# es número hexadecimal, cualquier número de dígitos)            |
| ' \\ c'                                     | (c es otro carácter, incluidas las barras diagonales inversas y las comillas) |



 

Los escapes no se admiten en expresiones de preprocesador.

## <a name="strings"></a>Cadenas

Las cadenas se representan en HLSL como se muestra a continuación:

"s" (s es cualquier cadena con escapes).

## <a name="identifiers"></a>Identificadores

Los identificadores se representan en HLSL como se muestra a continuación:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operadores


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



También cualquier otro carácter individual que no coincida con otra regla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndice (HLSL de DirectX)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




