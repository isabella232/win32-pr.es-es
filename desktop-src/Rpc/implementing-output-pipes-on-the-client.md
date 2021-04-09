---
title: Implementar canalizaciones de salida en el cliente
description: Al usar una canalización de salida para transferir datos del servidor al cliente, debe implementar un procedimiento de extracción en el cliente.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791992"
---
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="c170b-103">Implementar canalizaciones de salida en el cliente</span><span class="sxs-lookup"><span data-stu-id="c170b-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="c170b-104">Al usar una canalización de salida para transferir datos del servidor al cliente, debe implementar un procedimiento de extracción en el cliente.</span><span class="sxs-lookup"><span data-stu-id="c170b-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="c170b-105">El procedimiento de extracción toma un puntero a un búfer y un recuento de elementos del código auxiliar del cliente y, si el recuento de elementos es mayor que 0, procesa los datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="c170b-106">Por ejemplo, podría copiar los datos del búfer del código auxiliar en su propia memoria.</span><span class="sxs-lookup"><span data-stu-id="c170b-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="c170b-107">Como alternativa, podría procesar los datos en el búfer del código auxiliar y guardarlos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c170b-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="c170b-108">Cuando el recuento de elementos es igual a cero, el procedimiento de extracción completa cualquier tarea de limpieza necesaria antes de volver.</span><span class="sxs-lookup"><span data-stu-id="c170b-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="c170b-109">En el ejemplo siguiente, la función de cliente ReceiveLongs asigna una estructura de canalización y un búfer de memoria global.</span><span class="sxs-lookup"><span data-stu-id="c170b-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="c170b-110">Inicializa la estructura, realiza la llamada a procedimiento remoto y libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="c170b-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="c170b-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c170b-111">Example</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



<span data-ttu-id="c170b-112">En este ejemplo se incluye el archivo de encabezado generado por el compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="c170b-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="c170b-113">Para obtener más información, vea [definir canalizaciones en un archivo IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="c170b-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="c170b-114">También declara una variable, globalPipeData, que usa como receptor de datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="c170b-115">La variable globalBuffer es un búfer que el procedimiento de extracción utiliza para recibir los bloques de datos que almacena en globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="c170b-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="c170b-116">La función ReceiveLongs declara una canalización y asigna espacio de memoria para la variable global del receptor de datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="c170b-117">En el programa cliente/servidor, el receptor de datos puede ser un archivo o una estructura de datos que crea el cliente.</span><span class="sxs-lookup"><span data-stu-id="c170b-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="c170b-118">En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.</span><span class="sxs-lookup"><span data-stu-id="c170b-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="c170b-119">Antes de que pueda comenzar la transferencia de datos, el programa cliente debe inicializar la estructura de la canalización de salida.</span><span class="sxs-lookup"><span data-stu-id="c170b-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="c170b-120">Debe establecer punteros a la variable de estado, al procedimiento de extracción y al procedimiento de asignación.</span><span class="sxs-lookup"><span data-stu-id="c170b-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="c170b-121">En este ejemplo, la variable de canalización de salida se denomina outputPipe.</span><span class="sxs-lookup"><span data-stu-id="c170b-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="c170b-122">Los clientes señalan a los servidores que están preparados para recibir datos mediante la invocación de un procedimiento remoto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c170b-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="c170b-123">En este ejemplo, el procedimiento remoto se denomina outpipe.</span><span class="sxs-lookup"><span data-stu-id="c170b-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="c170b-124">Cuando el cliente llama al procedimiento remoto, el servidor inicia la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="c170b-125">Cada vez que llegan los datos, el código auxiliar del cliente llama a los procedimientos de asignación e instalación del cliente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c170b-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="c170b-126">En lugar de asignar memoria cada vez que se necesita un búfer, el procedimiento de asignación en este ejemplo simplemente establece un puntero a la variable globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="c170b-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="c170b-127">A continuación, el procedimiento de extracción vuelve a utilizar este búfer cada vez que transfiere los datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="c170b-128">Los programas cliente más complejos pueden necesitar asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.</span><span class="sxs-lookup"><span data-stu-id="c170b-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="c170b-129">El procedimiento de extracción de este ejemplo usa la variable de estado para realizar el seguimiento de la siguiente posición en la que se almacenarán los datos en el búfer del receptor de datos global.</span><span class="sxs-lookup"><span data-stu-id="c170b-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="c170b-130">Escribe los datos desde el búfer de canalización en el búfer del receptor.</span><span class="sxs-lookup"><span data-stu-id="c170b-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="c170b-131">A continuación, el código auxiliar del cliente recibe el siguiente bloque de datos del servidor y lo almacena en el búfer de canalización.</span><span class="sxs-lookup"><span data-stu-id="c170b-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="c170b-132">Cuando se han enviado todos los datos, el servidor transmite un búfer de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="c170b-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="c170b-133">Este es el procedimiento de extracción para dejar de recibir datos.</span><span class="sxs-lookup"><span data-stu-id="c170b-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c170b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c170b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c170b-135">codo</span><span class="sxs-lookup"><span data-stu-id="c170b-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="c170b-136">**/OI**</span><span class="sxs-lookup"><span data-stu-id="c170b-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 