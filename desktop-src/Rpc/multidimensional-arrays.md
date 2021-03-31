---
title: Matrices multidimensionales
description: Los atributos de matriz también se pueden usar con matrices multidimensionales.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995473"
---
# <a name="multidimensional-arrays"></a>Matrices multidimensionales

Los atributos de matriz también se pueden usar con matrices multidimensionales. Sin embargo, tenga cuidado para asegurarse de que todas las dimensiones de la matriz tienen el atributo correspondiente. Por ejemplo:

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

La matriz anterior es una matriz compatible (de tamaño d1size) de 30 matrices de elementos (con elementos d2len enviados para cada uno). La coma entre paréntesis del \[ [**tamaño \_ es**](/windows/desktop/Midl/size-is) \] Attribute especifica que el valor de d1size se aplica a la primera dimensión de la matriz. Del mismo modo, el comando de los paréntesis de la \[ [**longitud \_ es**](/windows/desktop/Midl/length-is) \] Attribute indica que el valor de d2len se aplica a la segunda dimensión de la matriz.

El compilador de MIDL 2,0 proporciona dos métodos para calcular las referencias de los parámetros: modo mixto (/**os**) y completamente interpretado (/Activated **o/** **Oicf**). De forma predeterminada, el compilador MIDL compila las interfaces en modo mixto. No es necesario especificar explícitamente el modificador [**/os**](/windows/desktop/Midl/-os) para obtener el cálculo de referencias en modo mixto.

El método totalmente interpretado calcula las referencias de los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento. En el cálculo de referencias en modo mixto, el código auxiliar calcula las referencias de algunos parámetros en línea. Aunque esto da como resultado un mayor tamaño de código auxiliar, también ofrece un mayor rendimiento.

> [!Caution]  
> Tenga cuidado al compilar archivos IDL en este modo. El uso de matrices multidimensionales en modo mixto puede dar lugar a parámetros cuyas referencias no se han calculado correctamente. Se recomienda el modificador de la línea de comandos [**/Oicf**](/windows/desktop/Midl/-oi) cuando la interfaz define parámetros que son matrices multidimensionales.

 

El \[ atributo [**String**](/windows/desktop/Midl/string) \] también se puede utilizar con matrices multidimensionales. El atributo se aplica a la dimensión menos significativa, como una matriz de cadenas compatible. También puede usar atributos de puntero multidimensionales. Por ejemplo:

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

En el ejemplo anterior, la variable ptr2d es un puntero a un bloque de punteros de tamaño d1len, cada uno de los cuales señala a los punteros d2len a **Long**.

Las matrices multidimensionales no son equivalentes a las matrices de punteros. Una matriz multidimensional es un bloque de datos único y grande en la memoria. Una matriz de punteros solo contiene un bloque de punteros en la matriz. Los datos a los que apuntan los punteros pueden encontrarse en cualquier parte de la memoria. Además, la sintaxis de ANSI C solo permite que la dimensión de matriz más significativa (más a la izquierda) no se especifique en una matriz multidimensional. Por lo tanto, la siguiente es una instrucción válida:

`long a1[] [20]`

Compárelo con la siguiente instrucción no válida:

`long a1[20] []`

 

 