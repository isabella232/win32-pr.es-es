---
description: El material siguiente se proporciona como aclaración para el cierre de las conexiones de socket que cierran los sockets. Es importante distinguir la diferencia entre apagar una conexión de socket y cerrar un socket.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Cierre estable, opciones de permanencia y cierre de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275402"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Cierre estable, opciones de permanencia y cierre de socket

El material siguiente se proporciona como aclaración para el cierre de las conexiones de socket que cierran los sockets. Es importante distinguir la diferencia entre apagar una conexión de socket y cerrar un socket.

Cerrar una conexión de socket implica un intercambio de mensajes de protocolo entre los dos extremos, lo que se conoce ahora como una secuencia de cierre. Se definen dos clases generales de secuencias de cierre: correcto y anulación (también denominada Hard). En una secuencia de cierre correcto, se pueden enviar todos los datos que se han puesto en cola, pero que aún no se han transmitido, antes de que se cierre la conexión. En un cierre anulado, se pierden los datos no enviados. La aparición de una secuencia de apagado (correcta o anulación) también se puede usar para proporcionar una \_ indicación de cierre FD a las aplicaciones asociadas, lo que significa que hay un apagado en curso.

Al cerrar un socket, por otro lado, el controlador de socket se desasigna para que la aplicación ya no pueda hacer referencia o usar el socket de ninguna manera.

En Windows Sockets, la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) y la función [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) se pueden usar para iniciar una secuencia de apagado, mientras que la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) se usa para desasignar identificadores de socket y liberar los recursos asociados. No obstante, se produce cierta cantidad de confusión, desde el hecho de que la función **closesocket** produce implícitamente una secuencia de cierre si aún no se ha producido. De hecho, se ha convertido en una práctica de programación bastante común que se basa en esta característica y que usa **closesocket** para iniciar la secuencia de apagado y desasignar el identificador de socket.

Para facilitar este uso, la interfaz de sockets proporciona controles por medio del mecanismo de la opción de socket que permite al programador indicar si la secuencia de apagado implícita debe ser correcta o anulada, y también si la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) debe ser persistente (que no se completa inmediatamente) para dejar tiempo para que se complete una secuencia de cierre correcto. Estas distinciones importantes y las consecuencias del uso de **closesocket** de esta manera todavía no se entienden ampliamente.

Mediante el establecimiento de los valores adecuados para las opciones de socket, por lo tanto \_ \_ , DONTLINGER, se pueden obtener los siguientes tipos de comportamiento con la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) :

-   Secuencia de apagado anulada, devolución inmediata desde [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Cierre estable, retraso en la devolución hasta que se complete la secuencia de cierre o transcurra un intervalo de tiempo especificado. Si el intervalo de tiempo expira antes de que se complete la secuencia de cierre correcto, se produce una secuencia de apagado anulado y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) devuelve.
-   Cierre estable, devolución inmediata, que permite que la secuencia de apagado se complete en segundo plano. Aunque este es el comportamiento predeterminado, la aplicación no tiene ninguna manera de saber cuándo se completa realmente la secuencia de cierre correcto.

El uso de las \_ Opciones de socket SO y so \_ DONTLINGER y la estructura de [**permanencia**](/windows/desktop/api/winsock/ns-winsock-linger) asociada se describe con más detalle en las secciones de referencia de [**\_ las opciones de socket de sockets sol**](sol-socket-socket-options.md) y la estructura de **permanencia** .

Una técnica que se puede usar para minimizar la posibilidad de que se produzcan problemas durante la destrucción de la conexión es evitar que se confíe en un apagado implícito Iniciado por [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). En su lugar, utilice una de las dos funciones de cierre explícita, [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Esto, a su vez, hace que \_ la aplicación del mismo nivel reciba una indicación de cierre FD que indica que se han recibido todos los datos pendientes. Para ilustrar esto, en la tabla siguiente se muestran las funciones que invocarían los componentes de cliente y servidor de una aplicación, donde el cliente es responsable de iniciar un cierre estable.

| En el cliente                                                                                                                | En el servidor                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) invoca [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ send) para señalar el final de la sesión y ese cliente no tiene más datos para enviar. |                                                                                                       |
|                                                                                                                            | (2) recibe FD \_ Close, lo que indica un cierre correcto en curso y que se han recibido todos los datos. |
|                                                                                                                            | (3) envía los datos de respuesta restantes.                                                                |
| (solo significado de sincronización local) Obtiene FD \_ Read y llama a [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) para obtener los datos de respuesta enviados por el servidor.  | (4) invoca [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ send) para indicar que el servidor no tiene más datos para enviar.  |
| (5) recibe la \_ indicación FD de cierre.                                                                                         | (solo significado de sincronización local) Invoca [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .                       |
| (6) invoca [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                          |                                                                                                       |



 

 

 



