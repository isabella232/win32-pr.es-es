---
description: Detalles de seguimiento de eventos de red Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Detalles de seguimiento de eventos de red Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278091"
---
# <a name="winsock-network-event-tracing-details"></a>Detalles de seguimiento de eventos de red Winsock

A continuación se detalla cada uno de los eventos de red Winsock de los que se puede realizar un seguimiento y se describen los parámetros y la información que se registran.

## <a name="socket-creation"></a>Creación de sockets

ID. de evento = 1

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para la creación de Sockets:

-   Identificadores de socket creados por llamadas a las funciones [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Identificadores de socket aceptados en sockets de escucha.
-   Identificadores de socket creados mediante llamadas a la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Los identificadores de socket reutilizados por las llamadas a las funciones [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) o [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .

Los parámetros siguientes se registran para un evento de creación de Sockets:



| Parámetro                                                                                                        | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                 | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>             | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | Tipo del socket.<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>N°<br/>             | Protocolo del socket.<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid<br/> | IDENTIFICADOR de proceso del modo de usuario que creó el socket.<br/>                           |



 

## <a name="socket-bind"></a>Enlace de socket

ID. de evento = 2 (IPv4), ID. de evento = 3 (IPv6)

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una operación de enlace:

-   Enlace implícito o explícito de un identificador de socket.

Los parámetros siguientes se registran para un evento de enlace:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>     | Dirección IP local.<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                 | El número de puerto IP local.<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estatus<br/>         | El código de estado o de error devuelto para la operación de enlace.<br/>                   |



 

## <a name="failed-bind"></a>Error de enlace

ID. de evento = 40

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una operación de enlace con error:

-   Enlace implícito o explícito de un identificador de socket que produce un error.

Los parámetros siguientes se registran para un evento de enlace con errores:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación de enlace con error.<br/>                     |



 

## <a name="socket-connect"></a>Conexión de socket

ID. de evento = 4 (IPv4), ID. de evento = 5 (IPv6)

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una solicitud de operación de conexión (una llamada a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):

-   Conexión de un socket a un destino para un socket orientado a la conexión o sin conexión.

Los parámetros siguientes se registran para un evento de conexión:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>     | Dirección IP remota.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                 | El número de puerto IP remoto.<br/>                                                  |



 

## <a name="connect-completed"></a>Conexión completada

ID. de evento = 6

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una conexión completada:

-   Se completó la operación de conexión.

Los parámetros siguientes se registran para un evento de conexión completada:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación de conexión.<br/>                          |



 

## <a name="afd-initiated-abort"></a>AFD-Initiated anular

ID. de evento = 7

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para las anulaciones iniciadas por Winsock o las operaciones de cancelación:

-   Anulación debido a la recepción de datos no leídos almacenados en búfer después de cerrar.
-   Una anulación después de una llamada a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con el parámetro *how* establecido en SD \_ Receive y una llamada a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) con los datos de recepción pendientes.
-   Una anulación después de un error al intentar vaciar el extremo.
-   Una anulación después de un error interno de Winsock.
-   Una anulación debido a una conexión con errores y la aplicación solicitó previamente que la conexión se anulara en determinadas circunstancias. Un ejemplo de este caso sería una aplicación que se establece de modo que sea \_ persistente con un tiempo de espera de cero y que todavía haya datos no confirmados en la conexión.
-   Anulación de una conexión que no está totalmente asociada con el punto de conexión de aceptación.
-   Una anulación en una llamada errónea a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) o [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .
-   Anulación debido a una operación de recepción con errores.
-   Anulación debido a un evento de Plug and Play.
-   Una anulación debido a una solicitud de vaciado con errores.
-   Una anulación debido a una solicitud de recepción de datos rápida con errores.
-   Una anulación debido a un error en una solicitud de envío.
-   Anulación debido a una solicitud de envío cancelada.
-   Anulación debido a que se ha cancelado la llamada a la función [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .

Los parámetros siguientes se registran para una operación de anulación o cancelación iniciada por Winsock:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido<br/>         | Motivo de la operación de anulación o cancelación.<br/>                               |



 

## <a name="transport-initiated-abort"></a>Transport-Initiated anular

ID. de evento = 8

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de anulación o cancelación iniciadas por el transporte:

-   Restablecimiento indicado por el transporte.

Los parámetros siguientes se registran para una operación de anulación o cancelación iniciada por Winsock:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido<br/>         | Motivo de la operación de anulación o cancelación.<br/>                               |



 

## <a name="failed-send-request"></a>Error de solicitud de envío

ID. de evento = 9

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock en busca de errores en las solicitudes [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :

-   Errores devueltos en solicitudes de [**envío**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) con error.

Los parámetros siguientes se registran para las solicitudes de envío que producen un error:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación.<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>Error de solicitud WsaSendMsg

ID. de evento = 10

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de Winsock en busca de errores en las solicitudes de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :

-   Errores devueltos en solicitudes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) erróneas.

Los parámetros siguientes se registran para las solicitudes de envío que producen un error:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación.<br/>                                  |



 

## <a name="failed-recv-request"></a>Solicitud de recepción errónea

ID. de evento = 11

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock en busca de errores en las solicitudes [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)o [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :

-   Errores devueltos en solicitudes de recepción con error.

Los parámetros siguientes se registran para las solicitudes de envío que producen un error:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación.<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>Error de solicitud recvfrom

ID. de evento = 12

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de Winsock en busca de errores en las solicitudes de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :

-   Errores devueltos en solicitudes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) con error.

Los parámetros siguientes se registran para una solicitud [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) que produce un error:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación.<br/>                                  |



 

## <a name="socket-close"></a>Cerrar socket

ID. de evento = 13

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de cierre de socket:

-   Un identificador de socket está cerrado.

Los parámetros siguientes se registran para un evento de cierre de socket:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | El valor devuelto para la operación de cierre del socket.<br/>                            |



 

## <a name="socket-cleanup"></a>Limpieza de sockets

ID. de evento = 14

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de limpieza de sockets (apagado):

-   Se llama a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) en un socket.
-   El transporte indica que se ha producido un error en la desconexión correcta.

Los parámetros siguientes se registran para un evento de limpieza de socket (shutdown) o de cierre de socket:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | El valor devuelto para la operación de limpieza de socket (shutdown).<br/>               |



 

## <a name="socket-accept"></a>Aceptación de socket

ID. de evento = 15 (IPv4), ID. de evento = 16 (IPv6)

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una solicitud de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :

-   Una solicitud de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) en un identificador de socket.

