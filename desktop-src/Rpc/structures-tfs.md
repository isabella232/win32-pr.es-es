---
title: Estructuras (RPC)
description: Descripción de varios tipos de estructuras en llamada a procedimiento remoto (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1783508a834ce2fa3d93d3db04edc1de362d6f888c29511c1eb6852cce0e83ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017415"
---
# <a name="structures-rpc"></a>Estructuras (RPC)

Hay varias categorías de estructuras, cada vez más complicadas en cuanto a las acciones necesarias para serializar. Comienzan con una estructura simple que se puede copiar en bloque como un todo y continúan con una estructura compleja que debe atenderse campo por campo.

-   [Estructura simple](#simple-structure)
-   [Estructura simple con punteros](#simple-structure-with-pointers)
-   [Estructura compatible](#conformant-structure)
-   [Estructura compatible con punteros](#conformant-structure-with-pointers)
-   [Estructura variable compatible (con o sin punteros)](#conformant-varying-structure-with-or-without-pointers)
-   [Estructura dura](#hard-structure)
-   [Estructura compleja](#complex-structure)
-   [Descripción del diseño de miembros de estructura](#structure-member-layout-description)

> [!Note]  
> En comparación con las categorías de matriz, queda claro que solo se pueden describir estructuras de hasta 64 000 de tamaño (el tamaño es para la parte plana de la estructura), es decir, no hay ningún equivalente de matrices SM y LG.

 

**Miembros comunes a estructuras**

-   **Alineación**

    Alineación necesaria del búfer antes de desmarque la estructura. Los valores válidos son 0, 1, 3 y 7 (la alineación real menos 1).

-   **tamaño de \_ memoria**

    Tamaño de la estructura en memoria en bytes; para las estructuras compatibles, este tamaño no incluye el tamaño de la matriz.

-   **desplazamiento \_ a la descripción de la \_ \_ matriz**

    Desplazamiento desde el puntero de cadena de formato actual a la descripción de la matriz compatible contenida en una estructura .

-   **diseño \_ de miembro**

    Descripción de cada elemento de la estructura. Las rutinas JPEG solo necesitan examinar esta parte de la cadena de formato de un tipo si se necesita la transformación endian o si el tipo es una estructura compleja.

-   **diseño de \_ puntero**

    Consulte la [sección Diseño del](pointer-layout-tfs.md) puntero.

## <a name="simple-structure"></a>Estructura simple

Una estructura simple solo contiene tipos base, matrices fijas y otras estructuras simples. La característica principal de la estructura simple es que se puede copiar en bloque como un todo.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Estructura simple con punteros

Una estructura simple con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y otras estructuras simples con punteros. Dado que el<> solo tendrá que visitarse al realizar una conversión de endianess, se coloca al final de la descripción.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Estructura compatible

Una estructura compatible solo contiene tipos base, matrices fijas y estructuras simples, y debe contener una cadena compatible o una matriz compatible. Esta matriz podría estar contenida realmente en otra estructura compatible o estructura compatible con punteros que se incrustan en esta estructura.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Estructura compatible con punteros

Una estructura compatible con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y estructuras simples con punteros; una estructura compatible debe contener una matriz compatible. Esta matriz podría estar contenida realmente en otra estructura compatible o estructura compatible con punteros que se incrustan en esta estructura.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Estructura variable compatible (con o sin punteros)

Una estructura variable compatible solo contiene tipos simples, punteros, matrices fijas, estructuras simples y estructuras simples con punteros. una estructura que varía de conformidad debe contener una cadena compatible o una matriz de variación conforme. La cadena o matriz conformes se puede incluir realmente en otra estructura compatible o estructura compatible con punteros que se incrustan en esta estructura.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Estructura dura

La estructura dura era un concepto destinado a eliminar las penalizaciones graves relacionadas con el procesamiento de estructuras complejas. Se deriva de una observación de que una estructura compleja normalmente solo tiene una o dos condiciones que impiden la copia en bloques y, por tanto, disminuyen su rendimiento en comparación con una estructura simple. Los responsables suelen ser uniones o campos de enumeración.

Una estructura dura es una estructura que tiene una enumeración 16, relleno final en memoria o una unión como último miembro. Estos tres elementos impiden que la estructura entre en una de las categorías de estructura anteriores, que tienen una pequeña sobrecarga de interpretación y un potencial de optimización máximo, pero no la fuerzan a la categoría de estructura muy compleja.

La enumeración enum16 no debe hacer que los tamaños de memoria y cable de la estructura difiren. La estructura no puede tener ninguna matriz compatible ni punteros (a menos que sea parte de la unión); los únicos miembros permitidos son tipos base, matrices fijas y estructuras simples.

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

El desplazamiento de enumeración<campo 2> proporciona el desplazamiento desde el principio de la estructura en memoria a una enumeración16 si contiene uno; de lo contrario, el desplazamiento de enumeración \_ \_<2> campo es –1.

El tamaño de copia<2 campos> proporciona el número total de bytes de la estructura, que se pueden copiar en bloque en el búfer o desde \_ este. Este total no incluye ninguna unión final ni ningún relleno final en la memoria. Este valor también es la cantidad que el puntero de búfer debe incrementarse después de la copia.

El campo mem copy incr<2> es el número de bytes que el puntero de memoria debe incrementarse después de la copia en bloque antes de controlar cualquier unión \_ \_ final. El incremento en esta cantidad (no por el tamaño de copia<2> bytes) produce un puntero de memoria adecuado \_ a cualquier unión final.

## <a name="complex-structure"></a>Estructura compleja

Una estructura compleja es cualquier estructura que contiene uno o varios campos que impiden que la estructura se copie en bloque o para las que se debe realizar una comprobación adicional durante la serialización o la desmarque (por ejemplo, comprobaciones enlazadas en una enumeración). Los siguientes tipos de NDR se encándase en esta categoría:

-   [tipos simples:](simple-types-tfs.md)ENUM16, \_ \_ INT3264 (solo en plataformas de 64 bits), una integral con \[ [ **intervalo**](/windows/desktop/Midl/range)\]
-   relleno de alineación al final de la estructura
-   punteros de interfaz (usan un complejo incrustado)
-   punteros omitidos (que está relacionado con el atributo \[ [**ignore**](/windows/desktop/Midl/ignore) \] y el token IGNORE de \_ FC)
-   matrices complejas, matrices variables, matrices de cadenas
-   Matrices conformes multidimensionales con al menos una dimensión no fija
-   uniones
-   Elementos definidos con \[ [**transmit \_ como**](/windows/desktop/Midl/transmit-as) \] , representan \[ [**\_ como**](/windows/desktop/Midl/represent-as) \] , wire \[ [**\_ marshal**](/windows/desktop/Midl/wire-marshal) \] , user \[ [**\_ marshal**](/windows/desktop/Midl/user-marshal)\]
-   estructuras complejas insertadas
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

El tamaño de<2> campo es el tamaño de \_ la estructura en memoria, en bytes.

Si la estructura contiene una matriz compatible, el desplazamiento a la descripción de la matriz conforme<el campo 2> proporciona el desplazamiento a la descripción de la matriz conforme; de lo contrario, es \_ \_ \_ \_ cero.

Si la estructura tiene punteros, el desplazamiento al diseño del puntero<el campo 2> proporciona el desplazamiento más allá del diseño de la estructura al diseño del puntero; de lo contrario, este campo es \_ \_ \_ cero.

El diseño del<> campo de una estructura compleja se controla de forma \_ ligeramente diferente que para otras estructuras. El diseño de<> campo de una estructura compleja solo contiene descripciones de campos de puntero reales \_ en la propia estructura. Los punteros contenidos en cualquier matriz, unión o estructura incrustada no se describen en el campo de diseño de puntero de \_<> estructura compleja.

> [!Note]  
> Esto contrasta con otras estructuras, que duplican la descripción de los punteros contenidos en matrices o estructuras insertadas en su propio diseño de \_ puntero<> campo.

 

El formato del diseño de puntero de una estructura compleja también es radicalmente diferente. Dado que solo contiene descripciones de miembros de puntero reales y porque se serializa una estructura compleja y se desmarcronó un campo a la vez, el campo de diseño de puntero<> simplemente contiene la descripción del puntero de todos los miembros del \_ puntero. No hay ningún PP de FC inicial y ninguno de los diseños de puntero habituales \_ \_<> información.

## <a name="structure-member-layout-description"></a>Descripción del diseño de miembros de estructura

La descripción del diseño de una estructura contiene uno o varios de los siguientes caracteres de formato:

-   Cualquiera de los caracteres de tipo base, como FC \_ CHAR, y así sucesivamente
-   Directivas de alineación. Hay tres caracteres de formato que especifican la alineación del puntero de memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 y FC \_ ALIGNM8.
    > [!Note]  
    > También hay tokens de alineación de búfer, FC \_ ALIGNB2 a FC \_ ALIGNM8; no se usan.

     

-   Relleno de memoria. Estos se producen solo al final de la descripción de una estructura y denota el número de bytes de relleno en memoria antes de la matriz compatible en la estructura: FC STRUCTPADn, donde n es el número de bytes de \_ relleno.
-   Cualquier tipo no base incrustado (tenga en cuenta, sin embargo, que una matriz compatible nunca se produce en el diseño de la estructura). Tiene una descripción de 4 bytes:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    donde no se garantiza que el desplazamiento tenga una alineación de 2 bytes.

    el \_ panel de<1> es un relleno necesario en la memoria antes del campo complejo.

    offset \_ to description<\_ 2> es un desplazamiento de tipo relativo al tipo incrustado.

También puede haber un FC PAD antes de la finalización de FC END si es necesario para asegurarse de que la cadena de formato se alineará en un límite de 2 bytes después de \_ \_ FC \_ END.

 

 