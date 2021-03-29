---
title: Problemas de empaquetado del compilador de C
description: Los niveles de empaquetado afectan al diseño de memoria de los tipos de MIDL y del compilador de C/C++ de Microsoft de la misma manera.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- 'MIDL del compilador MIDL; C: problemas de empaquetado del compilador'
- empaquetar MIDL
- MIDL de diseño de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904570"
---
# <a name="c-compiler-packing-issues"></a>Problemas de empaquetado del compilador de C

Los niveles de empaquetado afectan al diseño de memoria de los tipos de MIDL y del compilador de C/C++ de Microsoft de la misma manera. En entornos de compilación de Microsoft, como el entorno de compilación definido por VC + + o el kit de desarrollo de software (SDK) de plataforma, el nivel de empaquetado predeterminado para los compiladores de MIDL y C/C++ es el mismo. el nivel de empaquetado predeterminado para los entornos de compilación de Windows de 32 y 64 bits es 8.

## <a name="natural-alignment"></a>Alineación natural

En el caso de los tipos de memoria, la alineación predeterminada es la misma que su alineación natural.

-   Un tipo base, como Short, Float e \_ \_ Int64, y un puntero se alinea de forma natural si su representación comienza en una dirección cuyo tamaño es módulo. Todos los tipos base admitidos actualmente tienen tamaños de 1, 2, 4 u 8. Los punteros tienen un tamaño de 4 en entornos de 32 bits y 8 en entornos de 64 bits.
-   Un tipo compuesto está alineado de forma natural si cada uno de sus componentes está alineado de forma natural con respecto al principio del tipo y si no hay ningún hueco (relleno) innecesario entre los componentes. Los componentes compuestos, como campos o elementos, se recorren en componentes de puntero o de tipo base.

Una regla sencilla para ayudar a recordar este comportamiento es que la alineación natural de un tipo es igual a las alineaciones más importantes de sus componentes.

Existe una conexión entre la alineación y el tamaño de la memoria de un tipo en lenguajes como C o C++ y IDL, tal y como se expresa en el operador **sizeof ()**. El tamaño es un múltiplo de la alineación (el múltiplo mínimo que abarca el tipo). Esto sigue a partir de una representación de matriz en la memoria.

La alineación natural es importante porque el acceso a los datos desalineados puede producir una excepción en algunos sistemas. Los datos se pueden marcar para una manipulación segura cuando están mal alineados, pero normalmente esto implica una penalización de velocidad que puede ser considerable en algunas plataformas.

> [!Note]  
> En la memoria, se garantiza que los objetos de tipos con una alineación natural de *n* se alineen correctamente cuando se colocan en direcciones que son un múltiplo de *n*.

 

## <a name="packing-versus-alignment"></a>Empaquetado frente a alineación

Si se especifica un nivel de empaquetado mayor que la alineación natural de un tipo, no se cambia la alineación del tipo. La especificación de un nivel de empaquetado menor que la alineación natural reduce la alineación del tipo al nivel de empaquetado. Como resultado, los tipos empaquetados se pueden colocar en la memoria en direcciones que son un múltiplo del nivel de empaquetado (la alineación reducida) sin causar una falta de alineación. Esto afecta a los tipos simples y a los tipos de componentes. En el caso de los tipos compuestos, el diseño interno del tipo puede verse afectado, ya que la alineación reducida de los componentes puede cambiar el tamaño de relleno necesario para la alineación adecuada de los componentes, lo que reduce el tamaño del tipo.

Una regla sencilla para ayudar a recordar este comportamiento es que la nueva alineación de un tipo empaquetado es el menor del nivel de empaquetado y su alineación natural. El tamaño del tipo es un múltiplo de la nueva alineación. El operador **sizeof ()** devuelve el tamaño reducido de los tipos empaquetados.

Por ejemplo, con el nivel 2 de empaquetado se alinea a la 2 y, por lo tanto, se puede colocar en cualquier dirección, no solo en las direcciones que son un múltiplo de 4, como sucede con la alineación natural. Una estructura con un valor Short y Long, empaquetada en 2, no necesita la separación interna entre el corto y el tiempo siguiente que fue necesario para la alineación natural; por lo tanto, no solo la estructura se alinea ahora en 2, sino que también se reduce el tamaño de 8 a 6.

Como ejemplo, considere un tipo compuesto compuesto por un carácter de 1 byte, un entero de 4 bytes de longitud y un carácter de 1 byte:

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

Esta estructura se alinea de forma natural en 4 y tiene el tamaño natural de 12.

En el nivel de empaquetado 4 o superior, **la estructura se** alinea en 4 y `sizeof(struct mystructtype)` es igual a 12. La estructura no se alineará correctamente si se encuentra en la memoria en una dirección que no sea múltiplo de 4.

Para el nivel de empaquetado 2, la estructura se alinea en 2 y su tamaño es 8. La estructura empaquetada con el nivel 2 se alineará incorrectamente si se encuentra en la memoria en una dirección que no sea múltiplo de 2.

Para el nivel de empaquetado 1, la estructura se alinea en 1 y su tamaño es 6. La estructura empaquetada con el nivel 1 se puede colocar en cualquier parte sin que se produzca un error de alineación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[/ZP](./-zp.md)
</dt> <dt>

[/Pack](./-pack.md)
</dt> </dl>

 

 