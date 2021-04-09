---
title: Escalabilidad
description: Escalabilidad
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Escalabilidad
- Llamada a procedimiento remoto RPC, procedimientos recomendados, escalabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0728e35d9c9b27494014363c448be9965e39eea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903770"
---
# <a name="scalability"></a>Escalabilidad

El término, la escalabilidad, se suele usar infrecuentemente. En esta sección, se proporciona una definición dual:

-   La escalabilidad es la capacidad de aprovechar al máximo la potencia de procesamiento disponible en un sistema de varios procesadores (2, 4, 8, 32 o más procesadores).
-   La escalabilidad es la capacidad de atender un gran número de clientes.

Estas dos definiciones relacionadas se conocen comúnmente como *escalado* vertical. Al final de este tema se proporcionan sugerencias sobre el *escalado* horizontal.

Esta explicación se centra exclusivamente en la escritura de servidores escalables, no en clientes escalables, ya que los servidores escalables son requisitos más comunes. En esta sección también se trata la escalabilidad en el contexto de los servidores RPC y RPC únicamente. Aquí no se describen los procedimientos recomendados para la escalabilidad, como la reducción de la contención, la prevención de errores de caché frecuentes en ubicaciones de memoria globales o la prevención del uso compartido falso.

## <a name="rpc-threading-model"></a>Modelo de subprocesos RPC

Cuando un servidor recibe una llamada RPC, se llama a la rutina de servidor (rutina Manager) en un subproceso proporcionado por RPC. RPC utiliza un grupo de subprocesos adaptable que aumenta y disminuye a medida que la carga de trabajo fluctúa. A partir de Windows 2000, el núcleo del grupo de subprocesos RPC es un puerto de finalización. El puerto de finalización y su uso por parte de RPC están optimizados para las rutinas de servidor de contención cero a bajo. Esto significa que el grupo de subprocesos RPC aumenta de forma agresiva el número de subprocesos de servicio si algunos se bloquean. Funciona en la presunción de que el bloqueo es poco frecuente y, si se bloquea un subproceso, se trata de una condición temporal que se resuelve rápidamente. Este enfoque permite la eficacia de los pocos servidores de contención. Por ejemplo, un servidor RPC de llamada void que opere en un servidor 550MHz de ocho procesadores al que se tiene acceso a través de una red de área de sistema (SAN) de alta velocidad realiza más de 30.000 llamadas void por segundo desde más de 200 clientes remotos. Esto representa más de 108 millones llamadas por hora.

El resultado es que el grupo de subprocesos agresivo realmente se obtiene en la forma en que la contención en el servidor es alta. Para ilustrar, Imagine un servidor con un gran arancel que se usa para acceder a los archivos de forma remota. Suponga que el servidor adopta el enfoque más directo: simplemente lee/escribe el archivo sincrónicamente en el subproceso en el que RPC invoca la rutina de servidor. Además, supongamos que tenemos un servidor de cuatro procesadores que atiende a muchos clientes.

El servidor se iniciará con cinco subprocesos (esto varía realmente, pero se usan cinco subprocesos por simplicidad). Una vez que RPC recoge la primera llamada RPC, envía la llamada a la rutina de servidor y la rutina de servidor emite la e/s. Con poca frecuencia, se pierde la memoria caché de archivos y, a continuación, se bloquea la espera del resultado. En cuanto se bloquea, el quinto subproceso se libera para recoger una solicitud y se crea un sexto subproceso como un estado de espera activa. Suponiendo que cada décima operación de e/s pierda la memoria caché y se bloqueará durante 100 milisegundos (un valor de tiempo arbitrario), y suponiendo que el servidor de cuatro procesadores atiende las 20.000 llamadas por segundo (5.000 llamadas por procesador), un modelado simplista predecirá que cada procesador generará aproximadamente los subprocesos de 50. Se supone que se trata de una llamada que bloqueará cada 2 milisegundos y, después de 100 milisegundos, el primer subproceso se libera de nuevo para que el grupo se estabilice en unos 200 subprocesos (50 por procesador).

El comportamiento real es más complicado, ya que el número alto de subprocesos producirá cambios de contexto adicionales que ralentizan el servidor y también ralentizan la velocidad de creación de nuevos subprocesos, pero la idea básica está clara. El número de subprocesos aumenta rápidamente a medida que los subprocesos del servidor inician el bloqueo y esperan algo (es decir, una e/s o el acceso a un recurso).

