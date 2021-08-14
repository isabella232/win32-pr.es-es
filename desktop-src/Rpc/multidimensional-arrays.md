---
title: Matrices multidimensionales
description: Los atributos de matriz también se pueden usar con matrices multidimensionales.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7dac2b6d093fa56383ecaf976a83acf13fec9aa0c3820c1d608ccb69e9e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928093"
---
# <a name="multidimensional-arrays"></a>Matrices multidimensionales

Los atributos de matriz también se pueden usar con matrices multidimensionales. Sin embargo, tenga cuidado de asegurarse de que cada dimensión de la matriz tiene un atributo correspondiente. Por ejemplo:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

La matriz anterior es una matriz compatible (de tamaño d1size) de 30 matrices de elementos (con elementos d2len incluidos para cada una). La coma entre paréntesis del atributo size especifica que el valor de d1size se aplica a la primera dimensión de la \[ [**\_**](/windows/desktop/Midl/size-is) \] matriz. Del mismo modo, el comando entre paréntesis de la longitud es attribute indica que el valor de d2len se aplica a la segunda dimensión \[ [**\_**](/windows/desktop/Midl/length-is) de \] la matriz.

El compilador midl 2.0 proporciona dos métodos para serializar parámetros: modo mixto (/**so**) y totalmente interpretado (/**Oif** o /**Oicf**). De forma predeterminada, el compilador MIDL compila interfaces en modo mixto. No es necesario especificar explícitamente el modificador [**/Os**](/windows/desktop/Midl/-os) para obtener la serialización en modo mixto.

El método totalmente interpretado serializa los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento. En la serialización en modo mixto, el código auxiliar serializa algunos parámetros en línea. Aunque esto da como resultado un tamaño de código auxiliar mayor, también ofrece un mayor rendimiento.

> [!Caution]  
> Tenga cuidado al compilar archivos IDL en este modo. El uso de matrices multidimensionales en modo mixto puede dar lugar a parámetros que no se serializan correctamente. Se recomienda el modificador de línea de comandos [**/Oicf**](/windows/desktop/Midl/-oi) cuando la interfaz define parámetros que son matrices multidimensionales.

 

El \[ [**atributo**](/windows/desktop/Midl/string) \] string también se puede usar con matrices multidimensionales. El atributo se aplica a la dimensión menos significativa, como una matriz compatible de cadenas. También puede usar atributos de puntero multidimensionales. Por ejemplo:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

En el ejemplo anterior, la variable ptr2d es un puntero a un bloque de punteros de tamaño d1len, cada uno de los cuales apunta a punteros d2len a **long.**

Las matrices multidimensionales no son equivalentes a las matrices de punteros. Una matriz multidimensional es un bloque de datos único y grande en memoria. Una matriz de punteros solo contiene un bloque de punteros en la matriz. Los datos a los que apuntan los punteros pueden estar en cualquier lugar de la memoria. Además, la sintaxis de ANSI C solo permite que la dimensión de matriz más significativa (más a la izquierda) no se pueda especificar en una matriz multidimensional. Por lo tanto, lo siguiente es una instrucción válida:

`long a1[] [20]`

Compare esto con la siguiente instrucción no válida:

`long a1[20] []`

 

 