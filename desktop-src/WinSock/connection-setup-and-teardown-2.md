---
description: La función WSAAccept permite a una aplicación obtener información del llamador, como el identificador del autor de la llamada y la calidad del servicio, antes de decidir si se acepta una solicitud de conexión entrante.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configuración y desmontaje de la conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474524"
---
# <a name="connection-setup-and-teardown"></a>Configuración y desmontaje de la conexión

La [**función WSAAccept permite**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) a una aplicación obtener información del llamador, como el identificador del autor de la llamada y la calidad del servicio, antes de decidir si se acepta una solicitud de conexión entrante. Esto se hace con una devolución de llamada a una función de condición proporcionada por la aplicación.

Los datos de usuario a usuario especificados por los parámetros de la función [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) y la función de condición de [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) se pueden transferir al mismo nivel durante el establecimiento de la conexión, siempre que esta característica sea compatible con el proveedor de servicios.

También es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los puntos de conexión en el momento de la desmontaje de la conexión. El final que inicia la desmontaje puede llamar a la función [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para indicar que no se envían más datos e iniciar la secuencia de desmontaje de la conexión. Para determinados protocolos, parte de la desmontaje es la entrega de datos de desconexión del iniciador de la desmontaje. Después de recibir el aviso de que el extremo remoto ha iniciado la desmontaje (normalmente por la indicación FD CLOSE), se puede llamar a la función \_ [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para recibir los datos de desconexión, si los hay.

Para ilustrar cómo se pueden usar los datos de desconexión, considere el siguiente escenario. La mitad del cliente de una aplicación cliente/servidor es responsable de finalizar una conexión de socket. Coincidente con la terminación, proporciona (mediante datos de desconexión) el número total de transacciones que procesó con el servidor. A su vez, el servidor responde con el total acumulado de transacciones que ha procesado con todos los clientes. La secuencia de llamadas e indicaciones puede producirse de la siguiente manera:

| En el cliente                                                                                                              | En el servidor                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) [**Invoque WSASendDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) concluir la sesión y proporcionar el total de transacciones.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) Obtener FD CLOSE, recv con un valor devuelto de \_ cero o [WSAEDISCON](windows-sockets-error-codes-2.md) devuelve un error de [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) que indica un cierre correcto en curso. [](/windows/desktop/api/winsock/nf-winsock-recv) |
|                                                                                                                          | (3) [**Invoque WSARecvDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) obtener el total de transacciones del cliente.                                                                                                                                |
|                                                                                                                          | (4) Total acumulado acumulado de todas las transacciones.                                                                                                                                                                       |
|                                                                                                                          | (5) [**Invoque WSASendDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) transmitir el total general.                                                                                                                                          |
| (6) Recibir indicación FD \_ CLOSE.                                                                                        | (5a) Invoke [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) [**Invoque WSARecvDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) recibir y almacenar el total acumulado de transacciones. |                                                                                                                                                                                                                               |
| (8) Invocación [ **de closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Tenga en cuenta que el paso (5a) debe seguir el paso (5), pero no tiene ninguna relación de tiempo con los pasos (6), (7) o (8).

 

 



