---
description: En los siguientes casos, un socket Multipoint se describe con frecuencia definiendo su función en uno de los dos planos (control o datos).
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: Semántica para combinar hojas de Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706182"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>Semántica para combinar hojas de Multipoint

En los siguientes casos, un socket Multipoint se describe con frecuencia definiendo su función en uno de los dos planos (control o datos). Debe entenderse que el mismo socket tiene un rol en el otro plano, pero esto no se menciona a fin de mantener las referencias cortas. Por ejemplo, cuando se realiza una referencia a un " \_ socket raíz de c", puede ser una \_ raíz raíz/d de c \_ o un \_ socket de hoja raíz/d de c \_ .

En los esquemas de plano de control con raíz, los nuevos nodos hoja se agregan a una sesión de Multipoint en uno o ambos dos modos diferentes. En el primer método, la raíz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para iniciar una conexión con un nodo hoja y para invitarlo a participar en él. En el nodo hoja, la aplicación del mismo nivel debe haber creado un \_ socket hoja de c y haber usado [**escuchar**](/windows/desktop/api/Winsock2/nf-winsock2-listen) para establecerlo en modo de escucha. El nodo hoja recibe una \_ indicación de aceptación FD cuando se le invita a unirse a la sesión y señala su voluntad de unirse llamando a [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). A continuación, la aplicación raíz recibe una \_ indicación FD Connect cuando se ha completado la operación de **Unión** .

En el segundo método, los roles se invierten esencialmente. La aplicación raíz crea un \_ socket raíz de c y lo establece en modo de escucha. Un nodo hoja que quiere unirse a la sesión crea un \_ socket hoja de c y usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para iniciar la conexión y solicitar admisión. La aplicación raíz recibe el \_ método FD Accept cuando llega una solicitud admisión entrante y admite el nodo hoja llamando a [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). El nodo hoja recibe FD \_ Connect cuando se ha admitido.

En un plano de control no raíz, donde todos los nodos son \_ hojas de c, se usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para iniciar la inclusión de un nodo en una sesión de Multipoint existente. \_Se proporciona una indicación FD Connect cuando se ha completado la combinación y se puede usar el descriptor de socket devuelto en la sesión multipoint. En el caso de la multidifusión IP, esto correspondería a la opción de IP \_ agregar \_ socket de pertenencia.

(Los lectores familiarizados con el uso de la multidifusión IP del protocolo UDP sin conexión pueden estar relacionados con la semántica orientada a la conexión que se presenta aquí. En concreto, la noción de usar [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) en un socket UDP y esperar una \_ indicación de conexión FD puede ser preocupantes. No obstante, hay un gran precedente para aplicar la semántica orientada a la conexión a los protocolos sin conexión. Se permite y a veces útil, por ejemplo, para invocar la función de [**conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect) estándar en un socket UDP. El resultado general de la aplicación de la semántica orientada a la conexión a los sockets sin conexión es una restricción en la forma en que se pueden usar dichos sockets, y este es el caso aquí también. Un socket UDP usado en **WSAJoinLeaf** tendrá ciertas restricciones y esperará una \_ indicación FD Connect (que en este caso indica simplemente que se ha enviado el mensaje IGMP correspondiente) es una de estas limitaciones).

Por lo tanto, hay tres instancias en las que una aplicación usaría [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) actuando como:

-   Multipoint raíz e invitar a una nueva hoja para unirse a la sesión
-   Hoja que realiza una solicitud de admisión a una sesión de multipoint con raíz
-   Hoja que busca admisión en una sesión de Multipoint no raíz (por ejemplo, multidifusión IP)

 

 



