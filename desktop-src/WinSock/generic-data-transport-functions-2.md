---
description: Las funciones de transporte de datos expuestas por Ws2spi. h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funciones de transporte de datos genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541590"
---
# <a name="generic-data-transport-functions"></a>Funciones de transporte de datos genéricos

En esta sección se enumeran las funciones de transporte de datos expuestas por Ws2spi. h.



| Función                                                   | Descripción                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Una conexión entrante se confirma y se asocia a un socket creado inmediatamente. El socket original se devuelve al estado de escucha. Esta función también permite la aceptación condicional. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Realiza la versión asincrónica de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Asigna un nombre local a un socket sin nombre.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Cancela una llamada pendiente de bloqueo de Windows Sockets.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Cierra la sesión del proveedor de servicios de Windows Sockets subyacentes.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Quita un socket de la tabla de referencia de objetos por proceso. Solo bloquea si SO \_ se establece con un tiempo de espera distinto de cero en un socket de bloqueo.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Inicia una conexión en el socket especificado. Esta función también permite el intercambio de datos de conexión y la especificación QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Devuelve una estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que se puede usar para crear un nuevo descriptor de socket para un socket compartido.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Detecta apariciones de eventos de red.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Asocia eventos de red a un objeto de evento.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Obtiene el estado de finalización de la operación superpuesta.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera el nombre del elemento del mismo nivel conectado al socket especificado.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera la dirección local a la que está enlazado el socket especificado.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera opciones asociadas al socket especificado.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Proporciona parámetros de QoS basados en un nombre de servicio conocido.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Proporciona el control para los sockets.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Une un nodo hoja en una sesión multipoint.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Escucha las conexiones entrantes en un socket especificado.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Recibe datos de un socket conectado o no conectado. Esta función admite la e/s de dispersión/recopilación, los sockets superpuestos y proporciona el parámetro flags como IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Finaliza la recepción en un socket y recupera los datos de desconexión si el socket está orientado a la conexión.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Recibe datos de un socket conectado o no conectado. Esta función admite la e/s de dispersión/recopilación, los sockets superpuestos y proporciona el parámetro flags como IN/OUT.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Realiza multiplexaciones de e/s sincrónicas.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Envía datos a un socket conectado. Esta función también admite la e/s de dispersión y recopilación y los sockets superpuestos.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Inicia la terminación de una conexión de socket y, opcionalmente, envía datos de desconexión.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Envía datos a un socket conectado o no conectado. Esta función también admite la e/s de dispersión y recopilación y los sockets superpuestos.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Almacena las opciones asociadas al socket especificado.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Cierra parte de una conexión dúplex completa.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Una función de creación de sockets que toma una estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) como entrada y permite la creación de sockets superpuestos.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inicializa el proveedor de servicios de Windows Sockets subyacente.                                                                                                                                            |



 

 

 
