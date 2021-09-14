---
title: Matrices variables
description: En MIDL, las matrices variables tienen un tamaño fijo. Permiten a los clientes pasar diferentes partes de matrices de clientes a servidores. El tamaño de la parte de la matriz puede variar de invocación a invocación. Sin embargo, el tamaño de la matriz global es fijo.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169030"
---
# <a name="varying-arrays"></a>Matrices variables

En MIDL, las matrices variables tienen un tamaño fijo. Permiten a los clientes pasar diferentes partes de matrices de clientes a servidores. El tamaño de la parte de la matriz puede variar de invocación a invocación. Sin embargo, el tamaño de la matriz global es fijo.

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

La definición de interfaz que usa primero el atributo MIDL es especificar el número de índice del primer elemento de la parte de la matriz que el cliente \[ [**\_**](/windows/desktop/Midl/first-is) pasa \] al servidor. El \[ [**atributo length \_ is**](/windows/desktop/Midl/length-is) especifica el número total de elementos de \] matriz que pasa el cliente. Para obtener más información sobre estos atributos MIDL, vea [Atributos de matriz](array-attributes.md).

En el fragmento de código siguiente se muestra cómo un cliente podría invocar el procedimiento remoto definido en el archivo MIDL anterior.


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



Este fragmento llama dos veces al procedimiento remoto MyRemoteProc. En la primera invocación, pasa los elementos de matriz numerados de 20 a 119, tal y como indican los valores de las variables firstArrayElementNumber y totalElementsPassed. En la segunda llamada, el cliente pasa los elementos de matriz numerados de 120 a 319.

 

 