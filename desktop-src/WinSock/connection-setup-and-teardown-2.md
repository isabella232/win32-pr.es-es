---
description: La función WSAAccept permite a una aplicación obtener información del llamador como el identificador del autor de la llamada y la calidad del servicio antes de decidir si aceptar una solicitud de conexión entrante.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configuración y desmontaje de la conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696390"
---
# <a name="connection-setup-and-teardown"></a>Configuración y desmontaje de la conexión

La función [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) permite a una aplicación obtener información del llamador como el identificador del autor de la llamada y la calidad del servicio antes de decidir si aceptar una solicitud de conexión entrante. Esto se hace con una devolución de llamada a una función de condición proporcionada por la aplicación.

Los datos de usuario a usuario especificados por los parámetros de la función [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) y la función de condición de [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) se pueden transferir al mismo nivel durante el establecimiento de la conexión, siempre que el proveedor de servicios admita esta característica.

También es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los extremos en el momento de la destrucción de la conexión. El final que inicia el montaje puede llamar a la función [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para indicar que no se van a enviar más datos e iniciar la secuencia de destrucción de la conexión. Para determinados protocolos, parte del montaje es la entrega de datos de desconexión del iniciador de desmontaje. Después de recibir el aviso de que el extremo remoto ha iniciado la desmontaje (normalmente mediante la indicación FD de \_ cierre), se puede llamar a la función [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para recibir los datos de desconexión, si los hay.

Para ilustrar cómo se pueden usar los datos de desconexión, considere el siguiente escenario. La mitad del cliente de una aplicación cliente/servidor es responsable de finalizar una conexión de socket. Coincidentes con la terminación, proporciona (mediante Disconnect Data) el número total de transacciones que ha procesado con el servidor. A su vez, el servidor responde con el total acumulado de transacciones que ha procesado con todos los clientes. La secuencia de llamadas e indicaciones podría producirse de la siguiente manera:

| En el cliente                                                                                                              | En el servidor                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) invoque [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para concluir la sesión y proporcionar el total de la transacción.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) obtener FD \_ Close, [**recibir**](/windows/desktop/api/winsock/nf-winsock-recv) con un valor devuelto de cero o [WSAEDISCON](windows-sockets-error-codes-2.md) error devuelto por [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) que indica un cierre correcto en curso. |
|                                                                                                                          | (3) invocación de [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para obtener el total de la transacción del cliente.                                                                                                                                |
|                                                                                                                          | (4) calcular el total general acumulado de todas las transacciones.                                                                                                                                                                       |
|                                                                                                                          | (5) invoque [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para transmitir el total general.                                                                                                                                          |
| (6) recibir la \_ indicación de cierre FD.                                                                                        | (5A) invocación de [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) invoque [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para recibir y almacenar el total general de transacciones acumulativas. |                                                                                                                                                                                                                               |
| (8) invocación de [ **closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Tenga en cuenta que el paso (5A) debe seguir el paso (5), pero no tiene relación de tiempo con el paso (6), (7) o (8).

 

 



