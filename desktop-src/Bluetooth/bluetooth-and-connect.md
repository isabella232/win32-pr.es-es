---
title: Bluetooth conexión
description: Bluetooth la función connect para conectarse a un dispositivo Bluetooth destino, mediante un socket de Bluetooth creado anteriormente.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- conectar Bluetooth
- Bluetooth conexión y conexión Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974625"
---
# <a name="bluetooth-and-connect"></a>Bluetooth conexión

Bluetooth usa la función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para conectarse a un dispositivo Bluetooth destino, mediante un socket de Bluetooth creado anteriormente. El *parámetro name* de la función **connect,** que es una estructura [**SOCKADDR \_ BTH,**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) debe especificar un destino Bluetooth dispositivo. Se usan dos mecanismos para identificar el dispositivo de destino:

-   La [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar directamente el número de puerto al que se solicita una conexión. Este mecanismo requiere que la aplicación realice sus propias consultas de SDP antes de intentar una [**operación de**](/windows/desktop/api/winsock2/nf-winsock2-connect) conexión.
-   La [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar el identificador de clase de servicio único del servicio al que desea conectarse. Si el dispositivo del mismo nivel tiene más de un [](/windows/desktop/api/winsock2/nf-winsock2-connect) puerto que corresponde al identificador de clase de servicio, la llamada a la función connect se conecta al primer servicio válido. Este mecanismo se puede usar sin consultas SDP anteriores.

Al usar la [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la [**función connect,**](/windows/desktop/api/winsock2/nf-winsock2-connect) se aplican los siguientes requisitos:

-   El **miembro btAddr** debe ser una dirección de radio remota válida.
-   Para el **miembro serviceClassId,** si el miembro de puerto es cero, el sistema intenta usar **serviceClassId** para resolver el puerto remoto correspondiente al servicio. La clase de servicio es un GUID normalizado de 128 bits, definido por la especificación Bluetooth datos. Los GUID comunes se definen mediante el Bluetooth Números asignados. Como alternativa, se puede usar un GUID único para una aplicación específica del dominio.
-   El **miembro** de puerto debe ser un puerto remoto válido o cero si se especifica el miembro **serviceClassId.**

En la tabla siguiente se enumeran los códigos de resultados Bluetooth y la [**función connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

| Error o error\#                    | Descripción                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) a la que se llama para el socket ya conectado. |
| WSAEACCES10013<br/>        | La conexión de la aplicación solicitó autenticación, pero no se pudo establecer la autenticación.        |
| WSAENOBUFS10055<br/>       | Error irrecuperable de memoria no recuperable.                                                 |
| WSAEADDRINUSE10048<br/>    | El número de puerto o canal solicitado está en uso.                                       |
| WSAETIMEDOUT10060<br/>     | Se agote el tiempo de espera de E/S en el Bluetooth de radio (TIEMPO DE ESPERA DE \_ PÁGINA).                    |
| WSAEDISCON10101<br/>       | Canal RFCOMM desconectado por el emparejamiento remoto.                                    |
| WSAECONNRESET10054<br/>    | Multiplexor RFCOMM (sesión) desconectado por el par remoto.                      |
| WSAECOBORTED10053<br/>  | Socket cerrado por la aplicación.                                                   |
| WSAENETUNREACH10051<br/>   | Error distinto del tiempo de espera en L2CAP o Bluetooth nivel de radio.                       |
| WSAEHOSTDOWN10064<br/>     | La RFCOMM recibió la respuesta dm.                                                   |
| WSAENETDOWN10050<br/>      | Error de red inesperado.                                                          |
| WSAESHUTDOWN10058<br/>     | Canal L2CAP desconectado por el emparejamiento remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Bluetooth puerto o canal o dirección del dispositivo no válidos.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento de pila de controladores u otro error causado por un error.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

