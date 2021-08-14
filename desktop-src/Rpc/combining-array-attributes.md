---
title: Combinación de atributos de matriz
description: Los atributos de campo se pueden proporcionar en varias combinaciones, siempre y cuando el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se transmitirán al servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd440251a658dd5b888df7275f578369419d4b8b2d4f920b263bc5095c4bd948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931758"
---
# <a name="combining-array-attributes"></a>Combinación de atributos de matriz

Los atributos de campo se pueden proporcionar en varias combinaciones, siempre y cuando el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se transmitirán al servidor. Las relaciones entre los atributos se definen mediante las fórmulas siguientes:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Los valores asociados a los atributos deben cumplir varias reglas de sentido común basadas en esas fórmulas. Estas reglas son:

-   No especifique que un \[ [**primer valor de índice \_ sea**](/windows/desktop/Midl/first-is) \] menor que cero o que un último \[ [**\_ valor**](/windows/desktop/Midl/last-is) \] sea mayor que max \[ [**\_ es**](/windows/desktop/Midl/max-is) \] .
-   No especifique un tamaño negativo para una matriz. Defina el primer y el último elemento para que se den como resultado un valor de longitud de cero o mayor. Defina el \[ [**valor max \_ is**](/windows/desktop/Midl/max-is) \] para que el tamaño sea cero o mayor. Si midl se invocó con la opción de comprobación [**/error**](/windows/desktop/Midl/-error) bounds, el código auxiliar genera una excepción cuando el tamaño es menor que cero o la longitud transmitida es menor \_ que cero.
-   No use la longitud es y last son atributos al mismo tiempo, ni el tamaño es y \[ [**\_**](/windows/desktop/Midl/length-is) \] last \[ [**\_**](/windows/desktop/Midl/last-is) \] \[ **\_** \] \[ **\_ son** \] atributos al mismo tiempo.

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

 

 