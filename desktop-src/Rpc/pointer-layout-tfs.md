---
title: Diseño de puntero
description: El diseño de puntero describe los punteros de una estructura o una matriz.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903721"
---
# <a name="pointer-layout"></a>Diseño de puntero

El diseño de puntero describe los punteros de una estructura o una matriz.

## <a name="pointer_layout"></a><> de diseño de puntero \_

Un \_<> campo de diseño de puntero consta de los caracteres de formato FC \_ PP FC \_ Pad seguido de una o varias descripciones de puntero, como se describe más adelante, y terminando con un \_ carácter de formato final de FC:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Un \_ \_<> campo de diseño de instancia de puntero es una cadena de formato que describe una o varias instancias de punteros. En estos descriptores se utilizan los campos siguientes:

-   desplazamiento \_ en \_ memoria

    Desplazamiento con signo de la ubicación del puntero en la memoria. En el caso de un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles); en el caso de las matrices, el desplazamiento es desde el principio de la matriz.

-   desplazamiento \_ en \_ búfer

    Desplazamiento con signo en la ubicación del puntero en el búfer. En el caso de un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles): para las matrices, el desplazamiento es desde el principio de la matriz.

-   desplazamiento \_ a la \_ matriz

    Desplazamiento de una estructura envolvente a la matriz incrustada cuyos punteros se están controlando. En el caso de las matrices de nivel superior, este campo siempre será cero.

-   iteraciones

    Número total de punteros que tienen el mismo diseño<> describe.

-   incremento

    Incremento entre punteros sucesivos durante una repetición.

-   número \_ de \_ punteros

    Número de punteros diferentes en una instancia de repetición.

-   Descripción del puntero \_

    Descripción del puntero.

Todos los diseños de instancia de puntero utilizan la siguiente instancia de puntero único \_<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Los descriptores de instancia son los siguientes:

**Instancia única de un puntero a un tipo simple:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Puntero de repetición fijo:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Puntero de repetición variable:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

En el caso de las instancias de repetición fija y de puntero de repetición variable, hay un conjunto de descripciones de desplazamiento y puntero para cada puntero en la instancia de repetición.

## <a name="pointers-layout-design-issues"></a>Problemas de diseño del diseño de punteros

En esta sección se abordan los problemas relacionados con el procesamiento de estructuras y punteros incrustados. El problema es que el compilador genera diseños de puntero para estructuras y matrices con cierta redundancia. Esto es beneficioso, porque la información es útil y, por ejemplo, una estructura compatible puede recorrer un diseño de puntero para atender todos los punteros de la estructura y de la matriz compatible que forma parte de la estructura compatible. Sin embargo, existen algunas situaciones incrustadas que requieren que el motor NDR realice trabajo adicional para procesar todos los diseños de puntero en la secuencia adecuada, procesando cada puntero exactamente una vez.

## <a name="what-the-compiler-generates"></a>Lo que genera el compilador

Cada objeto descrito en esta sección tiene punteros, por lo que, por ejemplo, una estructura compatible tiene punteros en la parte de la estructura, así como en los elementos de la matriz. El elemento es una estructura simple con un puntero.

1.  Estructura compatible, nivel único

    El descriptor compatible tiene una parte PP donde se describen todos los punteros, tanto de la estructura como de la matriz. La lista de miembros tiene \_ un valor FC largo en lugar de un puntero. El descriptor de la matriz CARRAy tiene elementos mediante el uso de un complejo incrustado \_ y ningún descriptor de puntero. El elemento todavía tiene su descriptor de puntero único. El diseño de puntero precede al diseño de miembro en una estructura compatible y descriptores de estructura simples.

2.  Estructura compatible, dos o más niveles

    La descripción de PP tiene punteros de todos los niveles. Reutiliza la misma descripción de la matriz que la estructura compatible interna. La lista de miembros tiene \_ un valor FC largo en lugar de un puntero. Una estructura incrustada se refiere al uso de un complejo incrustado. El descriptor de estructura compatible se reutiliza tal cual. El tamaño de la parte plana de la estructura también viene completo, lo que significa que el tamaño de la estructura de nivel superior incluiría el tamaño plano de la estructura insertada.

3.  Estructura compleja, de un solo nivel

    Los miembros de puntero se marcan mediante el \_ puntero FC. El diseño de puntero se simplifica de manera que hay un descriptor de puntero (4 bytes) para cada \_ entrada de puntero FC en la lista. El diseño de puntero se recorre en paralelo con un recorrido de miembro, es decir, un \_ puntero FC hace que se procese la siguiente descripción del puntero. La matriz CARRAy tiene un diseño de puntero con todos los descriptores de la matriz y, a continuación, el elemento, mediante el uso de un complejo incrustado. El descriptor de elemento se reutiliza. El tamaño de la parte plana de la estructura viene completo; en otras palabras, el tamaño plano de la estructura de nivel superior incluye el tamaño plano de la estructura insertada. El diseño de miembro precede al diseño de puntero para estructuras complejas.

    Por lo tanto, la generación de la descripción de la matriz compatible es diferente en función de si se trata de una matriz dentro de una estructura compatible o dentro de una estructura compleja.

4.  Estructura compleja, 2 o más niveles, complejo en complejo

    La estructura compleja de nivel superior tiene sus punteros de miembro, la estructura compleja incrustada tiene sus punteros de miembro. Se reutiliza el descriptor de estructura compatible. El descriptor de matriz de la parte superior es la matriz reutilizada de la estructura insertada.

