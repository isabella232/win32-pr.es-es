---
title: Implementar canalizaciones de entrada en el cliente
description: Al usar una canalización de entrada para transferir datos desde el cliente al servidor, debe implementar un procedimiento de extracción.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904732"
---
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="f4e78-103">Implementar canalizaciones de entrada en el cliente</span><span class="sxs-lookup"><span data-stu-id="f4e78-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="f4e78-104">Al usar una canalización de entrada para transferir datos desde el cliente al servidor, debe implementar un procedimiento de extracción.</span><span class="sxs-lookup"><span data-stu-id="f4e78-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="f4e78-105">El procedimiento de extracción debe buscar los datos que se van a transferir, leer los datos en el búfer y establecer el número de elementos que se van a enviar.</span><span class="sxs-lookup"><span data-stu-id="f4e78-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="f4e78-106">No todos los datos tienen que estar en el búfer cuando el servidor empieza a extraer datos a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f4e78-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="f4e78-107">El procedimiento de extracción puede llenar el búfer incrementalmente.</span><span class="sxs-lookup"><span data-stu-id="f4e78-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="f4e78-108">Cuando no hay más datos para enviar, el procedimiento establece su último argumento en cero.</span><span class="sxs-lookup"><span data-stu-id="f4e78-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="f4e78-109">Cuando se envían todos los datos, el procedimiento de extracción debe realizar cualquier limpieza necesaria antes de volver.</span><span class="sxs-lookup"><span data-stu-id="f4e78-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="f4e78-110">Para un parámetro que se encuentra \[ en una canalización de salida, \] el procedimiento de extracción debe restablecer la variable de estado del cliente una vez transmitidos todos los datos, de modo que el procedimiento de inserción pueda usarlo para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="f4e78-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="f4e78-111">El siguiente ejemplo se extrae del programa Pipedemo que se incluye con el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="f4e78-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
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
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



<span data-ttu-id="f4e78-112">En este ejemplo se incluye el archivo de encabezado generado por el compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="f4e78-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="f4e78-113">Para obtener más información, vea [definir canalizaciones en archivos IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="f4e78-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="f4e78-114">También declara una variable que usa como el origen de datos denominado globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="f4e78-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="f4e78-115">La variable globalBuffer es un búfer que el procedimiento de extracción utiliza para enviar los bloques de datos que obtiene de globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="f4e78-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="f4e78-116">La función SendLongs declara la canalización de entrada y asigna memoria para la variable de origen de datos globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="f4e78-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="f4e78-117">En el programa cliente/servidor, el origen de datos puede ser un archivo o una estructura que crea el cliente.</span><span class="sxs-lookup"><span data-stu-id="f4e78-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="f4e78-118">También puede hacer que el programa cliente obtenga los datos del servidor, los procese y los devuelva al servidor mediante una canalización de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4e78-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="f4e78-119">En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.</span><span class="sxs-lookup"><span data-stu-id="f4e78-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="f4e78-120">Antes de que pueda comenzar la transferencia, el cliente debe establecer punteros a la variable de estado, el procedimiento de extracción y el procedimiento de asignación.</span><span class="sxs-lookup"><span data-stu-id="f4e78-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="f4e78-121">Estos punteros se mantienen en la variable de canalización que declara el cliente.</span><span class="sxs-lookup"><span data-stu-id="f4e78-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="f4e78-122">En este caso, SendLongs declara la incanalización.</span><span class="sxs-lookup"><span data-stu-id="f4e78-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="f4e78-123">Puede usar cualquier tipo de datos adecuado para la variable de estado.</span><span class="sxs-lookup"><span data-stu-id="f4e78-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="f4e78-124">Los clientes inician las transferencias de datos a través de una canalización mediante la invocación de un procedimiento remoto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f4e78-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="f4e78-125">Al llamar al procedimiento remoto, se indica al programa de servidor que el cliente está listo para transmitir.</span><span class="sxs-lookup"><span data-stu-id="f4e78-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="f4e78-126">Después, el servidor puede extraer los datos a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="f4e78-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="f4e78-127">En este ejemplo se invoca un procedimiento remoto denominado inpipe.</span><span class="sxs-lookup"><span data-stu-id="f4e78-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="f4e78-128">Una vez transferidos los datos al servidor, la función SendLongs libera el búfer asignado dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="f4e78-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="f4e78-129">En lugar de asignar memoria cada vez que se necesita un búfer.</span><span class="sxs-lookup"><span data-stu-id="f4e78-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="f4e78-130">en este ejemplo, el procedimiento de asignación simplemente establece un puntero a la variable globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="f4e78-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="f4e78-131">El procedimiento de extracción reutiliza este búfer cada vez que transfiere los datos.</span><span class="sxs-lookup"><span data-stu-id="f4e78-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="f4e78-132">Los programas cliente más complejos pueden necesitar asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.</span><span class="sxs-lookup"><span data-stu-id="f4e78-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="f4e78-133">El código auxiliar del cliente llama al procedimiento de extracción.</span><span class="sxs-lookup"><span data-stu-id="f4e78-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="f4e78-134">El procedimiento de extracción de este ejemplo utiliza la variable de estado para realizar el seguimiento de la siguiente posición en el búfer de origen de datos global del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="f4e78-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="f4e78-135">Lee los datos del búfer de origen en el búfer de canalización.</span><span class="sxs-lookup"><span data-stu-id="f4e78-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="f4e78-136">El código auxiliar del cliente transmite los datos al servidor.</span><span class="sxs-lookup"><span data-stu-id="f4e78-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="f4e78-137">Cuando se han enviado todos los datos, el procedimiento de extracción establece el tamaño del búfer en cero.</span><span class="sxs-lookup"><span data-stu-id="f4e78-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="f4e78-138">Esto indica al servidor que detenga la extracción de datos.</span><span class="sxs-lookup"><span data-stu-id="f4e78-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4e78-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4e78-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e78-140">codo</span><span class="sxs-lookup"><span data-stu-id="f4e78-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="f4e78-141">**/OI**</span><span class="sxs-lookup"><span data-stu-id="f4e78-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 