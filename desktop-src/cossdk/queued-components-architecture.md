---
description: El servicio de componentes en cola de COM+ mejora el modelo de programación COM proporcionando un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o de forma asincrónica (en cola).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Arquitectura de componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104567621"
---
# <a name="queued-components-architecture"></a>Arquitectura de componentes en cola

El servicio de componentes en cola de COM+ mejora el modelo de programación COM proporcionando un entorno en el que se puede invocar un componente de forma sincrónica (en tiempo real) o de forma asincrónica (en cola). Un componente no necesita tener en cuenta si se emplea en un contexto en tiempo real o en cola.

Las aplicaciones de mensajería son similares a las transacciones por correo electrónico entre programas. El solicitante envía un mensaje al servidor; Cuando el servidor lo recibe, se procesa el mensaje. Como el correo electrónico, un sistema de mensajería debe administrar los detalles de la red y asegurarse de que el mensaje se mueve desde el cliente al servidor. En el marco de trabajo de componentes en cola, Message Queue Server es responsable de ello.

El servicio de componentes en cola de COM+ consta de las siguientes partes:

-   Grabadora (para el cliente o el lado de envío)
-   Agente de escucha (para el servidor o el lado de recepción)
-   Reproductor (para el servidor o el lado de recepción)

![Diagrama que muestra la ruta de acceso desde el cliente al servidor: cliente, grabadora, cola, agente de escucha, reproductor, servidor.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>La grabadora

En un escenario típico de componentes en cola, el cliente llama a un componente en cola. La llamada se realiza a la grabadora de componentes en cola, que la empaqueta como parte de un mensaje en el servidor y lo coloca en una cola. La grabadora calcula las referencias del contexto de seguridad del cliente en el mensaje y registra todas las llamadas al método del cliente. En su rol como proxy para el componente del servidor, la grabadora selecciona interfaces de las interfaces de queuable en el catálogo de COM+.

Una representación de la grabación se envía a Message Queue Server como un mensaje que se va a enviar a un servidor. Cuando el componente en cola tiene el valor de atributo de transacción requerido o compatible, Message Queue Server acepta la entrega del mensaje solo si la transacción del cliente se confirma y la cola de Message Queue Server es transaccional, que es el valor predeterminado que se establece normalmente. Cuando la configuración del atributo de transacción requiere nuevo, Message Queue Server puede aceptar el mensaje incluso si se anula la transacción del cliente. Para obtener más información sobre las transacciones, vea [Message Queue Server transaccional](transactional-message-queuing.md).

## <a name="the-listener"></a>El agente de escucha

El agente de escucha de componentes en cola recupera el mensaje de la cola y lo pasa al reproductor de componentes en cola.

## <a name="the-player"></a>El reproductor

El reproductor Anula la serialización del contexto de seguridad del cliente en el lado del servidor y, a continuación, invoca el componente del servidor y realiza las mismas llamadas al método. El reproductor no reproduce las llamadas al método hasta que el componente de cliente finaliza y la transacción que registra el método llama a las confirmaciones.

## <a name="the-message-mover"></a>El Movedor de mensajes

El Movedor de mensajes de componentes en cola es una utilidad que mueve todos los mensajes de Message Queue Server con errores de una cola a otra para que se puedan Reintentar. La utilidad del Movedor de mensajes es un objeto de automatización que se puede invocar con un VBScript; para obtener más información, vea [control de errores](handling-errors-in-queued-components.md).

 

 



