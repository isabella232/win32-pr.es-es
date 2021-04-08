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
# <a name="conformant-arrays"></a><span data-ttu-id="63e86-103">Matrices compatibles</span><span class="sxs-lookup"><span data-stu-id="63e86-103">Conformant Arrays</span></span>

<span data-ttu-id="63e86-104">El tamaño de una matriz compatible puede variar o ajustarse cada vez que el cliente la pasa a un procedimiento remoto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="63e86-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="63e86-105">La definición de interfaz del archivo MIDL de la aplicación permite al cliente especificar el tamaño de la matriz cada vez que invoca el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="63e86-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="63e86-106">Use corchetes vacíos ( \[ \] ) o un asterisco entre corchetes ( \[ \* \] ) en la definición de la matriz para indicar una matriz compatible.</span><span class="sxs-lookup"><span data-stu-id="63e86-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="63e86-107">El ejemplo siguiente contiene la definición de un procedimiento remoto en una interfaz en un archivo MIDL.</span><span class="sxs-lookup"><span data-stu-id="63e86-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="63e86-108">El cliente especifica el tamaño de la matriz que pasa al servidor mediante el parámetro *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="63e86-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

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

<span data-ttu-id="63e86-109">La definición de interfaz usa el tamaño del atributo MIDL \[ [**\_ es**](/windows/desktop/Midl/size-is) \] para especificar el tamaño de la matriz que el cliente pasa al servidor.</span><span class="sxs-lookup"><span data-stu-id="63e86-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="63e86-110">Si prefiere indicar el valor máximo de los números de índice de la matriz, utilice \[ en su lugar el atributo [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="63e86-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="63e86-111">Para obtener más información sobre estos atributos MIDL, vea [atributos de matriz](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="63e86-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="63e86-112">En el fragmento de código siguiente se muestra cómo un cliente puede invocar el procedimiento remoto definido en el archivo MIDL anterior.</span><span class="sxs-lookup"><span data-stu-id="63e86-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="63e86-113">Este fragmento llama al procedimiento remoto MyRemoteProc dos veces.</span><span class="sxs-lookup"><span data-stu-id="63e86-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="63e86-114">En la primera invocación, pasa una matriz de 20 elementos.</span><span class="sxs-lookup"><span data-stu-id="63e86-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="63e86-115">En la segunda llamada, el cliente pasa una matriz de 200 elementos.</span><span class="sxs-lookup"><span data-stu-id="63e86-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 