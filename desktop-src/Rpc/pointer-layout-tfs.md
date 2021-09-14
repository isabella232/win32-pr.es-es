---
title: Diseño de puntero
description: El diseño de puntero describe los punteros de una estructura o una matriz.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161038"
---
# <a name="pointer-layout"></a>Diseño de puntero

El diseño de puntero describe los punteros de una estructura o una matriz.

## <a name="pointer_layout"></a>diseño \_ de puntero<>

Un campo de diseño<> puntero consta de los caracteres de formato FC PP FC PAD seguidos de una o varias descripciones de puntero, como se describe más adelante, y termina con un carácter de formato \_ \_ FC \_ \_ END:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Un diseño de instancia de<> campo es una cadena de formato que describe una \_ o varias instancias de \_ punteros. En estos descriptores se usan los siguientes campos:

-   desplazamiento \_ en \_ memoria

    Desplazamiento con firma a la ubicación del puntero en memoria. Para un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles); para matrices, el desplazamiento es desde el principio de la matriz.

-   desplazamiento \_ en búfer \_

    Desplazamiento con firma a la ubicación del puntero en el búfer. Para un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles): para las matrices, el desplazamiento es desde el principio de la matriz.

-   desplazamiento \_ a la \_ matriz

    Desplazamiento desde una estructura de entrada a la matriz incrustada cuyos punteros se están controlando. Para las matrices de nivel superior, este campo siempre será cero.

-   iteraciones

    Número total de punteros que tienen el mismo diseño<> descrito.

-   incremento

    Incremento entre punteros sucesivos durante repeat.

-   número \_ de \_ punteros

    Número de punteros diferentes en una instancia de repetición.

-   descripción del \_ puntero

    Descripción del puntero.

Todos los diseños de instancia de puntero usan la siguiente instancia de \_ puntero<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Los siguientes son descriptores de instancia:

**Instancia única de un puntero a un tipo simple:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Se ha corregido el puntero de repetición:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Puntero de repetición de variable:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

En el caso de las instancias de puntero de repetición fija y de repetición variable, hay un conjunto de descripciones de desplazamiento y puntero para cada puntero de la instancia de repetición.

## <a name="pointers-layout-design-issues"></a>Problemas de diseño de punteros

En esta sección se abordan los problemas relacionados con el procesamiento de estructuras compatibles y punteros incrustados. El problema es que el compilador genera diseños de puntero para estructuras y matrices con cierta redundancia. Esto es beneficioso, porque la información es útil y, como tal, por ejemplo, una estructura compatible puede recorrer un diseño de puntero para dar servicio a todos los punteros de la estructura y de la matriz compatible que forma parte de la estructura compatible. Sin embargo, existen algunas situaciones incrustadas que requieren que el motor PLACE realice trabajo adicional para procesar todos los diseños de puntero en la secuencia adecuada, procesando cada puntero exactamente una vez.

## <a name="what-the-compiler-generates"></a>Qué genera el compilador

Cada objeto que se describe en esta sección tiene punteros, por lo que, por ejemplo, una estructura compatible tiene punteros en la parte de la estructura, así como en los elementos de la matriz. El elemento es una estructura simple con un puntero.

1.  Estructura compatible, nivel único

    El descriptor compatible tiene una parte pp donde se describen todos los punteros, tanto de la estructura como de la matriz. La lista de miembros tiene FC \_ LONG en lugar de un puntero. El descriptor de matriz CARRAY tiene elementos mediante el uso de un complejo incrustado \_ y ningún descriptor de puntero. El elemento todavía tiene su descriptor de puntero único. El diseño de puntero precede al diseño de miembro en una estructura compatible y descriptores de estructura simples.

2.  Estructura compatible, dos o más niveles

    La descripción de PP tiene punteros de todos los niveles. Reutiliza la misma descripción de la matriz que la estructura conforme interna. La lista de miembros tiene FC \_ LONG en lugar de un puntero. Una estructura incrustada pasa por el uso de un complejo incrustado. El descriptor de estructura compatible se reutiliza tal y como está. El tamaño de la parte plana de la estructura también se completa, lo que significa que el tamaño de la estructura de nivel superior incluiría el tamaño plano de la estructura insertada.

3.  Estructura compleja, nivel único

    Los miembros de puntero están marcados por FC \_ POINTER. El diseño del puntero se simplifica de forma que hay un descriptor de puntero (4 bytes) para cada entrada \_ DE PUNTERO FC en la lista. El diseño del puntero se pasea en paralelo con un recorrido de miembro, es decir, un PUNTERO FC hace que se procese la \_ siguiente descripción del puntero. La matriz CARRAY tiene un diseño de puntero con todos los descriptores de la matriz y, a continuación, el elemento , mediante el uso de un complejo incrustado. Se reutiliza el descriptor de elemento. El tamaño de la parte plana de la estructura aparece completo; En otras palabras, el tamaño plano de la estructura de nivel superior incluye el tamaño plano de la estructura insertada. El diseño de miembro precede al diseño de puntero para estructuras complejas.

    Por lo tanto, la generación de descripción de matriz compatible es diferente en función de si se trata de una matriz dentro de una estructura compatible o dentro de una estructura compleja.

4.  Estructura compleja, 2 o más niveles, compleja en compleja

    La estructura compleja de nivel superior tiene sus punteros de miembro, la estructura compleja incrustada tiene sus punteros de miembro. Se reutiliza el descriptor de estructura compatible. El descriptor de matriz de la parte superior es la matriz reutilizada de la estructura insertada.

