---
title: Implementar canalizaciones de salida en el servidor
description: Para empezar a recibir datos de un servidor, un cliente llama a uno de los procedimientos remotos del servidor.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d93b2933499ca86ab49732d46cf2abe3c37247ed7bfa5e653e5aa0119b1e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020495"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implementar canalizaciones de salida en el servidor

Para empezar a recibir datos de un servidor, un cliente llama a uno de los procedimientos remotos del servidor. Este procedimiento debe llamar repetidamente al procedimiento de inserción en el código auxiliar del servidor. El compilador midl usa el archivo IDL de la aplicación para generar automáticamente el procedimiento de inserción del servidor.

La rutina del servidor remoto debe rellenar el búfer de la canalización de salida con datos antes de llamar al procedimiento de inserción. Cada vez que el programa de servidor invoca el procedimiento de inserción en su código auxiliar, el procedimiento de inserción serializa los datos y los transmite al cliente. El bucle continúa hasta que el servidor envía un búfer de longitud cero.

El ejemplo siguiente procede del programa Pipedemo incluido en los ejemplos que se incluyen con el SDK de Windows. Muestra un procedimiento de servidor remoto que usa una canalización para insertar datos desde el servidor al cliente.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Pipa](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 