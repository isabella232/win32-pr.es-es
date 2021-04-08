---
title: Matrices compatibles
description: El tamaño de una matriz compatible puede variar o ajustarse cada vez que el cliente la pasa a un procedimiento remoto en el servidor.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078203"
---
# <a name="conformant-arrays"></a>Matrices compatibles

El tamaño de una matriz compatible puede variar o ajustarse cada vez que el cliente la pasa a un procedimiento remoto en el servidor. La definición de interfaz del archivo MIDL de la aplicación permite al cliente especificar el tamaño de la matriz cada vez que invoca el procedimiento remoto. Use corchetes vacíos ( \[ \] ) o un asterisco entre corchetes ( \[ \* \] ) en la definición de la matriz para indicar una matriz compatible.

El ejemplo siguiente contiene la definición de un procedimiento remoto en una interfaz en un archivo MIDL. El cliente especifica el tamaño de la matriz que pasa al servidor mediante el parámetro *tamaño*.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

La definición de interfaz usa el tamaño del atributo MIDL \[ [**\_ es**](/windows/desktop/Midl/size-is) \] para especificar el tamaño de la matriz que el cliente pasa al servidor. Si prefiere indicar el valor máximo de los números de índice de la matriz, utilice \[ en su lugar el atributo [**Max \_ is**](/windows/desktop/Midl/max-is) \] . Para obtener más información sobre estos atributos MIDL, vea [atributos de matriz](array-attributes.md).

En el fragmento de código siguiente se muestra cómo un cliente puede invocar el procedimiento remoto definido en el archivo MIDL anterior.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Este fragmento llama al procedimiento remoto MyRemoteProc dos veces. En la primera invocación, pasa una matriz de 20 elementos. En la segunda llamada, el cliente pasa una matriz de 200 elementos.

 

 