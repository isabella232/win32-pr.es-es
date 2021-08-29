---
title: Desarrollo de RPC-Message queuing applications
description: Se requiere muy poco esfuerzo para aprovechar el transporte de MSMQ en la aplicación RPC.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- Llamada a procedimiento remoto RPC, tareas, desarrollo de aplicaciones de cola de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cf7b3a5d6d33facebb1de6a3c0f37eb9ba48f2afa54e6143ad5cb0169ad601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930578"
---
# <a name="developing-rpc-message-queuing-applications"></a>Desarrollo de RPC-Message queuing applications

Se requiere muy poco esfuerzo para aprovechar el transporte de MSMQ en la aplicación RPC. Para la mensajería sincrónica, solo debe especificar el transporte de la cola de mensajes [**(ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq)) como secuencia de protocolo. El **protocolo ncadg \_ mq** admite todas las características de datagrama estándar, excepto las llamadas de difusión. Además, tenga en cuenta que actualmente el transporte de cola de mensajes no admite puntos de conexión dinámicos.

Al aplicar el atributo message a las declaraciones de procedimiento remoto en el archivo IDL, se implementa automáticamente la puesta en cola de mensajes en modo asincrónico \[ [](/windows/desktop/Midl/message) \] para esas llamadas. Esto permite que las aplicaciones cliente y servidor controle muchas de las propiedades asociadas a mensajes y colas de mensajes, entre las que se incluyen:

-   Calidad del servicio
-   Confirmación del recibo
-   Registro en el diario
-   Prioridad de llamada
-   Persistencia de la cola de procesos de servidor

La calidad del servicio es el esfuerzo que realizará el transporte para entregar la llamada al proceso del servidor. Una entrega rápida se pondrá en cola en memoria, por lo que es bastante rápida, pero la llamada se perderá si un equipo o una conexión de red se queda sin conexión en el momento incorrecto. Una entrega recuperable se publicará en un archivo de disco hasta que se entregue, por lo que la llamada no se perderá, incluso en caso de bloqueo del equipo. Esto proporciona una entrega garantizada, pero a un costo de rendimiento, ya que cada llamada se escribe en el disco.

También puede decir al transporte de MSMQ que espere la confirmación de que la llamada alcanzó la cola de destino (servidor) antes de volver. Al elegir esta opción, se bloquea el cliente hasta que el servidor confirma la llamada; de lo contrario, el control vuelve al cliente inmediatamente después de realizar la llamada.

Mediante el uso del registro en diario, las llamadas se pueden registrar en el disco. Si el registro en diario está activado, cada llamada se registra en el disco a medida que se transmite al próximo salto en su camino al proceso del servidor.

La prioridad de llamada se puede usar junto con el atributo de función de mensaje RPC para permitir que las llamadas con mayor prioridad tengan prioridad sobre las llamadas con prioridad más baja, incluso si las llamadas de prioridad alta llegan más \[ [](/windows/desktop/Midl/message) \] adelante. La prioridad de llamada también funcionará de forma limitada con RPC sincrónica, pero las llamadas RPC sincrónicas no se pueden apilar de la misma manera que las llamadas asincrónicas.

El proceso de cliente controla todas las propiedades anteriores llamando a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Una vez establecidas, estas propiedades permanecen en vigor hasta que se cambian en otra llamada a **RpcBindingSetOption**.

El proceso del servidor RPC puede controlar la duración de su cola de recepción. De forma predeterminada, la cola se elimina cuando se cierra el proceso de servidor. Sin embargo, el proceso de servidor puede usar [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) al configurar su punto de conexión para que el transporte permita que la cola siga existiendo y acepte solicitudes de llamada incluso cuando el proceso del servidor no se está ejecutando. En este caso, las llamadas se ponen en cola y se ejecutan más adelante, cuando el proceso del servidor vuelve a estar en línea.

> [!Note]  
> Si usa llamadas de mensaje asincrónicas en una interfaz, debe registrar la interfaz llamando \[ [](/windows/desktop/Midl/message) \] a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) antes de llamar a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ mq).** Una vez que active la secuencia de protocolo, las llamadas que ya están esperando en la cola para el servidor comenzarán a leerse de la cola. Si no se ha registrado la interfaz RPC correspondiente, se producirá un error en las llamadas. Esta situación puede ocurrir si tiene un punto de conexión permanente para las llamadas a procedimiento remoto, el servidor se ha apagado y los clientes han continuado con el envío de llamadas al servidor. Estas llamadas se apilarán en la cola, a la espera de que se lean una vez que el servidor vuelva a estar en línea.

 

Para obtener más información, [**vea RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)y el mensaje \[ [](/windows/desktop/Midl/message) \] , [**ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq).

 

 