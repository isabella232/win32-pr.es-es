---
title: Escalabilidad
description: Escalabilidad
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Escalabilidad
- Llamada a procedimiento remoto RPC, procedimientos recomendados, escalabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2a004a5ce3adb0f27e2e31071cac69fc1c34bfc650c618dcf39b3c8ebc954f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018065"
---
# <a name="scalability"></a>Escalabilidad

A menudo se usa incorrectamente el término escalabilidad. En esta sección, se proporciona una definición dual:

-   La escalabilidad es la capacidad de utilizar totalmente la potencia de procesamiento disponible en un sistema de varios procesadores (2, 4, 8, 32 o más procesadores).
-   La escalabilidad es la capacidad de dar servicio a un gran número de clientes.

Estas dos definiciones relacionadas se conocen normalmente como *escalado vertical.* Al final de este tema se proporcionan sugerencias sobre *el escalado horizontal.*

Esta discusión se centra exclusivamente en escribir servidores escalables, no en clientes escalables, porque los servidores escalables son requisitos más comunes. En esta sección también se trata la escalabilidad solo en el contexto de los servidores RPC y RPC. Aquí no se analizan los procedimientos recomendados para la escalabilidad, como reducir la contención, evitar errores frecuentes de caché en ubicaciones de memoria global o evitar el uso compartido falso.

## <a name="rpc-threading-model"></a>Modelo de subprocesos RPC

Cuando un servidor recibe una llamada RPC, se llama a la rutina de servidor (rutina de administrador) en un subproceso proporcionado por RPC. RPC usa un grupo de subprocesos adaptable que aumenta y disminuye a medida que fluctúa la carga de trabajo. A partir Windows 2000, el núcleo del grupo de subprocesos RPC es un puerto de finalización. El puerto de finalización y su uso por RPC están optimizados para rutinas de servidor de contención de cero a baja. Esto significa que el grupo de subprocesos RPC aumenta agresivamente el número de subprocesos de mantenimiento si algunos se bloquean. Funciona con la sospecha de que el bloqueo es poco frecuente y, si se bloquea un subproceso, se trata de una condición temporal que se resuelve rápidamente. Este enfoque permite la eficacia de los servidores de contención baja. Por ejemplo, un servidor RPC de llamada void que funciona en un servidor de 550 MHz de ocho procesadores al que se accede a través de una red de área de sistema (SAN) de alta velocidad atiende más de 30 000 llamadas nulas por segundo desde más de 200 clientes remotos. Esto representa más de 108 millones de llamadas por hora.

El resultado es que el grupo de subprocesos agresivo se pone realmente en el camino cuando la contención en el servidor es alta. Para ilustrar esto, imagine un servidor de servicio pesado que se usa para acceder a los archivos de forma remota. Suponga que el servidor adopta el enfoque más sencillo: simplemente lee o escribe el archivo sincrónicamente en el subproceso en el que RPC invoca la rutina del servidor. Además, suponga que tenemos un servidor de cuatro procesadores que atiende a muchos clientes.

El servidor comenzará con cinco subprocesos (esto varía realmente, pero se usan cinco subprocesos por motivos de simplicidad). Una vez que RPC toma la primera llamada RPC, envía la llamada a la rutina de servidor y la rutina de servidor emite la E/S. Con poca frecuencia, se pierde la caché de archivos y, a continuación, se bloquea la espera del resultado. En cuanto se bloquea, se libera el quinto subproceso para recoger una solicitud y se crea un sexto subproceso como espera activa. Suponiendo que cada décima operación de E/S pierde la memoria caché y se bloqueará durante 100 milisegundos (un valor de tiempo arbitrario) y suponiendo que el servidor de cuatro procesadores atiende aproximadamente 20 000 llamadas por segundo (5000 llamadas por procesador), un modelado simplista predice que cada procesador genera aproximadamente 50 subprocesos. Esto supone que una llamada que se bloqueará se produce cada 2 milisegundos y, después de 100 milisegundos, el primer subproceso se libera de nuevo para que el grupo se estabilice en unos 200 subprocesos (50 por procesador).

El comportamiento real es más complicado, ya que el gran número de subprocesos provocará cambios de contexto adicionales que ralentizarán el servidor y también ralentizarán la velocidad de creación de nuevos subprocesos, pero la idea básica es clara. El número de subprocesos sube rápidamente a medida que los subprocesos del servidor empiezan a bloquearse y a esperar algo (ya sea una E/S o el acceso a un recurso).