5.  Estructura compleja con una estructura conforme insertada

    La estructura compatible de nivel superior tiene sus punteros de miembro. El descriptor de estructura compatible se reutiliza tal y como está. El descriptor de matriz se reutiliza a partir de la estructura conforme incrustada; en otras palabras, no tiene punteros en el descriptor de matriz. El elemento tiene su descriptor de puntero.

6.  Matrices de estructuras con punteros

    Una matriz de estructuras simples con punteros se genera como SMFARRAY o CARRAY dependiendo de si la matriz tiene un tamaño, pero en ambos casos tiene un diseño de puntero completo (FIXED REPEAT o \_ VARIABLE \_ REPEAT). El diseño del puntero está delante del diseño de miembro.

    Una matriz de estructuras complejas con punteros se genera como ARRAY DEUSUS independientemente de si es fija o de tamaño y, en ambos casos, no tiene ningún diseño \_ de puntero.

## <a name="what-the-ndr-engine-does"></a>Qué hace el motor de BAND

En esta sección se describe el comportamiento del motor BAND.

**Paso de serialización**

1.  Estructuras compatibles y estructura conforme insertada.

    La estructura de nivel superior se comporta como una estructura de un solo nivel.

2.  Estructura compleja insertada con matriz compatible

    Cualquier estructura compleja obliga a la estructura externa a ser una estructura compleja. La estructura incrustada nunca serializa su matriz. Cada estructura siempre pasa por punteros incrustados simplemente serializando miembros y un miembro que pasa a ser un PUNTERO \_ FC.

3.  Estructura compleja con estructura compatible

    La estructura conforme de la parte superior incrustada serializa la matriz compatible y todos los estados. El motor LEJOS nunca desciende a estructuras conformes anidadas más profundas, si las hay; Esto simplifica la solución, ya que una estructura compatible es un objeto hoja en lo que respecta a la serialización de objetos incrustados. La estructura compleja de nivel superior omite la serialización de matriz.

**Desmarque, evolucione y liberar pases**

La desmarque es simétrica a la serialización; La primera operación que realiza para estructuras complejas es averiguar la ubicación de los destinos en el búfer mediante una llamada a la **función ComposiciónComplexStructBufferSize.** A continuación, desmarshals los sentidos en paralelo, lo que permite usar el mismo esquema para desmarque las ramas correctamente. No debería haber confusión sobre los objetos de tamaño y las uniones. La imagen de memoria no debe usarse para objetos de tamaño y uniones, solo para el contenido del búfer.

Las marcas que se usan para realizar correctamente la serialización y la desmarque se usan de la misma manera en la operación de cambios y desenlazamiento para asegurarse de que los árboles se pasen exactamente una vez.

**Paso de endianess**

Al principio, el paso de endianess es algo similar a serializar o desmarque. Se requieren dos pases para procesar estructuras complejas. El primer paso convierte la parte plana y encuentra la ubicación de los árboles en el búfer de forma similar a la que realiza esta operación para desmarque. A continuación, el segundo paso convierte los contraversos.

Los pasos de endianess difieren de la manera siguiente: cada estructura y cada miembro debe escalonarse hasta que el miembro o elemento hoja sea un tipo simple. Esto es diferente de la desmarque; en la desmarque, por ejemplo, nunca es necesario procesar estructuras compatibles incrustadas en estructuras conformes, ni ningún miembro de la estructura compatible, en ese caso. Otro problema es que la conversión no es una operación idempotente, por lo que el paso de desmarque podría rehacer la desmarque de algunas piezas sin daños, mientras que la conversión se debe realizar estrictamente una vez por cada tipo simple.

Por lo tanto, el algoritmo de endianess se puede resumir como se muestra a continuación. BAND tiene una noción de la estructura compatible de nivel superior y una marca para marcarla, según corresponda. Al recorrer la primera vez, por ejemplo, para convertir la parte plana y obtener la ubicación de los nociones, no se usaría esta noción. MOUSE bajaría a través de las partes planas de todos los niveles de estructuras y nunca entraría en el procesamiento de punteros. Por último, CONVERT convertiría sin formato la matriz en el nivel superior.

Al recorrer la segunda vez, la marca se usaría para marcar el paso del puntero incrustado para evitar entrar en niveles más profundos de las estructuras compatibles y, a continuación, la estructura más compatible. De esta manera, la marca forzaría el comportamiento común de serialización o desmarque, que es evitar la degradación a niveles más profundos de estructuras compatibles.

El segundo paso para estructuras complejas con matrices compatibles funciona de la siguiente manera: las estructuras complejas funcionan de la manera común; lo que significa que los niveles más profundos nunca verían ni omitirían su tamaño de conformidad o sus matrices compatibles, y prefieren simplemente recorrer sus miembros sin tocar la matriz.

En el caso de estructuras complejas con estructuras compatibles, la estructura compatible debe tener en cuenta si es de nivel superior y si está en una estructura compleja. La parte plana de la matriz se procesa mediante la estructura de mayor conformidad. En el segundo paso, la estructura compatible de nivel superior omitiría la parte plana y pasará por el diseño del puntero y la devolución. La estructura superior más compleja omitiría su parte plana y también omitiría el diseño del puntero.

**Aspecto sólido de los paseos por la endianess**

El recorrido de endianess comprueba las condiciones habituales fuera del búfer y realiza otras comprobaciones de una naturaleza no relacionada. Las comprobaciones dirigidas a valores correlacionados (como el argumento de ajuste de tamaño frente al tamaño compatible) no se pueden realizar mediante este paso; se realizan más adelante, cuando se desmarque.

 

 




