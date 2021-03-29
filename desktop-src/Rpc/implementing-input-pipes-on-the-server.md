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
# <a name="implementing-input-pipes-on-the-server"></a>Implementar canalizaciones de entrada en el servidor

Para empezar a enviar datos a un servidor, un cliente llama a uno de los procedimientos remotos del servidor. Este procedimiento debe llamar repetidamente al procedimiento de extracción en el código auxiliar del servidor. El compilador MIDL usa el archivo IDL de la aplicación para generar automáticamente el procedimiento de extracción del servidor.

Cada vez que el programa de servidor invoca el procedimiento de extracción en su código auxiliar, el procedimiento de extracción recibe bloques de datos del cliente. No calcula las referencias de los datos en el búfer del servidor. Después, el procedimiento remoto del servidor puede procesar estos datos de la forma que sea necesario. El bucle continúa hasta que el servidor recibe un búfer de longitud cero.

El ejemplo siguiente es del programa Pipedemo incluido en los ejemplos que se incluyen con el kit de desarrollo de software (SDK) de la plataforma. Muestra un procedimiento de servidor remoto que usa una canalización para extraer datos del cliente al servidor.

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

 

 