5.  Estructura compleja con una estructura compatible incrustada

    Top = la estructura compatible con el nivel tiene sus punteros de miembro. El descriptor de estructura compatible se reutiliza tal cual. El descriptor de matriz se reutiliza de la estructura compatible con incrustación; en otras palabras, no tiene punteros en el descriptor de la matriz. El elemento tiene su descriptor de puntero.

6.  Matrices de estructuras con punteros

    Una matriz de estructuras simples con punteros se genera como SMFARRAY o CARRAy dependiendo de si la matriz tiene un tamaño, pero en ambos casos tiene un diseño de puntero que se completa ( \_ repetición fija o repetición de variables \_ ). El diseño del puntero viene antes del diseño de los miembros.

    Una matriz de estructuras complejas con punteros se genera como una \_ matriz ficticia, independientemente de si está fija o tiene un tamaño, y en ambos casos, no tiene ningún diseño de puntero.

## <a name="what-the-ndr-engine-does"></a>Qué hace el motor NDR

En esta sección se describe el comportamiento del motor NDR.

**El paso de cálculo de referencias**

1.  Estructuras compatibles y estructura compatible con Embedded.

    La estructura de nivel superior se comporta como una estructura de un solo nivel.

2.  Estructura compleja incrustada con matriz compatible

    Cualquier estructura compleja obliga a que la estructura exterior sea una estructura compleja. La estructura insertada nunca calcula las referencias de su matriz. Cada estructura siempre pasa por los punteros incrustados mediante la simple serialización de los miembros y un miembro que está pasando a ser un \_ puntero FC.

3.  Estructura compleja con estructura compatible

    La estructura compatible con el nivel superior incrustado calcula las referencias de la matriz compatible y de todos los punteros. El motor NDR nunca desciende hasta estructuras compatibles de anidación más profundas si hay alguna; Esto simplifica la solución, ya que la estructura compatible es un objeto hoja en lo que respecta a la serialización de objetos incrustados. La estructura compleja de nivel superior omite la serialización de la matriz.

**Desserialización, bufsizing y liberación de pasos**

La anulación de la serialización es simétrica al cálculo de referencias; la primera operación que realiza para estructuras complejas es encontrar la ubicación de los punteros en el búfer mediante una llamada a la función **NdrComplexStructBufferSize** . A continuación, se anulan las referencias de los punteros en paralelo, lo que permite que el mismo esquema calcule las referencias de los punteros correctamente para su uso. No debe haber ninguna confusión sobre los objetos y uniones de tamaño; la imagen de memoria no debe usarse para objetos y uniones con tamaño, solo para el contenido del búfer.

Las marcas que se usan para realizar la serialización y la desserialización correctamente se usan de la misma manera en bufsizing y liberan para asegurarse de que los punteros se recorren exactamente una vez.

**Orden Pass**

Al principio, el paso orden es algo similar a la serialización o la anulación de la serialización; se requieren dos pasos para procesar estructuras complejas. El primer paso convierte la parte plana y busca la ubicación de los punteros en el búfer de forma similar a como bufsizing realiza esta operación para la anulación de la serialización. A continuación, el segundo paso convierte los punteros.

Las pasadas orden difieren de la siguiente manera: cada estructura y cada miembro tiene que ser escalonado hasta que el miembro hoja o el elemento sea un tipo simple. Esto no es lo mismo que quitar las referencias. en el caso de la desserialización, por ejemplo, nunca es necesario procesar las estructuras compatibles incrustadas en estructuras compatibles, o cualquier miembro de la estructura compatible, para ese propósito. Otro problema es que la conversión no es una operación idempotente; por lo tanto, el paso de desserialización podría rehacer la anulación de la serialización de algunas partes sin daños, mientras que la conversión se debe realizar en una base de tipo estrictamente una vez por tipo simple.

Por lo tanto, el algoritmo orden se puede resumir como sigue. NDR tiene una noción de la estructura compatible de nivel superior y una marca para marcarla, según corresponda. Al caminar por primera vez, por ejemplo, para convertir la parte plana y obtener la ubicación de los punteros, esta noción no se utilizaría. NDR desaparecerá a través de las partes planas de todos los niveles de estructuras y nunca al procesamiento de punteros. Por último, el NDR tendría que convertir la matriz en el nivel superior.

Al recorrer la segunda vez, la marca se utilizaría para marcar el paso del puntero incrustado a fin de evitar que se escriban niveles más profundos de las estructuras compatibles y, después, la estructura compatible con el nivel superior. De esta manera, la marca forzaría el comportamiento común de serialización y desserialización, lo que es evitar descender en niveles más profundos de estructuras conformes.

El segundo paso para estructuras complejas con matrices compatibles funciona de la siguiente manera: las estructuras complejas funcionan de la manera habitual. lo que significa que los niveles más profundos nunca verían o omitirían su tamaño compatible o sus matrices compatibles, y en su lugar simplemente irían a sus miembros sin tocar la matriz.

En el caso de las estructuras complejas con estructuras compatibles, la estructura compatible debe ser consciente de si es de nivel superior y si está en una estructura compleja. La parte plana de la matriz se procesa mediante la estructura compatible de nivel superior. En el segundo paso, la estructura compatible con el nivel superior omitiría la parte plana y pasará por el diseño del puntero y devolverá. La estructura más compleja de nivel superior omitiría su parte plana y omitiría también el diseño del puntero.

**El aspecto sólido de los recorridos de orden**

El recorrido de orden comprueba las condiciones habituales del búfer y realiza otras comprobaciones de una naturaleza no correlacionada. Las comprobaciones dirigidas a los valores correlacionados (como el argumento de ajuste de tamaño frente al tamaño compatible) no se pueden realizar con este paso. se realizan posteriormente, cuando se anula el cálculo de referencias.

 

 