RPC y el puerto de finalización que las solicitudes entrantes intentarán mantener el número de subprocesos RPC que se pueden usar en el servidor para que sea igual al número de procesadores de la máquina. Esto significa que en un servidor de cuatro procesadores, una vez que un subproceso vuelve a RPC, si hay cuatro o más subprocesos RPC que se pueden usar, el quinto subproceso no tiene permiso para recopilar una nueva solicitud y, en su lugar, se quedará en estado de espera activa en caso de que uno de los subprocesos que se puedan usar actualmente sea. Si el quinto subproceso espera el tiempo suficiente como un estado de espera activa sin el número de subprocesos RPC que se pueden usar y se quita por debajo del número de procesadores, se liberará, es decir, el grupo de subprocesos disminuirá.

Imagine un servidor con muchos subprocesos. Como se explicó anteriormente, un servidor RPC termina con muchos subprocesos, pero solo si los subprocesos se bloquean a menudo. En un servidor en el que los subprocesos se bloquean a menudo, un subproceso que vuelve a RPC se saca pronto de la lista de espera activa, porque todos los subprocesos que se pueden usar actualmente se bloquean y se le proporciona una solicitud para procesar. Cuando un subproceso se bloquea, el distribuidor de subprocesos en el kernel cambia el contexto a otro subproceso. Este cambio de contexto solo consume ciclos de CPU. El subproceso siguiente ejecutará código diferente, tendrá acceso a estructuras de datos diferentes y tendrá una pila diferente, lo que significa que la tasa de aciertos de la memoria caché (las cachés L1 y L2) será mucho menor, lo que dará lugar a una ejecución más lenta. Los numerosos subprocesos que se ejecutan simultáneamente aumentan la contención de los recursos existentes, como el montón, las secciones críticas en el código del servidor, etc. Esto aumenta aún más la contención en el formulario de recursos. Si la memoria es baja, la presión de memoria ejercida por el número grande y creciente de subprocesos producirá errores de página, que aumentarán aún más la velocidad a la que se bloquean los subprocesos y provocarán que se creen incluso más subprocesos. En función de la frecuencia con que se bloquee y de la cantidad de memoria física disponible, el servidor puede estabilizarse con un nivel de rendimiento inferior con una tasa de cambio de contexto alta o puede deteriorarse hasta el punto en el que solo se accede repetidamente al disco duro y al cambio de contexto sin realizar ningún trabajo real. Esta situación no se mostrará en la carga de trabajo ligera, por supuesto, pero una carga de trabajo pesada pone el problema rápidamente en la superficie.

¿Cómo se puede evitar esto? Si se espera que los subprocesos se bloqueen, declare llamadas como asincrónicas y, una vez que la solicitud entre en la rutina del servidor, colóquelo en un grupo de subprocesos de trabajo que usen las capacidades asincrónicas del sistema de e/s y/o RPC. Si el servidor, a su vez, hace que las llamadas RPC realicen esos asíncronos y asegúrese de que la cola no crezca demasiado. Si la rutina de servidor está realizando la e/s de archivos, use la e/s asincrónica de archivos para poner en cola varias solicitudes en el sistema de e/s y tener solo unos pocos subprocesos en cola y recoger los resultados. Si la rutina de servidor está realizando una e/s de red, utilice de nuevo las capacidades asincrónicas del sistema para emitir las solicitudes y recoger las respuestas de forma asincrónica y usar el menor número posible de subprocesos. Cuando se realiza la e/s, o cuando se completa la llamada RPC realizada por el servidor, complete la llamada RPC asincrónica que entregó la solicitud. Esto permitirá que el servidor se ejecute con el menor número posible de subprocesos, lo que aumenta el rendimiento y el número de clientes que puede atender un servidor.

## <a name="scale-out"></a>Escalabilidad horizontal

RPC puede configurarse para que funcione con equilibrio de carga de red (NLB) si se configura NLB de modo que todas las solicitudes de una dirección de cliente determinada vayan al mismo servidor. Dado que cada cliente RPC abre un grupo de conexiones (para obtener más información, consulte [RPC y la red](rpc-and-the-network.md)), es fundamental que todas las conexiones desde el grupo del cliente determinado terminen en el mismo equipo servidor. Siempre que se cumpla esta condición, se puede configurar un clúster NLB para que funcione como un servidor RPC de gran tamaño con una escalabilidad potencialmente excelente.

 

 




