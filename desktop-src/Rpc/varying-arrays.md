---
title: Matrices variables
description: En MIDL, las distintas matrices tienen un tamaño fijo. Permiten a los clientes pasar diferentes partes de matrices de clientes a servidores. El tamaño de la parte de la matriz puede variar de invocación a invocación. Sin embargo, el tamaño de la matriz general es fijo.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3919eed28ef7a9c888d7c23e4ebe12a1db39c97b18fa325c6daf8a4cd62d6554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010553"
---
# <a name="varying-arrays"></a>Matrices variables

En MIDL, las distintas matrices tienen un tamaño fijo. Permiten a los clientes pasar diferentes partes de matrices de clientes a servidores. El tamaño de la parte de la matriz puede variar de invocación a invocación. Sin embargo, el tamaño de la matriz general es fijo.

Por ejemplo, en el ejemplo siguiente se muestra la definición de un procedimiento remoto en una interfaz en un archivo MIDL. El tamaño de la matriz que el cliente pasa al servidor se fija mediante la constante ARRAY \_ SIZE. La interfaz especifica la parte de la matriz que el cliente pasa al servidor en los parámetros firstElement y chunkSize.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

La definición de interfaz usa primero el atributo MIDL es especificar el número de índice del primer elemento de la parte de la matriz que el cliente \[ [**\_**](/windows/desktop/Midl/first-is) pasa \] al servidor. El \[ [**atributo length \_ es**](/windows/desktop/Midl/length-is) \] especifica el número total de elementos de matriz que pasa el cliente. Para obtener más información sobre estos atributos MIDL, vea [Atributos de matriz](array-attributes.md).

El fragmento de código siguiente muestra cómo un cliente podría invocar el procedimiento remoto definido en el archivo MIDL anterior.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Este fragmento llama dos veces al procedimiento remoto MyRemoteProc. En la primera invocación, pasa los elementos de la matriz numerados de 20 a 119, como indican los valores de las variables firstArrayElementNumber y totalElementsPassed. En la segunda llamada, el cliente pasa los elementos de matriz numerados de 120 a 319.

 

 