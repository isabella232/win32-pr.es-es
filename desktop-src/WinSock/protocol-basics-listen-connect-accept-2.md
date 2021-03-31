---
description: Conceptos básicos de los protocolos WSPListen, WSPAccept y WSPConnect para establecer una conexión de socket con Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Conceptos básicos del Protocolo: escuchar, conectar, aceptar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62ef290d71e571154b4d022c24c7e21f8fffa1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154254"
---
# <a name="protocol-basics-listen-connect-accept"></a>Conceptos básicos del Protocolo: escuchar, conectar, aceptar

Las operaciones básicas implicadas en el establecimiento de una conexión de socket se pueden explicar más fácilmente en términos del paradigma cliente-servidor.

En primer lugar, el lado servidor creará un socket, lo enlazará a una dirección local conocida (para que el cliente pueda encontrarlo) y colocará el socket en modo de escucha, a través de [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), para preparar las solicitudes de conexión entrantes y especificar la longitud de la cola de trabajo pendiente de conexión. Los proveedores de servicios mantienen solicitudes de conexión pendientes en una cola de trabajos pendientes hasta que el servidor las actúa o cuando se retiran (debido a un tiempo de espera) el cliente. Un proveedor de servicios puede pasar por alto silenciosamente las solicitudes para ampliar el tamaño de la cola de trabajos pendientes más allá de un límite superior definido por el proveedor.

En este punto, si se usa un socket de bloqueo, el lado del servidor puede llamar inmediatamente a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) , que se bloqueará hasta que haya una solicitud de conexión pendiente. Por el contrario, el servidor también puede usar uno de los mecanismos de indicación de eventos de red descritos anteriormente para organizar la notificación de solicitudes de conexión entrantes. Dependiendo del mecanismo de notificación seleccionado, el proveedor emitirá un mensaje de Windows o señalizará un objeto de evento cuando lleguen las solicitudes de conexión. Consulte [notificación de eventos de red](notification-of-network-events-2.md) sobre cómo registrarse para el evento de aceptación de red de FD \_ .

El lado cliente creará un socket adecuado e iniciará la conexión mediante una llamada a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), especificando la dirección del servidor conocido. Normalmente, los clientes no realizan una operación de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) explícita antes de iniciar una conexión, lo que permite al proveedor de servicios realizar un enlace implícito en su nombre. Si el socket está en modo de bloqueo, **WSPConnect** se bloqueará hasta que el servidor haya recibido y actuado en la solicitud de conexión (o hasta que se agote el tiempo de espera). De lo contrario, el cliente debe usar uno de los mecanismos de indicación de eventos de red descritos anteriormente para solicitar la notificación de que se ha establecido una nueva conexión. Dependiendo del mecanismo de notificación seleccionado, el proveedor lo indicará a través de un mensaje de Windows o mediante la señalización de un objeto de evento.

Cuando el lado del servidor invoca [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept), el proveedor de servicios llama a la función de condición proporcionada por la aplicación, usando los parámetros de función para pasar a la información del servidor de la entrada superior en la cola de trabajo pendiente de solicitud de conexión. Esta información incluye aspectos como la dirección del host de conexión, los datos de usuario disponibles y cualquier información de QoS disponible. Con esta información, la función de condición del servidor determina si se debe aceptar la solicitud, rechazar la solicitud o aplazar la toma de decisiones hasta más tarde. Esta decisión se indica mediante el valor devuelto de la función condition. Consulte [notificación de eventos de red](notification-of-network-events-2.md) sobre cómo registrarse para el \_ evento de red FD Connect.

Si el servidor decide aceptar la solicitud, el proveedor debe crear un nuevo socket con todos los mismos atributos y registros de eventos que el socket de escucha. El socket original permanece en el estado de escucha para que se puedan recibir las solicitudes de conexión posteriores. A través de los parámetros de salida de la función condition, el servidor también puede proporcionar los datos de usuario de respuesta y asignar parámetros de QoS (suponiendo que estas operaciones sean compatibles con el proveedor de servicios).

 

 
