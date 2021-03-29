---
title: Estructuras (RPC)
description: Descripción de varios tipos de estructuras en llamada a procedimiento remoto (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078097"
---
# <a name="structures-rpc"></a>Estructuras (RPC)

Hay varias categorías de estructuras, progresivamente más complicadas en cuanto a las acciones necesarias para calcular las referencias. Comienzan con una estructura simple que se puede copiar en bloque en su totalidad y continuar con una estructura compleja que tiene que ser servicio campo por campo.

-   [Estructura simple](#simple-structure)
-   [Estructura simple con punteros](#simple-structure-with-pointers)
-   [Estructura compatible](#conformant-structure)
-   [Estructura compatible con punteros](#conformant-structure-with-pointers)
-   [Estructura variable compatible (con o sin punteros)](#conformant-varying-structure-with-or-without-pointers)
-   [Estructura rígida](#hard-structure)
-   [Estructura compleja](#complex-structure)
-   [Descripción del diseño del miembro de estructura](#structure-member-layout-description)

> [!Note]  
> Cuando se comparan con las categorías de matriz, queda claro que solo se pueden describir las estructuras de hasta 64 KB de tamaño (el tamaño es para la parte plana de la estructura), es decir, no hay equivalentes de las matrices SM y LG.

 

**Miembros comunes a las estructuras**

-   **ecuación**

    La alineación necesaria del búfer antes de calcular las referencias de la estructura. Los valores válidos son 0, 1, 3 y 7 (la alineación real menos 1).

-   **tamaño de memoria \_**

    Tamaño de la estructura en memoria en bytes; en el caso de las estructuras compatibles, este tamaño no incluye el tamaño de la matriz.

-   **desplazamiento \_ a la descripción de la \_ matriz \_**

    Desplazamiento desde el puntero de cadena de formato actual a la descripción de la matriz compatible incluida en una estructura.

-   **diseño de miembros \_**

    Descripción de cada elemento de la estructura. Las rutinas de NDR solo necesitan examinar esta parte de la cadena de formato de un tipo si se necesita la transformación endian o si el tipo es una estructura compleja.

-   **diseño de puntero \_**

    Vea la sección de [diseño de puntero](pointer-layout-tfs.md) .

## <a name="simple-structure"></a>Estructura simple

Una estructura simple solo contiene tipos base, matrices fijas y otras estructuras simples. La característica principal de la estructura simple es que se puede copiar en bloque en su totalidad.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Estructura simple con punteros

Una estructura simple con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y otras estructuras simples con punteros. Dado que el diseño<> solo tendrá que visitarse al realizar una conversión orden, se coloca al final de la descripción.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Estructura compatible

Una estructura compatible solo contiene los tipos base, las matrices fijas y las estructuras simples, y debe contener una cadena compatible o una matriz compatible. En realidad, esta matriz puede estar contenida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Estructura compatible con punteros

Una estructura compatible con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y estructuras simples con punteros. una estructura compatible debe contener una matriz compatible. En realidad, esta matriz puede estar incluida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Estructura variable compatible (con o sin punteros)

Una estructura variable compatible solo contiene tipos simples, punteros, matrices fijas, estructuras simples y estructuras simples con punteros. una estructura variable ajustada debe contener una cadena compatible o una matriz de variación compatible. En realidad, la matriz o cadena compatible puede estar contenida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Estructura rígida

La estructura de hardware era un concepto destinado a eliminar penalizaciones dependientes relacionadas con el procesamiento de estructuras complejas. Se deriva de una observación de que una estructura compleja normalmente solo tiene una o dos condiciones que impiden la copia de bloques y, por lo tanto, se estropea su rendimiento en comparación con una estructura simple. Los culpable suelen ser uniones o campos de enumeración.

Una estructura rígida es una estructura que tiene un enum16, un relleno en memoria o una Unión como último miembro. Estos tres elementos impiden que la estructura caiga en una de las categorías de estructura anteriores, que disfrutan de una pequeña sobrecarga de interpretación y una posible optimización máxima, pero no la fuerzan en la categoría de estructura muy compleja.

Enum16 no debe hacer que los tamaños de memoria y de conexión de la estructura difieran. La estructura no puede tener ninguna matriz compatible ni ningún puntero (a menos que forme parte de la Unión). los únicos miembros permitidos son los tipos base, las matrices fijas y las estructuras simples.

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

El campo de desplazamiento de enumeración \_<2> proporciona el desplazamiento desde el principio de la estructura en memoria hasta un enum16 si contiene uno; de lo contrario, el desplazamiento de enumeración \_<2> campo es – 1.

El \_ campo Copy size<2> proporciona el número total de bytes de la estructura, que se pueden copiar en bloque en el búfer o desde él. Este total no incluye ninguna unión final ni ningún relleno en la memoria. Este valor también es la cantidad con la que se debe incrementar el puntero de búfer después de la copia.

El \_ \_ campo de> copiar incr<2 es el número de bytes que debe incrementar el puntero de memoria después de la copia de bloques antes de controlar cualquier unión final. Si se incrementa en esta cantidad (no en \_ el tamaño de copia<2> bytes), se produce un puntero de memoria adecuado a cualquier unión final.

## <a name="complex-structure"></a>Estructura compleja

Una estructura compleja es cualquier estructura que contenga uno o más campos que impidan que la estructura se copie en bloque o para la que se debe realizar una comprobación adicional durante el cálculo de referencias o la anulación de la serialización (por ejemplo, comprobaciones enlazadas en una enumeración). Los siguientes tipos de NDR se encuentran en esta categoría:

-   [tipos simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (solo en plataformas de 64 bits), un entero con \[ [ **rango**](/windows/desktop/Midl/range)\]
-   relleno de alineación al final de la estructura
-   punteros de interfaz (se usan con un complejo incrustado)
-   punteros omitidos (que están relacionados con el \[ atributo [**Ignore**](/windows/desktop/Midl/ignore) \] y el \_ token ignore de FC)
-   matrices complejas, matrices variables, matrices de cadenas
-   matrices compatibles multidimensionales con al menos una dimensión no fija
-   uniones
-   elementos definidos con \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**representar \_ como**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ serialización de conexión**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ serialización de usuario**](/windows/desktop/Midl/user-marshal)\]
-   estructuras complejas incrustadas
-   relleno al final de la estructura

Una estructura compleja tiene la siguiente descripción de formato:

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

El \_ campo tamaño de memoria<2> es el tamaño de la estructura en memoria, en bytes.

Si la estructura contiene una matriz compatible, el desplazamiento a la \_ \_ \_ \_ descripción de matriz compatible<2> campo proporciona el desplazamiento a la descripción de la matriz compatible; en caso contrario, es cero.

Si la estructura tiene punteros, el desplazamiento \_ al \_ diseño de puntero \_<2> campo proporciona el desplazamiento más allá del diseño de la estructura al diseño del puntero; de lo contrario, este campo es cero.

El \_ diseño de puntero<> campo de una estructura compleja se controla de forma ligeramente diferente que para otras estructuras. El \_ campo<> de diseño de puntero de una estructura compleja solo contiene descripciones de los campos de puntero reales de la propia estructura. Los punteros contenidos en las matrices, uniones o estructuras incrustadas no se describen en el campo<> de diseño de punteros de la estructura compleja \_ .

> [!Note]  
> Esto contrasta con otras estructuras, que duplican la descripción de los punteros contenidos en matrices o estructuras incrustadas en su propio diseño de puntero \_<> campo también.

 

El formato de la distribución de punteros de una estructura compleja también es radicalmente diferente. Dado que solo contiene descripciones de los miembros de puntero reales y porque se calculan las referencias de una estructura compleja y se anula la serialización de un campo cada vez, el \_ diseño de puntero<> campo contiene simplemente la descripción del puntero de todos los miembros de puntero. No se inicia FC \_ PP y ninguno de los diseños de puntero habituales \_<> información.

## <a name="structure-member-layout-description"></a>Descripción del diseño del miembro de estructura

La descripción del diseño de una estructura contiene uno o varios de los siguientes caracteres de formato:

-   Cualquiera de los caracteres de tipo base, como FC \_ Char, etc.
-   Directivas de alineación. Hay tres caracteres de formato que especifican la alineación del puntero de memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 y FC \_ ALIGNM8.
    > [!Note]  
    > También hay tokens de alineación de búfer, FC \_ ALIGNB2 a través de FC \_ ALIGNM8; no se usan.

     

-   Relleno de memoria. Esto solo se produce al final de la descripción de una estructura y denota el número de bytes de relleno en la memoria antes de la matriz compatible en la estructura: FC \_ STRUCTPADn, donde n es el número de bytes de relleno.
-   Cualquier tipo no base incrustado (tenga en cuenta, sin embargo, que una matriz compatible nunca se produce en el diseño de la estructura). Tiene una descripción de 4 bytes:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    donde no se garantiza que el desplazamiento tenga una alineación de 2 bytes.

    \_el controlador de memoria<1> es un relleno necesario en la memoria antes del campo complejo.

    offset \_ to \_ description<2> es un desplazamiento de tipo relativo al tipo incrustado.

También puede haber un controlador FC \_ antes del extremo FC de terminación \_ , si es necesario, para asegurarse de que la cadena de formato se alineará en un límite de 2 bytes después del final de FC \_ .

 

 