Los parámetros siguientes se registran para un evento Accept:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>     | Dirección IP remota.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                 | El número de puerto IP remoto.<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estatus<br/>         | El código de estado o de error devuelto para la operación de aceptación.<br/>                 |



 

## <a name="accept-failed"></a>Error de aceptación

ID. de evento = 17

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos Winsock para una operación de aceptación errónea:

-   Una solicitud [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) en un identificador de socket que produce un error.

Los parámetros siguientes se registran para un evento de aceptación con errores:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación de aceptación con error.<br/>                   |



 

## <a name="send-posted"></a>Envío enviado

ID. de evento = 18

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones post de búfer de envío y recepción de socket:

-   Una aplicación envía un envío.
-   Una operación de envío se completa en Winsock.

Los parámetros siguientes se registran para las operaciones de envío de socket:



| Parámetro                                                                                                            | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer. En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.<br/>  |



 

Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer. Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.

## <a name="receive-posted"></a>Recepción enviada

ID. de evento = 19

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones post de búfer de recepción de socket:

-   Una aplicación envía una recepción.
-   Una operación de recepción se completa en Winsock.

Los parámetros siguientes se registran para las operaciones de recepción de Sockets:



| Parámetro                                                                                                            | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer. En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.<br/>  |



 

Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer. Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.

## <a name="recvfrom-posted"></a>RecvFrom enviado

ID. de evento = 20

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock para una operación post de búfer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) en un socket:

-   Una aplicación envía una operación Receive from.

Los parámetros siguientes se registran para la operación recvfrom:



| Parámetro                                                                                                            | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer. En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.<br/>  |



 

Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer. Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.

## <a name="sendto-posted"></a>Enviar a enviado

ID. de evento = 21 (IPv4), ID. de evento = 22 (IPv6)

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos de Winsock para una operación de post de búfer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) en un socket:

