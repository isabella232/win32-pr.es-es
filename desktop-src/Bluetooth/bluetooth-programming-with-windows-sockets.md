---
title: Programación de Bluetooth con Windows Sockets
description: En esta sección se describe cómo usar las funciones y estructuras de Windows Sockets para programar una aplicación Bluetooth.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, tareas
- Windows Sockets
- programar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656363"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Programación de Bluetooth con Windows Sockets

En esta sección se describe cómo usar las funciones y estructuras de Windows Sockets para programar una aplicación Bluetooth. Puede encontrar información de referencia completa de los elementos de la API de Windows Sockets en [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2); en esta sección solo se proporciona información específica de Bluetooth para cada elemento de programación de Windows Sockets.

También puede descargar el [ejemplo de conexión Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obtener un ejemplo completo.

Al igual que con la programación de la aplicación de Windows Sockets, se debe llamar a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para iniciar la funcionalidad de Windows Sockets y habilitar Bluetooth.

En los temas siguientes se proporcionan instrucciones sobre el uso de las funciones y estructuras de Windows Sockets con la API de Microsoft Bluetooth:



| Tema                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth y aceptar](bluetooth-and-accept.md)                                                 | Bluetooth usa la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar los intentos de conexión entrantes en un socket.<br/>                                                                                                                                                                                                  |
| [Bluetooth y BIND](bluetooth-and-bind.md)                                                     | Bluetooth utiliza la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) para enlazar con un socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth y BLOB](bluetooth-and-blob.md)                                                     | Bluetooth usa la estructura de [**blobs**](/windows/desktop/api/nspapi/ns-nspapi-blob) para pasar o recibir datos específicos del transporte a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante las llamadas a las funciones [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* . <br/>             |
| [Bluetooth y conectar](bluetooth-and-connect.md)                                               | Bluetooth usa la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para conectarse a un dispositivo Bluetooth de destino mediante un Socket Bluetooth creado previamente.<br/>                                                                                                                                                              |
| [Bluetooth y función getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | La función [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) proporciona traducción desde el nombre de host a la dirección para los transportes basados en IP.<br/>                                                                                                                                                                                   |
| [Bluetooth y getpeername](bluetooth-and-getpeername.md)                                       | Se usa para recuperar la dirección Bluetooth del dispositivo Bluetooth del mismo nivel.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth y getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth usa la función [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) para recuperar la dirección del dispositivo de servidor y el número de Puerto asignados a un socket a través de una llamada anterior a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth y getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth usa la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar varios parámetros asociados con el canal de servidor o la conexión. <br/>                                                                                                                                                           |
| [Bluetooth y escuchar, seleccionar y closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth usa las funciones [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sin ninguna modificación de la programación estándar de Windows Sockets.<br/>                                                                                                   |
| [Bluetooth y operaciones de lectura o escritura](bluetooth-and-read-or-write-operations.md)             | Detalla las operaciones de lectura y escritura de Winsock admitidas.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth y-i](bluetooth-and-setsockopt.md)                                         | Bluetooth usa la [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función-to para establecer diversos parámetros asociados con el canal de servidor o la conexión.<br/>                                                                                                                                                              |
| [Bluetooth y apagado](bluetooth-and-shutdown.md)                                             | Bluetooth usa la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) para desconectarse de la radio remota.<br/>                                                                                                                                                                                                             |
| [Bluetooth y socket](bluetooth-and-socket.md)                                                 | Bluetooth usa la función [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) para crear un socket para las conexiones entrantes o salientes.<br/>                                                                                                                                                                                               |
| [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md)                                 | Detalla las opciones de socket compatibles con Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth y WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Se usa para convertir una dirección de dispositivo Bluetooth en una cadena, que a su vez se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) cuando se recupera información del servicio de dispositivo.<br/>                                           |
| [Bluetooth y WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth usa la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultar dispositivos y detectar servicios.<br/>                                                                                                                                                                         |
| [Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth usa la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para hacer coincidir las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth y WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth usa la función [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para finalizar una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)y, quizás, extendida en llamadas posteriores a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth y WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | La estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) se usa en operaciones como la consulta de dispositivos, la consulta de servicio y la configuración del servicio.<br/>                                                                                                                                                                |
| [Bluetooth y WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio en el espacio de nombres Bluetooth (NS \_ BTH) del registro.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

