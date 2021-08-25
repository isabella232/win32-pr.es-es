---
description: Conceptos básicos del protocolo de WSPListen, WSPAccept y WSPConnect para establecer una conexión de socket con sockets Windows sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Conceptos básicos del protocolo: Escuchar, Conectar, Aceptar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db73ea4bca5a709ff6d030fcbb44661c6181e552955d02b67d8eb2bcf680bf92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857925"
---
# <a name="protocol-basics-listen-connect-accept"></a>Conceptos básicos del protocolo: Escuchar, Conectar, Aceptar

Las operaciones básicas implicadas en el establecimiento de una conexión de socket se pueden explicar más cómodamente en términos del paradigma cliente-servidor.

En primer lugar, el lado servidor creará un socket, lo enlazará a una dirección local conocida (para que el cliente pueda encontrarlo) y colocará el socket en modo de escucha, a través de [**WSPListen,**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))con el fin de prepararse para las solicitudes de conexión entrantes y especificar la longitud de la cola de trabajos pendientes de conexión. Los proveedores de servicios mantienen las solicitudes de conexión pendientes en una cola de trabajos pendientes hasta que el servidor los actúa o el cliente los retira (debido a un tiempo de espera). Un proveedor de servicios puede omitir de forma silenciosa las solicitudes para ampliar el tamaño de la cola de trabajos pendientes más allá de un límite superior definido por el proveedor.

En este momento, si se usa un socket de bloqueo, el lado servidor puede llamar inmediatamente a [**WSPAccept,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) que se bloqueará hasta que haya una solicitud de conexión pendiente. Por el contrario, el servidor también puede usar uno de los mecanismos de indicación de eventos de red que se han analizado anteriormente para organizar la notificación de las solicitudes de conexión entrantes. Dependiendo del mecanismo de notificación seleccionado, el proveedor emitirá un mensaje de Windows o señalará un objeto de evento cuando lleguen las solicitudes de conexión. Consulte [Notificación de eventos de red](notification-of-network-events-2.md) para obtener información sobre cómo registrarse para el evento de red FD \_ ACCEPT.

El lado cliente creará un socket adecuado e iniciará la conexión mediante una llamada a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), especificando la dirección del servidor conocida. Normalmente, los clientes [](/windows/desktop/api/winsock/nf-winsock-bind) no realizan una operación de enlace explícita antes de iniciar una conexión, lo que permite al proveedor de servicios realizar un enlace implícito en su nombre. Si el socket está en modo de bloqueo, **WSPConnect** se bloqueará hasta que el servidor haya recibido y actuado sobre la solicitud de conexión (o hasta que se produzca un tiempo de espera). De lo contrario, el cliente debe usar uno de los mecanismos de indicación de eventos de red que se han analizado anteriormente para organizar la notificación de una nueva conexión que se va a establecer. Según el mecanismo de notificación seleccionado, el proveedor lo indicará a través de un mensaje Windows mensaje o mediante la señalización de un objeto de evento.

Cuando el lado servidor invoca [**WSPAccept,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)el proveedor de servicios llama a la función de condición proporcionada por la aplicación, usando parámetros de función para pasar a la información del servidor desde la entrada superior de la cola de trabajos pendientes de solicitud de conexión. Esta información incluye aspectos como la dirección del host de conexión, los datos de usuario disponibles y cualquier información de QoS disponible. Con esta información, la función de condición del servidor determina si se debe aceptar la solicitud, rechazarla o aplazar la toma de una decisión hasta más adelante. Esta decisión se indica a través del valor devuelto de la función de condición. Consulte [Notificación de eventos de red](notification-of-network-events-2.md) para obtener información sobre cómo registrarse para el evento de red FD \_ CONNECT.

Si el servidor decide aceptar la solicitud, el proveedor debe crear un nuevo socket con todos los mismos atributos y registros de eventos que el socket de escucha. El socket original permanece en estado de escucha para que se puedan recibir solicitudes de conexión posteriores. A través de los parámetros de salida de la función de condición, el servidor también puede proporcionar cualquier dato de usuario de respuesta y asignar parámetros qoS (suponiendo que el proveedor de servicios admite estas operaciones).

 

 
