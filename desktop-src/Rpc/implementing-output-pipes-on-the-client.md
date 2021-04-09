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
# <a name="implementing-output-pipes-on-the-client"></a>Implementar canalizaciones de salida en el cliente

Al usar una canalización de salida para transferir datos del servidor al cliente, debe implementar un procedimiento de extracción en el cliente. El procedimiento de extracción toma un puntero a un búfer y un recuento de elementos del código auxiliar del cliente y, si el recuento de elementos es mayor que 0, procesa los datos. Por ejemplo, podría copiar los datos del búfer del código auxiliar en su propia memoria. Como alternativa, podría procesar los datos en el búfer del código auxiliar y guardarlos en un archivo. Cuando el recuento de elementos es igual a cero, el procedimiento de extracción completa cualquier tarea de limpieza necesaria antes de volver.

En el ejemplo siguiente, la función de cliente ReceiveLongs asigna una estructura de canalización y un búfer de memoria global. Inicializa la estructura, realiza la llamada a procedimiento remoto y libera la memoria.

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



En este ejemplo se incluye el archivo de encabezado generado por el compilador MIDL. Para obtener más información, vea [definir canalizaciones en un archivo IDL](defining-pipes-in-idl-files.md). También declara una variable, globalPipeData, que usa como receptor de datos. La variable globalBuffer es un búfer que el procedimiento de extracción utiliza para recibir los bloques de datos que almacena en globalPipeData.

La función ReceiveLongs declara una canalización y asigna espacio de memoria para la variable global del receptor de datos. En el programa cliente/servidor, el receptor de datos puede ser un archivo o una estructura de datos que crea el cliente. En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.

Antes de que pueda comenzar la transferencia de datos, el programa cliente debe inicializar la estructura de la canalización de salida. Debe establecer punteros a la variable de estado, al procedimiento de extracción y al procedimiento de asignación. En este ejemplo, la variable de canalización de salida se denomina outputPipe.

Los clientes señalan a los servidores que están preparados para recibir datos mediante la invocación de un procedimiento remoto en el servidor. En este ejemplo, el procedimiento remoto se denomina outpipe. Cuando el cliente llama al procedimiento remoto, el servidor inicia la transferencia de datos. Cada vez que llegan los datos, el código auxiliar del cliente llama a los procedimientos de asignación e instalación del cliente según sea necesario.

En lugar de asignar memoria cada vez que se necesita un búfer, el procedimiento de asignación en este ejemplo simplemente establece un puntero a la variable globalBuffer. A continuación, el procedimiento de extracción vuelve a utilizar este búfer cada vez que transfiere los datos. Los programas cliente más complejos pueden necesitar asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.

El procedimiento de extracción de este ejemplo usa la variable de estado para realizar el seguimiento de la siguiente posición en la que se almacenarán los datos en el búfer del receptor de datos global. Escribe los datos desde el búfer de canalización en el búfer del receptor. A continuación, el código auxiliar del cliente recibe el siguiente bloque de datos del servidor y lo almacena en el búfer de canalización. Cuando se han enviado todos los datos, el servidor transmite un búfer de tamaño cero. Este es el procedimiento de extracción para dejar de recibir datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[codo](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 