RPC y el puerto de finalización que cancela las solicitudes entrantes intentarán mantener el número de subprocesos RPC utilizables en el servidor para que sea igual al número de procesadores de la máquina. Esto significa que, en un servidor de cuatro procesadores, una vez que un subproceso vuelve a RPC, si hay cuatro o más subprocesos RPC utilizables, el quinto subproceso no puede recoger una nueva solicitud y, en su lugar, se encontrará en estado de espera activa en caso de que uno de los bloques de subprocesos que se puedan usar actualmente. Si el quinto subproceso espera lo suficiente como espera activa sin que el número de subprocesos RPC utilizables se reduzca por debajo del número de procesadores, se liberará, es decir, el grupo de subprocesos disminuirá.

Imagine un servidor con muchos subprocesos. Como se explicó anteriormente, un servidor RPC termina con muchos subprocesos, pero solo si los subprocesos se bloquean con frecuencia. En un servidor en el que los subprocesos a menudo se bloquean, un subproceso que vuelve a RPC pronto se sale de la lista de espera activa, porque todos los subprocesos que se pueden usar actualmente se bloquean y se le da una solicitud para procesar. Cuando un subproceso se bloquea, el distribuidor de subprocesos del kernel cambia el contexto a otro subproceso. Este cambio de contexto por sí solo consume ciclos de CPU. El siguiente subproceso va a ejecutar código diferente, acceder a diferentes estructuras de datos y tendrá una pila diferente, lo que significa que la tasa de aciertos de caché de memoria (las cachés L1 y L2) será mucho menor, lo que dará lugar a una ejecución más lenta. Los numerosos subprocesos que se ejecutan simultáneamente aumentan la contención de los recursos existentes, como el montón, las secciones críticas en el código del servidor, y así sucesivamente. Esto aumenta aún más la contención a medida que se forman convoyes en recursos. Si la memoria es baja, la presión de memoria que el número grande y creciente de subprocesos provocan errores en la página, lo que aumenta aún más la velocidad a la que se bloquean los subprocesos y hace que se cree incluso más subprocesos. Dependiendo de la frecuencia con la que se bloquee y la cantidad de memoria física disponible, el servidor puede estabilizarse en un nivel inferior de rendimiento con una alta tasa de cambio de contexto, o puede que se deterioren hasta el punto en que solo accede repetidamente al disco duro y al cambio de contexto sin realizar ningún trabajo real. Esta situación no se mostrará bajo una carga de trabajo ligera, por supuesto, pero una carga de trabajo pesada lleva rápidamente el problema a la superficie.

¿Cómo se puede evitar esto? Si se espera que los subprocesos se bloqueen, declare las llamadas como asincrónicas y, una vez que la solicitud entra en la rutina del servidor, en cola en un grupo de subprocesos de trabajo que usan las funcionalidades asincrónicas del sistema de E/S o RPC. Si el servidor, a su vez, realiza llamadas RPC, realiza esas llamadas asincrónicas y asegúrese de que la cola no crezca demasiado. Si la rutina de servidor realiza E/S de archivos, use E/S de archivo asincrónica para poner en cola varias solicitudes en el sistema de E/S y hacer que solo unos pocos subprocesos las en cola y recogen los resultados. Si la rutina de servidor está realizando E/S de red, de nuevo, use las funcionalidades asincrónicas del sistema para emitir las solicitudes y recoger las respuestas de forma asincrónica y usar el menor número posible de subprocesos. Cuando se complete la E/S o la llamada RPC realizada al servidor, complete la llamada RPC asincrónica que entregó la solicitud. Esto permitirá que el servidor se ejecute con el menor número de subprocesos posible, lo que aumenta el rendimiento y el número de clientes que un servidor puede dar servicio.

## <a name="scale-out"></a>Escalabilidad horizontal

RPC se puede configurar para que funcione con equilibrio de carga de red (NLB) si NLB está configurado de forma que todas las solicitudes de una dirección de cliente determinada vayan al mismo servidor. Dado que cada cliente RPC abre un grupo de conexiones (para obtener más información, vea [RPC](rpc-and-the-network.md)y la red ), es esencial que todas las conexiones del grupo del cliente determinado terminen en el mismo equipo servidor. Siempre que se cumple esta condición, se puede configurar un clúster NLB para que funcione como un servidor RPC grande con una escalabilidad potencialmente excelente.

 

 




