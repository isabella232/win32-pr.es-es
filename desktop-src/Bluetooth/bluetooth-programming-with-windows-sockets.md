---
title: Bluetooth Programación con Windows sockets
description: En esta sección se describe cómo usar Windows y estructuras de sockets para programar una Bluetooth aplicación.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, tareas
- Windows Sockets
- programar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004095"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth Programación con Windows sockets

En esta sección se describe cómo usar Windows y estructuras de sockets para programar una Bluetooth aplicación. Puede encontrar información de referencia completa para los Windows API de Sockets en [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2); En esta sección solo se Bluetooth información específica de cada elemento de programación Windows Sockets.

También puede descargar el ejemplo [de conexión Bluetooth para](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) obtener un ejemplo completo.

Como con toda la programación de Windows Sockets, se debe llamar a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para iniciar la funcionalidad Windows Sockets y habilitar Bluetooth.

En los temas siguientes se proporcionan instrucciones sobre el uso de funciones y estructuras Windows Sockets con microsoft Bluetooth API:



| Tema                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth y aceptar](bluetooth-and-accept.md)                                                 | Bluetooth utiliza la [**función accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar los intentos de conexión entrantes en un socket.<br/>                                                                                                                                                                                                  |
| [Bluetooth y enlazar](bluetooth-and-bind.md)                                                     | Bluetooth utiliza la [**función bind**](/windows/desktop/api/winsock/nf-winsock-bind) para enlazar a un socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth y BLOB](bluetooth-and-blob.md)                                                     | Bluetooth utiliza la estructura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) para pasar o recibir datos específicos del transporte a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante las llamadas a las funciones [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService.** \* <br/>             |
| [Bluetooth conexión](bluetooth-and-connect.md)                                               | Bluetooth usa la función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para conectarse a un dispositivo Bluetooth destino, mediante un socket de Bluetooth creado anteriormente.<br/>                                                                                                                                                              |
| [Bluetooth y getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | La [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) proporciona la traducción del nombre de host a la dirección de los transportes basados en IP.<br/>                                                                                                                                                                                   |
| [Bluetooth y getpeername](bluetooth-and-getpeername.md)                                       | Se usa para recuperar la Bluetooth del dispositivo del mismo Bluetooth mismo nivel.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth y getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth usa la función [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) para recuperar la dirección del dispositivo del servidor y el número de puerto asignados a un socket mediante una llamada anterior a la [**función bind.**](/windows/desktop/api/winsock/nf-winsock-bind)<br/>                                                                                            |
| [Bluetooth y getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth utiliza la [**función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar varios parámetros asociados con el canal del servidor o la conexión. <br/>                                                                                                                                                           |
| [Bluetooth escucha, selección y cierre de la lista](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth las funciones [**listen,**](/windows/desktop/api/winsock2/nf-winsock2-listen) [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sin ninguna modificación de la programación estándar Windows Sockets.<br/>                                                                                                   |
| [Bluetooth operaciones de lectura y escritura](bluetooth-and-read-or-write-operations.md)             | Detalla las operaciones de lectura y escritura admitidas de Winsock.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth y setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth usa la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para establecer varios parámetros asociados al canal del servidor o a la conexión.<br/>                                                                                                                                                              |
| [Bluetooth y apagado](bluetooth-and-shutdown.md)                                             | Bluetooth usa la [**función shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) para desconectarse de la radio remota.<br/>                                                                                                                                                                                                             |
| [Bluetooth y socket](bluetooth-and-socket.md)                                                 | Bluetooth utiliza la [**función de socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket para las conexiones entrantes o salientes.<br/>                                                                                                                                                                                               |
| [Bluetooth y opciones de socket](bluetooth-and-socket-options.md)                                 | Detalla las opciones de socket compatibles con Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth y WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Se usa para convertir una dirección de dispositivo Bluetooth en una cadena, que a su vez se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) al recuperar información del servicio del dispositivo.<br/>                                           |
| [Bluetooth y WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth usa la [**función WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultar dispositivos y detectar servicios.<br/>                                                                                                                                                                         |
| [Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth usa la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para buscar coincidencias con las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth y WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth usa la función [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para finalizar una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)y quizás extendida en llamadas posteriores a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth y WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | La [**estructura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) se usa en operaciones como la consulta de dispositivos, la consulta del servicio y la configuración del servicio.<br/>                                                                                                                                                                |
| [Bluetooth y WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio dentro del espacio de nombres Bluetooth (NS \_ BTH) del registro.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

