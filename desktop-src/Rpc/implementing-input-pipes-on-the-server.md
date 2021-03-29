---
title: Implementar canalizaciones de entrada en el servidor
description: Para empezar a enviar datos a un servidor, un cliente llama a uno de los procedimientos remotos del servidor.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903567"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="6f532-103">Implementar canalizaciones de entrada en el servidor</span><span class="sxs-lookup"><span data-stu-id="6f532-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="6f532-104">Para empezar a enviar datos a un servidor, un cliente llama a uno de los procedimientos remotos del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f532-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="6f532-105">Este procedimiento debe llamar repetidamente al procedimiento de extracción en el código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f532-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="6f532-106">El compilador MIDL usa el archivo IDL de la aplicación para generar automáticamente el procedimiento de extracción del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f532-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="6f532-107">Cada vez que el programa de servidor invoca el procedimiento de extracción en su código auxiliar, el procedimiento de extracción recibe bloques de datos del cliente.</span><span class="sxs-lookup"><span data-stu-id="6f532-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="6f532-108">No calcula las referencias de los datos en el búfer del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f532-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="6f532-109">Después, el procedimiento remoto del servidor puede procesar estos datos de la forma que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6f532-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="6f532-110">El bucle continúa hasta que el servidor recibe un búfer de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="6f532-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="6f532-111">El ejemplo siguiente es del programa Pipedemo incluido en los ejemplos que se incluyen con el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="6f532-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="6f532-112">Muestra un procedimiento de servidor remoto que usa una canalización para extraer datos del cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="6f532-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




