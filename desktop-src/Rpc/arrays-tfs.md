---
title: Matrices (RPC) (TFS)
description: Las categorías de matriz de llamada a procedimiento remoto (RPC) incluyen tamaño fijo, compatible, variable, variable y compleja.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073495"
---
# <a name="arrays-rpc"></a>Matrices (RPC)

Se han definido varias categorías de matriz en función de sus características de rendimiento, principalmente si la matriz se puede copiar en bloque.

Para algunas categorías, como una matriz de tamaño fijo, existen dos tipos de descriptores de matriz; se indican mediante una corrección en el nombre del token de FC inicial.



| Carácter de formato | Descripción                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | El tamaño total del tipo se puede representar en un entero de 16 bits sin signo.    |
| LG               | El tamaño total del tipo necesita una longitud de 32 bits sin signo para representarse. |



 

Campos comunes a las matrices:

-   tamaño \_ total

    Tamaño total de la matriz en memoria, en bytes. Esto es lo mismo que el tamaño del cable después de la alineación. El tamaño total se calcula para las categorías para las que el problema de relleno no existe y el tamaño es el tamaño real de la matriz.

-   tamaño de \_ elemento

    Tamaño total en memoria de un solo elemento de la matriz, incluido el relleno (esto puede ocurrir solo para matrices complejas).

-   Descripción del \_ elemento

    Descripción del tipo de elemento de matriz.

-   diseño de \_ puntero

    Vea el [tema Diseño de](pointer-layout-tfs.md) puntero para obtener más información.

## <a name="fixed-sized-arrays"></a>Matrices de tamaño fijo

Se genera una cadena de formato de matriz de tamaño fijo para las matrices que tienen un tamaño conocido y, por tanto, se pueden copiar en bloque en el búfer de serialización. Los dos formatos de descriptor de matriz fijos son los siguientes.

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

y

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>Matriz compatible

Una matriz compatible se puede copiar en bloque una vez que se conoce el tamaño de la matriz.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

La descripción de conformidad<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ si [**se usa /robust.**](/windows/desktop/Midl/-robust)

## <a name="conformant-varying-array"></a>Matriz variable compatible

También se puede copiar en bloque una matriz variable compatible.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

La descripción de conformidad<> descripción de varianza<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de si \_ \_ se usa [**/robust.**](/windows/desktop/Midl/-robust)

## <a name="varying-array"></a>Matriz variable

Las matrices variables tienen dos posibilidades en función del tamaño de la matriz.

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

La descripción de varianza<> es un descriptor de correlación y tiene 4 o 6 bytes en función del \_ [**/robust**](/windows/desktop/Midl/-robust) que se esté utilizando.

Para las matrices variables incrustadas dentro de una estructura, el campo de desplazamiento<2> de la descripción de varianza<> es un desplazamiento relativo desde la posición de la matriz variable en la estructura hasta el campo de descripción de \_ varianza. El desplazamiento suele ser relativo al principio de la estructura .

## <a name="complex-arrays"></a>Matrices complejas

Una matriz compleja es cualquier matriz con un elemento que impide que se copie en bloque y, como tal, es necesario realizar acciones adicionales. Estos elementos hacen que una matriz sea compleja:

-   tipos simples: ENUM16, \_ INT3264 (solo en plataformas de \_ 64 bits), una integral con \[ [ **intervalo**](/windows/desktop/Midl/range)\]
-   punteros de referencia e interfaz (todos los punteros en plataformas de 64 bits)
-   uniones
-   estructuras complejas (consulte el tema Descripción de la estructura compleja para obtener una lista completa de los motivos por los que una estructura es compleja)
-   Elementos definidos con transmisión como , \[ [**\_ serialización**](/windows/desktop/Midl/transmit-as) \] \[ [**\_ de usuario**](/windows/desktop/Midl/user-marshal)\]
-   Todas las matrices multidimensionales con al menos una dimensión compatible o variable son complejas independientemente del tipo de elemento subyacente.

La descripción de la matriz compleja es la siguiente:

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

El número \_ de \_ elementos<2> campo es cero si la matriz es compatible.

La descripción de conformidad<> descripción de varianza<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de si \_ \_ se usa [**/robust.**](/windows/desktop/Midl/-robust) Si la matriz tiene conformidad o varianza, la descripción de conformidad<> o descripción de varianza<> los campos tienen descripciones válidas; de lo contrario, los primeros 4 bytes del descriptor de correlación se \_ \_ establecen en 0xFFFFFFFF. Las marcas, cuando están presentes, se establecen en cero.

 

 
