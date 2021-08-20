---
title: Problemas de empaquetado del compilador de C
description: Los niveles de empaquetado afectan al diseño de memoria de los tipos tanto para MIDL como para el compilador de Microsoft C/C++ de la misma manera.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL del compilador MIDL, problemas de empaquetado del compilador de C
- empaquetado de MIDL
- MIDL de diseño de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d355214c7f3222d67fd7673de4f9d32d19b4c885e8f97143c80df7b98bc0e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807898"
---
# <a name="c-compiler-packing-issues"></a>Problemas de empaquetado del compilador de C

Los niveles de empaquetado afectan al diseño de memoria de los tipos tanto para MIDL como para el compilador de Microsoft C/C++ de la misma manera. En entornos de compilación de Microsoft, como el entorno de compilación definido por VC++ o el Kit de desarrollo de software de plataforma (SDK), el nivel de empaquetado predeterminado para los compiladores MIDL y C/C++ es el mismo; El nivel de empaquetado predeterminado para los entornos de compilación de 32 y 64 Windows bits es 8.

## <a name="natural-alignment"></a>Alineación natural

Para los tipos en memoria, la alineación predeterminada es la misma que la alineación natural.

-   Un tipo base, como short, float e \_ int64, y un puntero se alinean de forma natural si su representación comienza en una dirección que es \_ módulo de su tamaño. Todos los tipos base admitidos actualmente tienen tamaños de 1, 2, 4 u 8. Los punteros tienen un tamaño de 4 en entornos de 32 bits y de 8 en entornos de 64 bits.
-   Un tipo compuesto se alinea de forma natural si cada uno de sus componentes se alinea de forma natural con respecto al principio del tipo y si no hay espacios innecesarios (relleno) entre los componentes. Los componentes compuestos, como campos o elementos, se repiten en los componentes de puntero o de tipo base.

Una regla sencilla para ayudar a recordar este comportamiento es que la alineación natural de un tipo es igual a las alineaciones más grandes de sus componentes.

Hay una conexión entre la alineación y el tamaño de memoria de un tipo en lenguajes como C o C++ e IDL tal como se expresa mediante el **operador sizeof().** El tamaño es un múltiplo de la alineación (el múltiplo mínimo que abarca el tipo). Esto se debe a una representación de matriz en memoria.

La alineación natural es importante porque el acceso a datos mal alineados puede provocar una excepción en algunos sistemas. Los datos se pueden marcar para una manipulación segura cuando no están alineados, pero normalmente eso implica una reducción de la velocidad que puede ser considerable en algunas plataformas.

> [!Note]  
> En memoria, se garantiza que los objetos de tipos con una alineación natural de *n* se alinean correctamente cuando se colocan en direcciones que son un múltiplo de *n*.

 

## <a name="packing-versus-alignment"></a>Empaquetado frente a alineación

La especificación de un nivel de empaquetado mayor que la alineación natural de un tipo no cambia la alineación de tipos. Si se especifica un nivel de empaquetado menor que la alineación natural, se reduce la alineación del tipo al nivel de empaquetado. Como resultado, los tipos empaquetados se pueden colocar en memoria en direcciones que son un múltiplo del nivel de empaquetado (la alineación reducida) sin provocar una desalineación. Esto afecta tanto a los tipos simples como a los tipos de componente. En el caso de los tipos compuestos, el diseño interno del tipo puede verse afectado, ya que la alineación reducida de los componentes puede cambiar el tamaño del relleno necesario para la alineación adecuada de los componentes, lo que reduce el tamaño del tipo.

Una regla sencilla para ayudar a recordar este comportamiento es que la nueva alineación de un tipo empaquetado es la más pequeña del nivel de empaquetado y su alineación natural. El tamaño del tipo es un múltiplo de la nueva alineación. El **operador sizeof()** devuelve el tamaño reducido para los tipos empaquetados.

Por ejemplo, con el nivel de empaquetado 2, un largo se alinea en 2 y, por tanto, se puede colocar en cualquier dirección uniforme, no solo en las direcciones que son un múltiplo de 4, como sería el caso de alineación natural. Una estructura con un corto y un largo, empaquetados en 2, no necesita la brecha interna entre el corto y el siguiente largo necesario para la alineación natural; por lo tanto, no solo la estructura ahora está alineada en 2, sino que también tiene su tamaño reducido de 8 a 6.

Por ejemplo, considere un tipo compuesto que consta de un carácter de 1 byte, un entero de 4 bytes de longitud y un carácter de 1 byte:

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

Para el nivel de empaquetado 4 o superior, la **estructura mystruct** se alinea en 4 y `sizeof(struct mystructtype)` es igual a 12. La estructura se alineará mal si se encuentra en la memoria en una dirección que no es un múltiplo de 4.

Para el nivel de empaquetado 2, la estructura se alinea en 2 y su tamaño es 8. La estructura empaquetada con el nivel 2 estará mal alineada si se encuentra en memoria en una dirección que no es un múltiplo de 2.

Para el nivel de empaquetado 1, la estructura se alinea en 1 y su tamaño es 6. La estructura empaquetada con el nivel 1 se puede colocar en cualquier lugar sin provocar un error de alineación errónea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[/Zp](./-zp.md)
</dt> <dt>

[/pack](./-pack.md)
</dt> </dl>

 

 