-   Una aplicación envía un envío desde.

Los parámetros siguientes se registran para la operación [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Parámetro                                                                                                            | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valor booleano que indica si se usó la e/s de la ruta de acceso rápida.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer. En el caso de los búferes encadenados, este parámetro es el número total de bytes en todos los búferes de la cadena.<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>                     | Dirección IP remota del socket.<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                                 | Número de puerto IP remoto del socket.<br/>                                                                                        |



 

Cuando FastPath es true, la dirección de modo de usuario del primer búfer de la matriz de búferes se registra en el parámetro buffer. Cuando FastPath es false, la dirección del búfer del kernel de Winsock se registra en el parámetro buffer.

## <a name="recv-completed"></a>Recepción completada

ID. de evento = 23

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de recepción de sockets completadas:

-   Una operación de envío se completa en el transporte.
-   Una operación de recepción se completa en el transporte.

Los parámetros siguientes se registran para un envío completado o recibido:



| Parámetro                                                                                                            | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer de bytes recibido. En el caso de los búferes encadenados, este parámetro es el total de bytes recibidos en todos los búferes de la cadena.<br/> |



 

## <a name="send-completed"></a>Envío completado

ID. de evento = 24

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de envío de sockets completadas:

-   Una operación de envío se completa en el transporte.

Los parámetros siguientes se registran para un envío completado:



| Parámetro                                                                                                            | Descripción                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer de bytes enviados. En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.<br/> |



 

## <a name="sendmsg-completed"></a>SendMsg completado

ID. de evento = 25

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación post de búfer de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) en un socket:

