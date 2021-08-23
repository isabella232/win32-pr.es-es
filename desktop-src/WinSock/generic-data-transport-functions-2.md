---
description: Funciones de transporte de datos expuestas por Ws2spi.h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funciones genéricas de transporte de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d13b067713fe6a2600d6667ebe7eac058c5fcae87fc5bfd14311b3a263b862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132358"
---
# <a name="generic-data-transport-functions"></a>Funciones genéricas de transporte de datos

En esta sección se enumeran las funciones de transporte de datos expuestas por Ws2spi.h.



| Función                                                   | Descripción                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Se confirma una conexión entrante y se asocia a un socket creado inmediatamente. El socket original se devuelve al estado de escucha. Esta función también permite la aceptación condicional. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Realiza la versión asincrónica de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Asigna un nombre local a un socket sin nombre.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Cancela un bloqueo pendiente de Windows sockets.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Cierra la sesión del proveedor de Windows sockets subyacente.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Quita un socket de la tabla de referencia de objetos por proceso. Solo se bloquea si SO LINGER se establece con un tiempo de espera distinto de \_ cero en un socket de bloqueo.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Inicia una conexión en el socket especificado. Esta función también permite el intercambio de datos de conexión y la especificación de QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Devuelve una [**estructura INFO \_ de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que se puede usar para crear un nuevo descriptor de socket para un socket compartido.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Detecta repeticiones de eventos de red.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Asocia eventos de red a un objeto de evento.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Obtiene el estado de finalización de la operación superpuesta.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera el nombre del elemento del mismo nivel conectado al socket especificado.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera la dirección local a la que está enlazado el socket especificado.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera las opciones asociadas al socket especificado.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Proporciona parámetros de QoS basados en un nombre de servicio conocido.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Proporciona control para sockets.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Une un nodo hoja a una sesión multipunto.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Escucha las conexiones entrantes en un socket especificado.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Recibe datos de un socket conectado o no conectado. Esta función admite E/S de dispersión/recopilación, sockets superpuestos y proporciona el parámetro flags como IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Finaliza la recepción en un socket y recupera los datos de desconexión si el socket está orientado a la conexión.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Recibe datos de un socket conectado o no conectado. Esta función admite E/S de dispersión/recopilación, sockets superpuestos y proporciona el parámetro flags como IN/OUT.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Realiza la multiplexación de E/S sincrónica.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Envía datos a un socket conectado. Esta función también admite E/S de dispersión/recopilación y sockets superpuestos.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Inicia la terminación de una conexión de socket y, opcionalmente, envía datos de desconexión.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Envía datos a un socket conectado o no conectado. Esta función también admite E/S de dispersión/recopilación y sockets superpuestos.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Almacena las opciones asociadas al socket especificado.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Cierra parte de una conexión dúplex completa.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Una función de creación de sockets que toma una estructura [**\_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) como entrada y permite crear sockets superpuestos.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inicializa el proveedor de Windows sockets subyacente.                                                                                                                                            |



 

 

 
