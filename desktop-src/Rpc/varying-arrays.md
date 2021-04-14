---
title: Matrices variables
description: En MIDL, las distintas matrices tienen un tamaño fijo. Permiten a los clientes pasar distintas partes de las matrices de los clientes a los servidores. El tamaño de la parte de la matriz puede variar de una invocación a la invocación. Sin embargo, el tamaño de la matriz global es fijo.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488102"
---
# <a name="varying-arrays"></a>Matrices variables

En MIDL, las distintas matrices tienen un tamaño fijo. Permiten a los clientes pasar distintas partes de las matrices de los clientes a los servidores. El tamaño de la parte de la matriz puede variar de una invocación a la invocación. Sin embargo, el tamaño de la matriz global es fijo.

Por ejemplo, en el ejemplo siguiente se muestra la definición de un procedimiento remoto en una interfaz en un archivo MIDL. El tamaño de la matriz que el cliente pasa al servidor se corrige con el tamaño constante de la matriz \_ . La interfaz especifica la parte de la matriz que el cliente pasa al servidor en los parámetros firstElement y chunkSize.

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

La definición de interfaz usa el atributo MIDL en \[ [**primer lugar \_**](/windows/desktop/Midl/first-is) \] para especificar el número de índice del primer elemento en la parte de la matriz que el cliente pasa al servidor. El \[ [**atributo \_ length**](/windows/desktop/Midl/length-is) \] especifica el número total de elementos de matriz que el cliente pasa. Para obtener más información sobre estos atributos MIDL, vea [atributos de matriz](array-attributes.md).

En el fragmento de código siguiente se muestra cómo un cliente puede invocar el procedimiento remoto definido en el archivo MIDL anterior.


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



Este fragmento llama al procedimiento remoto MyRemoteProc dos veces. En la primera invocación, pasa los elementos de la matriz numerados del 20 al 119, tal y como indican los valores de las variables firstArrayElementNumber y totalElementsPassed. En la segunda llamada, el cliente pasa los elementos de la matriz numerados del 120 al 319.

 

 