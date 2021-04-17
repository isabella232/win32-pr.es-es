---
title: Combinación de atributos de matriz
description: Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se van a transmitir al servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676458"
---
# <a name="combining-array-attributes"></a>Combinación de atributos de matriz

Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se van a transmitir al servidor. Las relaciones entre los atributos se definen mediante las siguientes fórmulas:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Los valores asociados a los atributos deben obedecer varias reglas de sentido común basadas en esas fórmulas. Estas reglas son:

-   No especifique que el \[ [**primer \_**](/windows/desktop/Midl/first-is) \] valor de índice sea menor que cero o que el \[ valor [**Last \_ sea**](/windows/desktop/Midl/last-is) \] mayor que \[ [**Max \_ is**](/windows/desktop/Midl/max-is) \] .
-   No especifique un tamaño negativo para una matriz. Defina el primer y el último elemento para que tengan como resultado un valor de longitud de cero o superior. Defina el \[ valor [**Max \_ is**](/windows/desktop/Midl/max-is) \] para que el tamaño sea cero o superior. Si se invocó MIDL con la opción [**/error**](/windows/desktop/Midl/-error) Bounds \_ check, el código auxiliar genera una excepción cuando el tamaño es menor que cero, o la longitud transmitida es menor que cero.
-   No use la \[ [**longitud \_**](/windows/desktop/Midl/length-is) \] y el \[ [**último \_ es**](/windows/desktop/Midl/last-is) los \] atributos al mismo tiempo, o el \[ **tamaño \_** y el \] \[ **último \_ son** \] atributos al mismo tiempo.

Debido a la relación de cierre de C entre matrices y punteros, MIDL también permite declarar matrices en listas de parámetros mediante la notación de puntero. MIDL trata un parámetro que es un puntero a un tipo como una matriz de ese tipo si el parámetro tiene cualquiera de los atributos que normalmente se asocian a las matrices.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

En el ejemplo anterior, los parámetros de matriz y puntero de las funciones fArray6 y fArray7 son equivalentes.

 

 