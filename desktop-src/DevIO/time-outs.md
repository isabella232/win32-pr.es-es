---
description: Un identificador de un recurso de comunicaciones tiene un conjunto asociado de parámetros de tiempo de espera que afectan al comportamiento de las operaciones de lectura y escritura.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Tiempos de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db31fafc0f4d98832f1fb7fa5d22b32cba33d73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807400"
---
# <a name="time-outs"></a>Tiempos de espera

Un identificador de un recurso de comunicaciones tiene un conjunto asociado de parámetros de tiempo de espera que afectan al comportamiento de las operaciones de lectura y escritura. Los tiempos de espera pueden provocar que una operación [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) finalice cuando transcurre un intervalo de tiempo de espera, aunque no se haya leído o escrito el número especificado de caracteres. No se trata como un error cuando se produce un tiempo de espera durante una operación de lectura o escritura (es decir, el valor devuelto de la función de lectura o escritura indica Success). El recuento de bytes leídos o escritos realmente lo detecta **readfile** o **WriteFile** (o la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , si la e/s se realizó como una operación superpuesta).

Cuando una aplicación abre un recurso de comunicaciones, el sistema establece los valores de tiempo de espera del recurso en los valores en vigor cuando se utilizó por última vez el recurso. Si nunca se ha abierto el recurso de comunicaciones, el sistema establece los valores de tiempo de espera en algún valor predeterminado. En cualquier caso, una aplicación siempre debe determinar los valores de tiempo de espera actuales después de abrir el recurso y, a continuación, establecerlos explícitamente para satisfacer sus requisitos. Para determinar los valores de tiempo de espera actuales de un recurso de comunicaciones, utilice la función [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) . Para cambiar los valores de tiempo de espera, utilice la función [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) .

Los parámetros de tiempo de espera habilitan dos tipos de tiempos de espera. Se produce un tiempo de espera de intervalo cuando el tiempo transcurrido entre la recepción de dos caracteres cualesquiera supera un número especificado de milisegundos. El tiempo se inicia cuando se recibe el primer carácter y se reinicia cuando se recibe cada nuevo carácter. Se produce un tiempo de espera total cuando la cantidad total de tiempo consumida por una operación de lectura supera un número calculado de milisegundos. El tiempo se inicia inmediatamente cuando comienza la operación de e/s. Las operaciones de escritura solo admiten tiempos de espera totales. Las operaciones de lectura admiten tanto el intervalo como los tiempos de espera totales, que se pueden usar por separado o combinados.

El tiempo, en milisegundos, del período de tiempo de espera total para una operación de lectura o escritura se calcula mediante el multiplicador y los valores constantes de la estructura [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) especificada en la función [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) o [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) . Se usa la siguiente fórmula:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



El uso de un multiplicador y una constante permite que el período de tiempo de espera total varíe, en función de la cantidad de datos que se solicitan. Una aplicación solo puede utilizar la constante estableciendo el multiplicador en cero, o usar solo el multiplicador estableciendo la constante en cero. Si tanto la constante como el multiplicador son cero, no se utiliza el tiempo de espera total.

Si todos los parámetros de tiempo de espera de lectura son cero, los tiempos de espera de lectura no se usan y no se completa una operación de lectura hasta que se haya leído el número solicitado de bytes o se produzca un error. Del mismo modo, si todos los parámetros de tiempo de espera de escritura son cero, no se completa una operación de escritura hasta que se haya escrito el número de bytes solicitado o se produzca un error.

Si el parámetro de tiempo de espera de intervalo de lectura es el valor **MAXDWORD** y los parámetros de tiempo de espera de lectura total son cero, una operación de lectura se completa inmediatamente después de leer los caracteres que están disponibles en el búfer de entrada, incluso si está vacío.

El intervalo de tiempo obliga a que se devuelva una operación de lectura cuando hay un periodo en recepción. Un proceso que usa los tiempos de espera de intervalo puede establecer un parámetro de intervalo bastante corto, de modo que pueda responder rápidamente a ráfagas aisladas de uno o algunos caracteres, aunque puede recopilar grandes búferes de caracteres con una sola llamada cuando los datos se reciben en una secuencia estable.

Los tiempos de espera de una operación de escritura pueden ser útiles cuando la transmisión está bloqueada por algún tipo de control de flujo o cuando se ha llamado a la función [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) para suspender la transmisión de caracteres.

En la tabla siguiente se resume el comportamiento de las operaciones de lectura en función de los valores especificados para los tiempos de espera totales e intervalos.



| Total | Intervalo | Comportamiento                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Devuelve cuando el búfer se rellena completamente. Los tiempos de espera no se usan.                                                                                                                    |
| T     | 0        | Devuelve cuando el búfer se rellena completamente o cuando se han transcurrido T milisegundos desde el inicio de la operación.                                                                   |
| 0     | Y        | Devuelve cuando el búfer se rellena completamente o cuando se han transcurrido Y milisegundos entre la recepción de dos caracteres cualesquiera. El tiempo no comienza hasta que se recibe el primer carácter. |
| T     | Y        | Devuelve cuando el búfer se rellena completamente o cuando se produce un tipo de tiempo de espera.                                                                                                     |



 

> [!Note]  
> Sin embargo, ese tiempo es relativo al sistema que controla el dispositivo físico. Para un dispositivo remoto, como un módem, el tiempo es relativo al sistema del servidor al que está conectado el módem. Cualquier retraso de propagación de red no se factoriza en. Por ejemplo, una aplicación cliente podría especificar un tiempo de espera total que se calcula como 500 milisegundos. Cuando han transcurrido 500 milisegundos en el servidor, se devuelve al cliente un error de tiempo de espera. Si hay un retraso de propagación de la red de 50 milisegundos, el cliente no recibirá ninguna notificación del tiempo de espera hasta aproximadamente 50 milisegundos después del tiempo de espera realmente producido.

 

> [!Note]  
> Los parámetros de tiempo de espera afectan al comportamiento de las operaciones de lectura y escritura superpuestas en un dispositivo de comunicaciones. Con e/s superpuestas, la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) puede devolver antes de que se haya completado la operación. Los parámetros de tiempo de espera pueden determinar cuándo se ha completado la operación.

 

 

 
