---
title: " in, out, size_is prototipo"
description: '\ in, out, size \_ es \ prototype usa una matriz de caracteres de un solo recuento que se pasa desde el cliente al servidor y desde el servidor al cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359053"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="40cac-103">\[in, out, el tamaño \_ es \] prototype</span><span class="sxs-lookup"><span data-stu-id="40cac-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="40cac-104">El prototipo de función siguiente usa una matriz de caracteres de un solo recuento que se pasa de ambas maneras: de cliente a servidor y de servidor a cliente:</span><span class="sxs-lookup"><span data-stu-id="40cac-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="40cac-105">Como parámetro \[ [**in**](/windows/desktop/Midl/in) \] , *achInOut* debe apuntar a un almacenamiento válido en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="40cac-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="40cac-106">El desarrollador asigna la memoria asociada a la matriz en el lado cliente antes de efectuar la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="40cac-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="40cac-107">El código auxiliar usa el \[ parámetro [**size \_**](/windows/desktop/Midl/size-is) \] *strsize* para asignar memoria en el servidor y, a continuación, usar la \[ [**longitud \_ es**](/windows/desktop/Midl/length-is) el \] parámetro *PCB* para transmitir los elementos de la matriz a esta memoria.</span><span class="sxs-lookup"><span data-stu-id="40cac-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="40cac-108">El desarrollador debe asegurarse de que el código de cliente establece la **\[ longitud \_ \]** de la variable antes de llamar al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="40cac-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="40cac-109">En algunas situaciones, el uso de parámetros independientes en lugar de una sola cadena para la entrada y la salida es más eficaz y proporciona flexibilidad.</span><span class="sxs-lookup"><span data-stu-id="40cac-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="40cac-110">Esto se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="40cac-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="40cac-111">En el ejemplo anterior, la matriz de caracteres achInOut también se utiliza como \[ parámetro [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="40cac-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="40cac-112">En C, el nombre de la matriz es equivalente al uso de un puntero.</span><span class="sxs-lookup"><span data-stu-id="40cac-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="40cac-113">De forma predeterminada, todos los punteros de nivel superior son punteros de referencia; no cambian de valor y apuntan a la misma área de memoria en el cliente antes y después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="40cac-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="40cac-114">Toda la memoria a la que el procedimiento remoto tiene acceso debe ajustarse al tamaño que el cliente especifica antes de la llamada, o el código auxiliar generará una excepción.</span><span class="sxs-lookup"><span data-stu-id="40cac-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="40cac-115">Antes de volver, la función Analyze en el servidor debe restablecer el parámetro *PCB* para indicar el número de elementos que el servidor transmitirá al cliente, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="40cac-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 