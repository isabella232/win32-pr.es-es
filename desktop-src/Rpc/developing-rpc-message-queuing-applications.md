---
title: Desarrollo de aplicaciones de RPC-Message Queue Server
description: Es necesario muy poco esfuerzo para aprovechar el transporte de MSMQ en la aplicación RPC.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- RPC llamada a procedimiento remoto, tareas, desarrollar aplicaciones de Message Queue Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e51707c0a6903200e51dd35e50e998430c8eae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078258"
---
# <a name="developing-rpc-message-queuing-applications"></a>Desarrollo de aplicaciones de RPC-Message Queue Server

Es necesario muy poco esfuerzo para aprovechar el transporte de MSMQ en la aplicación RPC. En el caso de la mensajería sincrónica, solo es necesario especificar el transporte de la cola de mensajes ([**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq)) como la secuencia de protocolos. El **Protocolo \_ MQ de ncadg** admite todas las características de datagramas estándar, excepto las llamadas de difusión. Además, tenga en cuenta que, actualmente, el transporte de cola de mensajes no admite puntos de conexión dinámicos.

Al aplicar el \[ [](/windows/desktop/Midl/message) \] atributo Message a las declaraciones de procedimiento remoto en el archivo IDL, se implementa automáticamente Message Queue Server para esas llamadas. Esto permite que las aplicaciones cliente y servidor controlen muchas de las propiedades asociadas a mensajes y colas de mensajes, entre las que se incluyen:

-   Calidad de servicio
-   Confirmación de recepción
-   Registro en diario
-   Prioridad de llamada
-   Persistencia de la cola de procesos del servidor

La calidad de servicio es el esfuerzo que realizará el transporte para proporcionar la llamada al proceso de servidor. Una entrega rápida se pondrá en cola en la memoria, por lo que es bastante rápida, pero se perderá la llamada si un equipo o una conexión de red deja de funcionar en el momento equivocado. Una entrega recuperable se publicará en un archivo de disco hasta que se entregue, por lo que no se perderá la llamada, incluso en caso de que se produzca un bloqueo del equipo. Esto proporciona una entrega garantizada, pero a un costo de rendimiento, ya que cada llamada se escribe en el disco.

También puede indicar al transporte de MSMQ que espere la confirmación de que la llamada llegó a la cola de destino (servidor) antes de devolver. Al elegir esta opción, el cliente se bloquea hasta que el servidor confirma la llamada; de lo contrario, el control vuelve al cliente inmediatamente después de realizar la llamada.

Mediante el uso del registro en diario, se pueden registrar llamadas en el disco. Si el registro en diario está activado, cada llamada se registra en el disco a medida que se transmite al próximo salto al proceso del servidor.

La prioridad de llamada se puede usar junto con el \[ atributo de función de [**mensaje**](/windows/desktop/Midl/message) RPC para permitir que las \] llamadas con mayor prioridad tengan prioridad sobre las llamadas con menor prioridad, incluso si las llamadas de prioridad alta llegan más tarde. La prioridad de la llamada también funcionará de manera limitada con RPC sincrónico, pero las llamadas RPC sincrónicas no se pueden apilar de la misma manera que las llamadas asincrónicas.

El proceso de cliente controla todas las propiedades anteriores mediante una llamada a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Una vez establecidas, estas propiedades permanecen en vigor hasta que se cambian en otra llamada a **RpcBindingSetOption**.

El proceso de servidor RPC puede controlar la duración de su cola de recepción. De forma predeterminada, la cola se elimina cuando finaliza el proceso del servidor. Sin embargo, el proceso de servidor puede usar [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) al configurar su punto de conexión para indicar al transporte que permita que la cola continúe existiendo y acepte solicitudes de llamada incluso cuando el proceso de servidor no se está ejecutando. En este caso, las llamadas se ponen en cola y se ejecutan más adelante, cuando el proceso del servidor vuelve a estar en línea.

> [!Note]  
> Si utiliza llamadas asincrónicas a \[ [**mensajes**](/windows/desktop/Midl/message) \] en una interfaz, debe registrar la interfaz llamando a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) antes de llamar a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ MQ)**. Una vez que se activa la secuencia de protocolos, las llamadas que ya esperan en la cola del servidor comenzarán a leerse en la cola. Si no se ha registrado la interfaz RPC correspondiente, se producirá un error en las llamadas. Esta situación puede producirse si tiene una configuración de un punto de conexión permanente para las llamadas a procedimientos remotos, se ha cerrado el servidor y los clientes han continuado enviando llamadas al servidor. Estas llamadas se apilarán en la cola, en espera de ser leídas una vez que el servidor vuelva a estar en línea.

 

Para obtener más información, vea [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)y \[ [**Message**](/windows/desktop/Midl/message) \] , [**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq).

 

 