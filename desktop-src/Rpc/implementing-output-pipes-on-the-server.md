---
title: Implementación de canalizaciones de salida en el servidor
description: Para empezar a recibir datos de un servidor, un cliente llama a uno de los procedimientos remotos del servidor.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078254"
---
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="0e242-103">Implementación de canalizaciones de salida en el servidor</span><span class="sxs-lookup"><span data-stu-id="0e242-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="0e242-104">Para empezar a recibir datos de un servidor, un cliente llama a uno de los procedimientos remotos del servidor.</span><span class="sxs-lookup"><span data-stu-id="0e242-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="0e242-105">Este procedimiento debe llamar repetidamente al procedimiento de extracción en el código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="0e242-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="0e242-106">El compilador MIDL usa el archivo IDL de la aplicación para generar automáticamente el procedimiento de instalación del servidor.</span><span class="sxs-lookup"><span data-stu-id="0e242-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="0e242-107">La rutina del servidor remoto debe rellenar los datos del búfer de la canalización de salida antes de llamar al procedimiento de extracción.</span><span class="sxs-lookup"><span data-stu-id="0e242-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="0e242-108">Cada vez que el programa de servidor invoca el procedimiento de extracción en su código auxiliar, el procedimiento de envío calcula las referencias de los datos y los transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="0e242-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="0e242-109">El bucle continúa hasta que el servidor envía un búfer de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="0e242-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="0e242-110">El ejemplo siguiente es del programa Pipedemo incluido en los ejemplos incluidos en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0e242-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="0e242-111">Muestra un procedimiento de servidor remoto que usa una canalización para insertar datos del servidor en el cliente.</span><span class="sxs-lookup"><span data-stu-id="0e242-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a><span data-ttu-id="0e242-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e242-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e242-113">codo</span><span class="sxs-lookup"><span data-stu-id="0e242-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="0e242-114">**/OI**</span><span class="sxs-lookup"><span data-stu-id="0e242-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 