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
# <a name="implementing-output-pipes-on-the-server"></a>Implementación de canalizaciones de salida en el servidor

Para empezar a recibir datos de un servidor, un cliente llama a uno de los procedimientos remotos del servidor. Este procedimiento debe llamar repetidamente al procedimiento de extracción en el código auxiliar del servidor. El compilador MIDL usa el archivo IDL de la aplicación para generar automáticamente el procedimiento de instalación del servidor.

La rutina del servidor remoto debe rellenar los datos del búfer de la canalización de salida antes de llamar al procedimiento de extracción. Cada vez que el programa de servidor invoca el procedimiento de extracción en su código auxiliar, el procedimiento de envío calcula las referencias de los datos y los transmite al cliente. El bucle continúa hasta que el servidor envía un búfer de longitud cero.

El ejemplo siguiente es del programa Pipedemo incluido en los ejemplos incluidos en el Windows SDK. Muestra un procedimiento de servidor remoto que usa una canalización para insertar datos del servidor en el cliente.


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

[codo](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 