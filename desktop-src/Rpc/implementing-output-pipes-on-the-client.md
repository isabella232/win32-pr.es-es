---
title: Implementar canalizaciones de salida en el cliente
description: Cuando se usa una canalización de salida para transferir datos desde el servidor al cliente, debe implementar un procedimiento de inserción en el cliente.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e959db9e505bb7dfe570552fe0385251485591fecb1f818ab4d5de402c2297b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929134"
---
# <a name="implementing-output-pipes-on-the-client"></a>Implementar canalizaciones de salida en el cliente

Cuando se usa una canalización de salida para transferir datos desde el servidor al cliente, debe implementar un procedimiento de inserción en el cliente. El procedimiento de inserción toma un puntero a un búfer y un recuento de elementos del código auxiliar del cliente y, si el recuento de elementos es mayor que 0, procesa los datos. Por ejemplo, podría copiar los datos del búfer del código auxiliar en su propia memoria. Como alternativa, podría procesar los datos en el búfer del código auxiliar y guardarlos en un archivo. Cuando el recuento de elementos es igual a cero, el procedimiento de inserción completa las tareas de limpieza necesarias antes de volver.

En el ejemplo siguiente, la función de cliente ReceiveLongs asigna una estructura de canalización y un búfer de memoria global. Inicializa la estructura , realiza la llamada a procedimiento remoto y, a continuación, libera la memoria.

## <a name="example"></a>Ejemplo


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



En este ejemplo se incluye el archivo de encabezado generado por el compilador midl. Para obtener más información, [vea Definición de canalizaciones en el archivo IDL](defining-pipes-in-idl-files.md). También declara una variable, globalPipeData, que usa como receptor de datos. La variable globalBuffer es un búfer que el procedimiento de inserción usa para recibir bloques de datos que almacena en globalPipeData.

La función ReceiveLongs declara una canalización y asigna espacio de memoria para la variable de receptor de datos global. En el programa cliente/servidor, el receptor de datos puede ser un archivo o una estructura de datos que el cliente crea. En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.

Antes de que pueda comenzar la transferencia de datos, el programa cliente debe inicializar la estructura de canalización de salida. Debe establecer punteros a la variable de estado, el procedimiento de inserción y el procedimiento de asignación. En este ejemplo, la variable de canalización de salida se denomina outputPipe.

Los clientes señalan a los servidores que están listos para recibir datos mediante la invocación de un procedimiento remoto en el servidor. En este ejemplo, el procedimiento remoto se denomina OutPipe. Cuando el cliente llama al procedimiento remoto, el servidor comienza la transferencia de datos. Cada vez que llegan los datos, el código auxiliar del cliente llama a los procedimientos de inserción y de aoc del cliente según sea necesario.

En lugar de asignar memoria cada vez que se necesita un búfer, el procedimiento de asignación de este ejemplo simplemente establece un puntero a la variable globalBuffer. A continuación, el procedimiento de extracción reutiliza este búfer cada vez que transfiere datos. Es posible que los programas cliente más complejos necesiten asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.

El procedimiento de inserción de este ejemplo usa la variable de estado para realizar un seguimiento de la siguiente posición donde almacenará los datos en el búfer del receptor de datos global. Escribe datos del búfer de canalización en el búfer receptor. A continuación, el código auxiliar de cliente recibe el siguiente bloque de datos del servidor y los almacena en el búfer de canalización. Cuando se han enviado todos los datos, el servidor transmite un búfer de tamaño cero. Esto hace que el procedimiento de inserción deje de recibir datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Pipa](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 