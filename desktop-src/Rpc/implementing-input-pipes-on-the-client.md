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
# <a name="implementing-input-pipes-on-the-client"></a>Implementar canalizaciones de entrada en el cliente

Al usar una canalización de entrada para transferir datos desde el cliente al servidor, debe implementar un procedimiento de extracción. El procedimiento de extracción debe buscar los datos que se van a transferir, leer los datos en el búfer y establecer el número de elementos que se van a enviar. No todos los datos tienen que estar en el búfer cuando el servidor empieza a extraer datos a sí mismo. El procedimiento de extracción puede llenar el búfer incrementalmente.

Cuando no hay más datos para enviar, el procedimiento establece su último argumento en cero. Cuando se envían todos los datos, el procedimiento de extracción debe realizar cualquier limpieza necesaria antes de volver. Para un parámetro que se encuentra \[ en una canalización de salida, \] el procedimiento de extracción debe restablecer la variable de estado del cliente una vez transmitidos todos los datos, de modo que el procedimiento de inserción pueda usarlo para recibir datos.

El siguiente ejemplo se extrae del programa Pipedemo que se incluye con el kit de desarrollo de software (SDK) de la plataforma.


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



En este ejemplo se incluye el archivo de encabezado generado por el compilador MIDL. Para obtener más información, vea [definir canalizaciones en archivos IDL](defining-pipes-in-idl-files.md). También declara una variable que usa como el origen de datos denominado globalPipeData. La variable globalBuffer es un búfer que el procedimiento de extracción utiliza para enviar los bloques de datos que obtiene de globalPipeData.

La función SendLongs declara la canalización de entrada y asigna memoria para la variable de origen de datos globalPipeData. En el programa cliente/servidor, el origen de datos puede ser un archivo o una estructura que crea el cliente. También puede hacer que el programa cliente obtenga los datos del servidor, los procese y los devuelva al servidor mediante una canalización de entrada. En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.

Antes de que pueda comenzar la transferencia, el cliente debe establecer punteros a la variable de estado, el procedimiento de extracción y el procedimiento de asignación. Estos punteros se mantienen en la variable de canalización que declara el cliente. En este caso, SendLongs declara la incanalización. Puede usar cualquier tipo de datos adecuado para la variable de estado.

Los clientes inician las transferencias de datos a través de una canalización mediante la invocación de un procedimiento remoto en el servidor. Al llamar al procedimiento remoto, se indica al programa de servidor que el cliente está listo para transmitir. Después, el servidor puede extraer los datos a sí mismo. En este ejemplo se invoca un procedimiento remoto denominado inpipe. Una vez transferidos los datos al servidor, la función SendLongs libera el búfer asignado dinámicamente.

En lugar de asignar memoria cada vez que se necesita un búfer. en este ejemplo, el procedimiento de asignación simplemente establece un puntero a la variable globalBuffer. El procedimiento de extracción reutiliza este búfer cada vez que transfiere los datos. Los programas cliente más complejos pueden necesitar asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.

El código auxiliar del cliente llama al procedimiento de extracción. El procedimiento de extracción de este ejemplo utiliza la variable de estado para realizar el seguimiento de la siguiente posición en el búfer de origen de datos global del que se va a leer. Lee los datos del búfer de origen en el búfer de canalización. El código auxiliar del cliente transmite los datos al servidor. Cuando se han enviado todos los datos, el procedimiento de extracción establece el tamaño del búfer en cero. Esto indica al servidor que detenga la extracción de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[codo](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 