---
title: Matrices (RPC) (TFS)
description: Entre las categorías de matriz de llamada a procedimiento remoto (RPC) se incluyen el tamaño fijo, el cumplimiento, la estructura variable, la variable y la complejidad.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388817"
---
# <a name="arrays-rpc"></a>Matrices (RPC)

Varias categorías de matriz se han definido en función de sus características de rendimiento, principalmente si la matriz puede ser copiada en bloque.

En algunas categorías, como una matriz de tamaño fijo, existen dos tipos de descriptores de matriz; se indican con una corrección en el nombre del token de FC inicial.



| Carácter de formato | Descripción                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | El tamaño total del tipo se puede representar en un int sin signo de 16 bits.    |
| LG               | El tamaño total del tipo requiere un valor de unsigned Long de 32 bits para que se represente. |



 

Campos comunes a las matrices:

-   \_Tamaño total

    Tamaño total de la matriz en memoria, en bytes. Es igual que el tamaño de conexión después de la alineación. El tamaño total se calcula para las categorías para las que no existe el problema de relleno y el tamaño es el tamaño real de la matriz.

-   tamaño del elemento \_

    Tamaño total en memoria de un solo elemento de la matriz, incluido el relleno (esto puede ocurrir solo para matrices complejas).

-   Descripción del elemento \_

    Descripción del tipo de elemento de la matriz.

-   diseño de puntero \_

    Vea el tema [diseño de puntero](pointer-layout-tfs.md) para obtener más información.

## <a name="fixed-sized-arrays"></a>Matrices de tamaño fijo

Se genera una cadena de formato de matriz de tamaño fijo para las matrices que tienen un tamaño conocido y, por lo tanto, se puede copiar en bloque en el búfer de serialización. Los dos formatos de descriptor de matriz fijos son los siguientes.

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

La descripción del cumplimiento \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .

## <a name="conformant-varying-array"></a>Matriz variable compatible

Una matriz variable compatible también se puede copiar en bloque.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

La descripción del cumplimiento \_<> y la \_ Descripción de la varianza<> es un descriptor de correlación y tiene 4 o 6 bytes en función de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .

## <a name="varying-array"></a>Matriz variable

Las distintas matrices tienen dos posibilidades, dependiendo del tamaño de la matriz.

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

La descripción de la varianza \_<> es un descriptor de correlación y tiene 4 o 6 bytes según el [**/Robust**](/windows/desktop/Midl/-robust) que se está usando.

En el caso de las distintas matrices incrustadas dentro de una estructura, el desplazamiento<2> campo de la descripción de la varianza \_<> es un desplazamiento relativo desde la posición de la matriz variable en la estructura hasta el campo de varianza que describe. El desplazamiento suele ser relativo al principio de la estructura.

## <a name="complex-arrays"></a>Matrices complejas

Una matriz compleja es cualquier matriz con un elemento que impide que se copie en bloque y, como tal, se debe realizar una acción adicional. Estos elementos hacen que una matriz sea compleja:

-   tipos simples: ENUM16, \_ \_ INT3264 (solo en plataformas de 64 bits), un entero con \[ [ **rango**](/windows/desktop/Midl/range)\]
-   punteros de referencia y de interfaz (todos los punteros en plataformas de 64 bits)
-   uniones
-   estructuras complejas (consulte el tema de descripción de la estructura compleja para obtener una lista completa de los motivos para que una estructura sea compleja)
-   elementos definidos con \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ cálculo de referencias de usuarios**](/windows/desktop/Midl/user-marshal)\]
-   Todas las matrices multidimensionales con al menos una dimensión compatible y/o variable son complejas, independientemente del tipo de elemento subyacente.

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

La descripción del cumplimiento \_<> y la \_ Descripción de la varianza<> es un descriptor de correlación y tiene 4 o 6 bytes en función de si se usa [**/Robust**](/windows/desktop/Midl/-robust) . Si la matriz tiene cumplimiento y/o varianza, la descripción del cumplimiento \_<> y/o la descripción de la varianza \_<> campos tienen descripciones válidas; de lo contrario, los cuatro primeros bytes del descriptor de correlación se establecen en 0xFFFFFFFF. Las marcas, cuando están presentes, se establecen en cero.

 

 
