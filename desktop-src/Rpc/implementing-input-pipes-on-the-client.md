---
title: Implementar canalizaciones de entrada en el cliente
description: Cuando se usa una canalización de entrada para transferir datos desde el cliente al servidor, debe implementar un procedimiento de extracción.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0301fc7324a982db81b6c728131762361cfce185f3d432f238ca2cf8d715546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929124"
---
# <a name="implementing-input-pipes-on-the-client"></a>Implementar canalizaciones de entrada en el cliente

Cuando se usa una canalización de entrada para transferir datos desde el cliente al servidor, debe implementar un procedimiento de extracción. El procedimiento de extracción debe encontrar los datos que se transferirán, leer los datos en el búfer y establecer el número de elementos que se enviarán. No todos los datos deben estar en el búfer cuando el servidor comienza a extraer datos a sí mismo. El procedimiento de extracción puede rellenar el búfer de forma incremental.

Cuando no hay más datos que enviar, el procedimiento establece su último argumento en cero. Cuando se envían todos los datos, el procedimiento de extracción debe realizar la limpieza necesaria antes de volver. Para un parámetro que es una canalización de entrada y salida, el procedimiento de extracción debe restablecer la variable de estado del cliente una vez transmitidos todos los datos, de modo que el procedimiento de inserción pueda usarlo para recibir \[ \] datos.

El ejemplo siguiente se extrae del programa Pipedemo incluido con Platform Software Development Kit (SDK).


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



En este ejemplo se incluye el archivo de encabezado generado por el compilador MIDL. Para obtener más información, [vea Definición de canalizaciones en archivos IDL.](defining-pipes-in-idl-files.md) También declara una variable que usa como origen de datos denominado globalPipeData. La variable globalBuffer es un búfer que el procedimiento de extracción usa para enviar los bloques de datos que obtiene de globalPipeData.

La función SendLongs declara la canalización de entrada y asigna memoria para la variable de origen de datos globalPipeData. En el programa cliente/servidor, el origen de datos puede ser un archivo o estructura que el cliente crea. También puede hacer que el programa cliente obtenga datos del servidor, los procese y los devuelva al servidor mediante una canalización de entrada. En este sencillo ejemplo, el origen de datos es un búfer asignado dinámicamente de enteros largos.

Antes de que pueda comenzar la transferencia, el cliente debe establecer punteros a la variable de estado, al procedimiento de extracción y al procedimiento de asignación. Estos punteros se mantienen en la variable de canalización que declara el cliente. En este caso, SendLongs declara inPipe. Puede usar cualquier tipo de datos adecuado para la variable de estado.

Los clientes inician transferencias de datos a través de una canalización mediante la invocación de un procedimiento remoto en el servidor. Llamar al procedimiento remoto indica al programa de servidor que el cliente está listo para transmitir. A continuación, el servidor puede extraer los datos a sí mismo. En este ejemplo se invoca un procedimiento remoto denominado InPipe. Una vez transferidos los datos al servidor, la función SendLongs libera el búfer asignado dinámicamente.

En lugar de asignar memoria cada vez que se necesita un búfer. El procedimiento alloc de este ejemplo simplemente establece un puntero a la variable globalBuffer. El procedimiento de extracción reutiliza este búfer cada vez que transfiere datos. Es posible que los programas cliente más complejos necesiten asignar un nuevo búfer cada vez que el servidor extrae datos del cliente.

El código auxiliar del cliente llama al procedimiento de extracción. El procedimiento de extracción de este ejemplo usa la variable de estado para realizar el seguimiento de la siguiente posición en el búfer del origen de datos global del que se va a leer. Lee datos del búfer de origen en el búfer de canalización. El código auxiliar del cliente transmite los datos al servidor. Cuando se han enviado todos los datos, el procedimiento de extracción establece el tamaño del búfer en cero. Esto indica al servidor que deje de extraer datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Pipa](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 