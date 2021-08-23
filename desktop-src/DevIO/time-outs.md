---
description: Un identificador de un recurso de comunicaciones tiene un conjunto asociado de parámetros de tiempo de espera que afectan al comportamiento de las operaciones de lectura y escritura.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Tiempos de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6226e8a2d13020bd4dc90a416e7ef359fbd919cf54e886c5e691e5fca2cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956794"
---
# <a name="time-outs"></a>Tiempos de espera

Un identificador de un recurso de comunicaciones tiene un conjunto asociado de parámetros de tiempo de espera que afectan al comportamiento de las operaciones de lectura y escritura. Los tiempos de espera pueden hacer que una operación [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx,**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) concluya cuando transcurra un intervalo de tiempo de espera, aunque el número especificado de caracteres no se haya leído ni escrito. No se trata como un error cuando se produce un tiempo de espera durante una operación de lectura o escritura (es decir, el valor devuelto de la función de lectura o escritura indica que se ha producido correctamente). ReadFile o **WriteFile** notifican  el recuento de bytes leídos o escritos realmente (o por la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**FileIOCompletionRoutine,**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) si la E/S se realizó como una operación superpuesta).

Cuando una aplicación abre un recurso de comunicaciones, el sistema establece los valores de tiempo de espera del recurso en los valores en vigor cuando se usó el recurso por última vez. Si el recurso de comunicaciones nunca se ha abierto, el sistema establece los valores de tiempo de espera en algún valor predeterminado. En cualquier caso, una aplicación siempre debe determinar los valores de tiempo de espera actuales después de abrir el recurso y, a continuación, establecerlos explícitamente para que cumplan sus requisitos. Para determinar los valores de tiempo de espera actuales de un recurso de comunicaciones, use la [**función GetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) Para cambiar los valores de tiempo de espera, use la [**función SetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)

Los parámetros de tiempo de espera habilitan dos tipos de tiempos de espera. Se produce un tiempo de espera de intervalo cuando el tiempo entre la recepción de dos caracteres cualquiera supera un número especificado de milisegundos. El tiempo se inicia cuando se recibe el primer carácter y se reinicia cuando se recibe cada nuevo carácter. Se produce un tiempo de espera total cuando la cantidad total de tiempo consumido por una operación de lectura supera un número calculado de milisegundos. El tiempo se inicia inmediatamente cuando comienza la operación de E/S. Las operaciones de escritura solo admiten tiempos de espera totales. Las operaciones de lectura admiten intervalos y tiempos de espera totales, que se pueden usar por separado o combinarse.

El tiempo, en milisegundos, del período de tiempo de espera total de una operación de lectura o escritura se calcula mediante el multiplicador y los valores constantes de la estructura [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) especificada en la función [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) o [**SetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) Se usa la siguiente fórmula:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



El uso de un multiplicador y una constante permite que el período de tiempo de espera total varíe en función de la cantidad de datos que se soliciten. Una aplicación solo puede usar la constante estableciendo el multiplicador en cero o utilizando solo el multiplicador estableciendo la constante en cero. Si la constante y el multiplicador son cero, no se usa el tiempo de espera total.

Si todos los parámetros de tiempo de espera de lectura son cero, no se usan tiempos de espera de lectura y no se completa una operación de lectura hasta que se haya leído el número de bytes solicitado o se produzca un error. Del mismo modo, si todos los parámetros de tiempo de espera de escritura son cero, no se completará una operación de escritura hasta que se haya escrito el número de bytes solicitado o se produzca un error.

Si el parámetro de tiempo de espera del intervalo de lectura es el valor **MAXDWORD** y ambos parámetros de tiempo de espera total de lectura son cero, se completa una operación de lectura inmediatamente después de leer los caracteres que están disponibles en el búfer de entrada, incluso si está vacío.

El intervalo de tiempo obliga a una operación de lectura a devolverse cuando hay un intervalo en la recepción. Un proceso que usa tiempos de espera de intervalo puede establecer un parámetro de intervalo bastante corto, por lo que puede responder rápidamente a ráfagas pequeñas y aisladas de uno o varios caracteres, pero todavía puede recopilar búferes grandes de caracteres con una sola llamada cuando se reciben datos en una secuencia estable.

Los tiempos de espera para una operación de escritura pueden ser útiles cuando algún tipo de control de flujo bloquea la transmisión o cuando se llama a la función [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) para suspender la transmisión de caracteres.

En la tabla siguiente se resume el comportamiento de las operaciones de lectura en función de los valores especificados para los tiempos de espera totales e intervalos.



| Total | Intervalo | Comportamiento                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Devuelve cuando el búfer se rellena completamente. No se usan tiempos de espera.                                                                                                                    |
| T     | 0        | Devuelve cuando el búfer se rellena completamente o cuando han transcurrido milisegundos de T desde el principio de la operación.                                                                   |
| 0     | Y        | Devuelve cuando el búfer se rellena completamente o cuando transcurren milisegundos Y entre la recepción de dos caracteres cualquiera. El tiempo no comienza hasta que se recibe el primer carácter. |
| T     | Y        | Devuelve cuando el búfer se rellena completamente o cuando se produce cualquier tipo de tiempo de espera.                                                                                                     |



 

> [!Note]  
> Sin embargo, ese tiempo es relativo al sistema que controla el dispositivo físico. Para un dispositivo remoto, como un módem, el tiempo es relativo al sistema de servidor al que está conectado el módem. No se tiene en cuenta ningún retraso de propagación de red. Por ejemplo, una aplicación cliente podría especificar un tiempo de espera total que calcula en 500 milisegundos. Cuando han transcurrido 500 milisegundos en el servidor, se devuelve un error de tiempo de espera al cliente. Si hay un retraso de propagación de red de 50 milisegundos, no se notificará al cliente el tiempo de espera hasta aproximadamente 50 milisegundos después de que se haya producido realmente el tiempo de espera.

 

> [!Note]  
> Los parámetros de tiempo de espera afectan al comportamiento de las operaciones de lectura y escritura superpuestas en un dispositivo de comunicaciones. Con la E/S superpuesta, la función [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) puede devolver antes de que se haya completado la operación. Los parámetros de tiempo de espera pueden determinar cuándo se ha completado la operación.

 

 

 
