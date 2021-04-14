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
# <a name="varying-arrays"></a><span data-ttu-id="e46bf-106">Matrices variables</span><span class="sxs-lookup"><span data-stu-id="e46bf-106">Varying Arrays</span></span>

<span data-ttu-id="e46bf-107">En MIDL, las distintas matrices tienen un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="e46bf-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="e46bf-108">Permiten a los clientes pasar distintas partes de las matrices de los clientes a los servidores.</span><span class="sxs-lookup"><span data-stu-id="e46bf-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="e46bf-109">El tamaño de la parte de la matriz puede variar de una invocación a la invocación.</span><span class="sxs-lookup"><span data-stu-id="e46bf-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="e46bf-110">Sin embargo, el tamaño de la matriz global es fijo.</span><span class="sxs-lookup"><span data-stu-id="e46bf-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="e46bf-111">Por ejemplo, en el ejemplo siguiente se muestra la definición de un procedimiento remoto en una interfaz en un archivo MIDL.</span><span class="sxs-lookup"><span data-stu-id="e46bf-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="e46bf-112">El tamaño de la matriz que el cliente pasa al servidor se corrige con el tamaño constante de la matriz \_ .</span><span class="sxs-lookup"><span data-stu-id="e46bf-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="e46bf-113">La interfaz especifica la parte de la matriz que el cliente pasa al servidor en los parámetros firstElement y chunkSize.</span><span class="sxs-lookup"><span data-stu-id="e46bf-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

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

<span data-ttu-id="e46bf-114">La definición de interfaz usa el atributo MIDL en \[ [**primer lugar \_**](/windows/desktop/Midl/first-is) \] para especificar el número de índice del primer elemento en la parte de la matriz que el cliente pasa al servidor.</span><span class="sxs-lookup"><span data-stu-id="e46bf-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="e46bf-115">El \[ [**atributo \_ length**](/windows/desktop/Midl/length-is) \] especifica el número total de elementos de matriz que el cliente pasa.</span><span class="sxs-lookup"><span data-stu-id="e46bf-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="e46bf-116">Para obtener más información sobre estos atributos MIDL, vea [atributos de matriz](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e46bf-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="e46bf-117">En el fragmento de código siguiente se muestra cómo un cliente puede invocar el procedimiento remoto definido en el archivo MIDL anterior.</span><span class="sxs-lookup"><span data-stu-id="e46bf-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="e46bf-118">Este fragmento llama al procedimiento remoto MyRemoteProc dos veces.</span><span class="sxs-lookup"><span data-stu-id="e46bf-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="e46bf-119">En la primera invocación, pasa los elementos de la matriz numerados del 20 al 119, tal y como indican los valores de las variables firstArrayElementNumber y totalElementsPassed.</span><span class="sxs-lookup"><span data-stu-id="e46bf-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="e46bf-120">En la segunda llamada, el cliente pasa los elementos de la matriz numerados del 120 al 319.</span><span class="sxs-lookup"><span data-stu-id="e46bf-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 