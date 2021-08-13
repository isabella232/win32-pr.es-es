---
description: El servicio de componentes en cola de COM+ mejora el modelo de programación COM al proporcionar un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o asincrónicamente (en cola).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Arquitectura de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93914fd82a14c73b134098a759c8d61e324b6cda65d03de23f9c3ea2fcfb53f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916215"
---
# <a name="queued-components-architecture"></a>Arquitectura de componentes en cola

El servicio de componentes en cola de COM+ mejora el modelo de programación COM al proporcionar un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o asincrónicamente (en cola). Un componente no necesita ser consciente de si se emplea en un contexto en tiempo real o en cola.

Las aplicaciones de mensajería son como transacciones de correo electrónico entre programas. El solicitante envía un mensaje al servidor; cuando el servidor llega a él, se procesa el mensaje. Al igual que el correo electrónico, un sistema de mensajería debe controlar los detalles de la red y asegurarse de que el mensaje se mueve del cliente al servidor. En el marco de componentes en cola, Message Queuing es responsable de esto.

El servicio de componentes en cola de COM+ consta de las siguientes partes:

-   Grabadora (para el cliente o el lado de envío)
-   Agente de escucha (para el servidor o el lado de recepción)
-   Player (para el servidor o el lado de recepción)

![Diagrama que muestra la ruta de acceso del cliente al servidor: cliente, grabadora, cola, agente de escucha, reproductor, servidor.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>La grabadora

En un escenario típico de componentes en cola, el cliente llama a un componente en cola. La llamada se realiza a la grabadora de componentes en cola, que la empaqueta como parte de un mensaje al servidor y la coloca en una cola. La grabadora serializa el contexto de seguridad del cliente en el mensaje y registra todas las llamadas al método del cliente. En su rol de proxy para el componente de servidor, la grabadora selecciona interfaces de las interfaces que se pueden usar en el catálogo de COM+.

Una representación de la grabación se envía a Message Queuing como un mensaje que se va a enviar a un servidor. Cuando el componente en cola tiene el valor de atributo de transacción Requerido o Admitido, Message Queuing acepta la entrega del mensaje solo si la transacción del lado cliente se confirma y la cola de Message Queuing es transaccional, que es el valor predeterminado establecido normalmente. Cuando la configuración del atributo de transacción es Requires New, Message Queuing puede aceptar el mensaje incluso si se anula la transacción del lado cliente. Para obtener más información sobre las transacciones, [vea Transactional Message Queuing](transactional-message-queuing.md).

## <a name="the-listener"></a>El agente de escucha

El agente de escucha de componentes en cola recupera el mensaje de la cola y lo pasa al reproductor de componentes en cola.

## <a name="the-player"></a>El reproductor

El reproductor desmarque el contexto de seguridad del cliente en el lado servidor y, a continuación, invoca el componente de servidor y realiza las mismas llamadas de método. El reproductor no reproduce las llamadas al método hasta que se completa el componente de cliente y se confirma la transacción que registró las llamadas al método.

## <a name="the-message-mover"></a>El motor de mensajes

El motor de mensajes de componentes en cola es una utilidad que mueve todos los mensajes de Message Queuing con errores de una cola a otra para que se puedan reinterír. La utilidad de mover mensajes es un objeto de Automation que se puede invocar con un VBScript; Para obtener más información, vea [Controlar errores.](handling-errors-in-queued-components.md)

 

 



