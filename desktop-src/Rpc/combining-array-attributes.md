---
title: Combinar atributos de matriz
description: Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se transmitirán al servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071429"
---
# <a name="combining-array-attributes"></a>Combinar atributos de matriz

Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se transmitirán al servidor. Las relaciones entre los atributos se definen mediante las fórmulas siguientes:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Los valores asociados a los atributos deben cumplir varias reglas de sentido común basadas en esas fórmulas. Estas reglas son:

-   No especifique una primera \[ [**es un valor \_ de**](/windows/desktop/Midl/first-is) índice menor que cero o un \] último \[ [**\_ valor**](/windows/desktop/Midl/last-is) \] es mayor que max \[ [**\_ es**](/windows/desktop/Midl/max-is) \] .
-   No especifique un tamaño negativo para una matriz. Defina el primer y el último elemento para que se den como resultado un valor de longitud de cero o mayor. Defina el \[ [**valor máximo \_ es**](/windows/desktop/Midl/max-is) \] para que el tamaño sea cero o mayor. Si se invocó MIDL con la opción [**/error**](/windows/desktop/Midl/-error) bounds check, el código auxiliar genera una excepción cuando el tamaño es menor que cero o la longitud transmitida es menor \_ que cero.
-   No use la longitud es y last es atributos al mismo tiempo, ni el tamaño es y el último \[ [**\_**](/windows/desktop/Midl/length-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] \[ **\_** \] \[ **\_ son** \] atributos al mismo tiempo.

Debido a la relación de cierre en C entre matrices y punteros, MIDL también permite declarar matrices en listas de parámetros mediante la notación de puntero. MIDL trata un parámetro que es un puntero a un tipo como una matriz de ese tipo si el parámetro tiene cualquiera de los atributos asociados normalmente a matrices.

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

 

 