-   Una aplicación completa una operación [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Los parámetros siguientes se registran para la finalización de [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :



| Parámetro                                                                                                            | Descripción                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer de bytes enviados. En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>                     | Dirección IP remota del socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                                 | Número de puerto IP remoto del socket.<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>RecvFrom completado

ID. de evento = 26 (IPv4), ID. de evento = 27 (IPv6)

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación post de búfer de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) en un socket:

-   Una aplicación completa una operación [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .

Los parámetros siguientes se registran para la finalización de [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :



| Parámetro                                                                                                            | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer de bytes recibido. En el caso de los búferes encadenados, este parámetro es el total de bytes recibidos en todos los búferes de la cadena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>                     | Dirección IP remota del socket.<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                                 | Número de puerto IP remoto del socket.<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>Enviar a completado

ID. de evento = 28

Nivel = 5 (detallado)

Con el fin de diagnosticar daños en el búfer del usuario (por ejemplo, cuando una aplicación vuelve a usar el mismo búfer en otra llamada de envío o recepción mientras todavía está en uso), el búfer de datos se registra cuando se envía a Winsock y al finalizar el transporte subyacente. Se realiza un seguimiento de los siguientes eventos Winsock cuando se completa una operación de envío de búfer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) en un socket:

-   Una aplicación completa una operación [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .

Los parámetros siguientes se registran para la finalización de [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Parámetro                                                                                                            | Descripción                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                 | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Recuento de búferes.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Búfer<br/>                         | Dirección virtual del búfer. En el caso de los búferes encadenados, este parámetro es la dirección virtual del primer búfer de la cadena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longitud del búfer de bytes enviados. En el caso de los búferes encadenados, este parámetro es el total de bytes enviados desde todos los búferes de la cadena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>                     | Dirección IP remota del socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                                 | Número de puerto IP remoto del socket.<br/>                                                                                           |



 

## <a name="socket-option-set"></a>Conjunto de opciones de socket

ID. de evento = 29

Nivel = 5 (detallado)

Cada vez que una aplicación cambie determinados valores de opción de socket y ioctl, se registrarán los nuevos valores. Las opciones registradas se pueden usar para diagnosticar un rendimiento deficiente o un comportamiento extraño en las aplicaciones. Se realiza un seguimiento de los siguientes eventos Winsock para determinadas opciones de socket y ioctl:

-   Por lo tanto, \_ SNDBUF cambia.
-   Por lo tanto, \_ RCVBUF cambia.
-   FIONBIO
-   SIO \_ habilitar \_ la \_ puesta en cola circular
-   SIO \_ UDP \_ CONNRESET
-   \_OOBINLINE

Los parámetros siguientes se registran [**para las llamadas a la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y que cambian cualquiera de los valores anteriores:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>Desea<br/>         | Opción de socket o IOCTL que se ha modificado. <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor<br/>             | Nuevo valor de la opción de socket o ioctl. <br/>                              |



 

## <a name="selectpoll-posted"></a>Seleccionar/sondeo publicado

ID. de evento = 30

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   La aplicación envía una solicitud [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Los parámetros siguientes se registran para los eventos [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :



| Parámetro                                                                                                        | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                 | IDENTIFICADOR del proceso propietario.<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | Número de identificadores pasados por la aplicación (solo válido en el evento de inicio).<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Super<br/>                 | Tiempo máximo de espera de la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="selectpoll-completed"></a>Selección/sondeo completado

ID. de evento = 31

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   Winsock completa una llamada [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Los parámetros siguientes se registran cuando se completa una operación [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :



| Parámetro                                                                                            | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error<br/>             | Código de error devuelto para la operación [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

ID. de evento = 32

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock cuando una aplicación llama a la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :

-   Registra la máscara de eventos pasada en la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

Los parámetros siguientes se registran para las llamadas de función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :



| Parámetro                                                                                                | Descripción                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>         | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>     | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | El valor de la máscara de eventos. <br/>                                              |



 

## <a name="dropped-datagram"></a>Datagrama quitado

ID. de evento = 33 (IPv4), ID. de evento = 34 (IPv6)

Nivel = 5 (detallado)

Para ayudar a diagnosticar problemas relacionados con las aplicaciones de datagramas, se realiza un seguimiento de los siguientes eventos de Winsock:

-   Cuando llega un datagrama y se quita en el espacio de búfer insuficiente.
-   En un datagrama conectado, si los datos llegan de un origen que no es el destino conectado.

Los parámetros siguientes se registran para los datagramas que se han quitado:



| Parámetro                                                                                                    | Descripción                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>             | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>         | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize<br/> | Tamaño del paquete que se ha quitado. <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>             | Dirección IP del origen del paquete. <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                         | Número de puerto IP del origen del paquete.<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Debido<br/>                 | El código de error o la razón por la que se quitó el paquete.<br/>                            |



 

## <a name="connection-indicated"></a>Conexión indicada

ID. de evento = 35 (IPv4), ID. de evento = 36 (IPv6)

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones indicadas para la conexión:

-   Una aplicación recibe una solicitud de conexión.

Los parámetros siguientes se registran para las conexiones indicadas desde los eventos de transporte:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>     | Dirección IP remota. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                 | El número de puerto IP remoto.<br/>                                                  |



 

## <a name="data-indicated"></a>Datos indicados

ID. de evento = 37

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones indicadas:

-   Una aplicación recibe datos en un socket conectado.

Los parámetros siguientes se registran para los datos indicados en los eventos de transporte:



| Parámetro                                                                                                                        | Descripción                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                                 | IDENTIFICADOR del proceso propietario.<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                             | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados<br/> | Número de bytes recibidos en el socket.<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>Datos indicados desde el transporte

ID. de evento = 38 (IPv4), ID. de evento = 39 (IPv6)

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock para los datos indicados en las operaciones de transporte:

-   Una aplicación envía una solicitud de recepción y recibe datos.

Los parámetros siguientes se registran para los datos indicados en los eventos de transporte:



| Parámetro                                                                                                                        | Descripción                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>                                 | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/>                             | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Dirección<br/>                                 | Dirección IP remota. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Casilla<br/>                                             | El número de puerto IP remoto.<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados<br/> | Número de bytes recibidos en el socket.<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>Desconexión indicada del transporte

ID. de evento = 41

Nivel = 5 (detallado)

Se realiza un seguimiento de los siguientes eventos Winsock para las operaciones de desconexión indicadas:

-   Una aplicación recibe una indicación de desconexión.

Los parámetros siguientes se registran para la desconexión indicada en los eventos de transporte:



| Parámetro                                                                                            | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Procese<br/>     | Dirección de la estructura del EPROCESS de kernel para el proceso.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Finales<br/> | Dirección del socket del kernel Winsock utilizada como identificador único de un socket.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
