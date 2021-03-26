---
title: Gramática
description: Las instrucciones de HLSL se construyen con las siguientes reglas para la gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532902"
---
# <a name="grammar"></a>Gramática

Las instrucciones de HLSL se construyen con las siguientes reglas para la gramática.

-   [Eran](#whitespace)
-   [Números de punto flotante](#floating-point-numbers)
-   [Números enteros](#integer-numbers)
-   [Caracteres](#characters)
-   [Cadenas](#strings)
-   [Identificadores](#identifiers)
-   [Operadores](#operators)
-   [Temas relacionados](#related-topics)

## <a name="whitespace"></a>Espacio en blanco

Los caracteres siguientes se reconocen como un espacio en blanco.



|                            |
|----------------------------|
| SPACE                      |
| TAB                        |
| EOL                        |
| Comentarios de estilo de C (/ \* \* /) |
| Comentarios de estilo de C++ (//)    |



 

## <a name="floating-point-numbers"></a>Números de punto flotante

Los números de punto flotante se representan en HLSL de la siguiente manera:

-   elemento de exponente de constante fraccionaria (OPC) sufijo flotante (OPT)

    exponente de secuencia de dígitos-sufijo flotante de parte (OPT)

-   fraccionario-constante:

    Digit-Sequence (OPT). Digit-Sequence

    secuencia de dígitos.

-   exponente: parte:

    e signo (OPT) dígito-secuencia

    E signo (OPT) dígito-secuencia

-   sign : one of

    \+ -

-   Digit-Sequence:

    digit

    digit-sequence digit

-   floating-suffix : one of

    h H f F l

    Use el sufijo "L" para especificar un literal de punto flotante de precisión de 64 bits completo. Un literal de punto flotante de 32 bits es el valor predeterminado.

    Por ejemplo, el compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 32 bits y omite los bits inferiores:

    ```
    double x = -0.6473313946860445;
    ```

    

    El compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 64 bits:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Números enteros

Los números enteros se representan en HLSL de la siguiente manera:

-   entero: entero constante: sufijo (OPT)
-   entero: constante: uno de

    \# (número decimal)

    0 \# (número octal)

    0x \# (número hexadecimal)

-   Integer-Suffix puede ser cualquiera de los siguientes:

    u U l L

## <a name="characters"></a>Characters

Los caracteres se representan en HLSL de la siguiente manera:



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| "c"                                       | óptico                                                     |
| ' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v ' | escape                                                       |
| '\\\#\#\#'                                | (escape octal, cada uno \# es un dígito octal)                       |
| ' \\ x \# '                                   | (escape hexadecimal, \# es un número hexadecimal, cualquier número de dígitos)            |
| ' \\ c '                                     | (c es otro carácter, incluida la barra diagonal inversa y comillas) |



 

Los escapes no se admiten en expresiones de preprocesador.

## <a name="strings"></a>Cadenas

Las cadenas se representan en HLSL de la siguiente manera:

"s" (s es cualquier cadena con escapes).

## <a name="identifiers"></a>Identificadores

Los identificadores se representan en HLSL de la siguiente manera:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operadores


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



También cualquier otro carácter individual que no coincidía con otra regla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




