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
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588465"
---
# <a name="bluetooth-and-connect"></a>Bluetooth conexión

Bluetooth la función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para conectarse a un dispositivo Bluetooth destino, mediante un socket de Bluetooth creado anteriormente. El *parámetro name* de la función **connect,** que es una estructura [**SOCKADDR \_ BTH,**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) debe especificar un destino Bluetooth dispositivo. Se usan dos mecanismos para identificar el dispositivo de destino:

-   La [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar directamente el número de puerto al que se solicita una conexión. Este mecanismo requiere que la aplicación realice sus propias consultas de SDP antes de intentar una operación [**de**](/windows/desktop/api/winsock2/nf-winsock2-connect) conexión.
-   La [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar el identificador de clase de servicio único del servicio al que desea conectarse. Si el dispositivo del mismo nivel tiene más de un puerto que corresponde al identificador de clase de servicio, la llamada a la función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) se conecta al primer servicio válido. Este mecanismo se puede usar sin consultas SDP anteriores.

Al usar la [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la [**función connect,**](/windows/desktop/api/winsock2/nf-winsock2-connect) se aplican los siguientes requisitos:

-   El **miembro btAddr** debe ser una dirección de radio remota válida.
-   Para el **miembro serviceClassId,** si el miembro port es cero, el sistema intenta usar **serviceClassId** para resolver el puerto remoto correspondiente al servicio. La clase de servicio es un GUID normalizado de 128 bits, definido por la especificación Bluetooth normalizado. Los GUID comunes se definen mediante el documento Bluetooth Números asignados. Como alternativa, se puede usar un GUID único para una aplicación específica del dominio.
-   El **miembro** de puerto debe ser un puerto remoto válido o cero si se especifica el **miembro serviceClassId.**

En la tabla siguiente se enumeran los códigos de resultados Bluetooth y la [**función connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

| Error o error\#                    | Descripción                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Función [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) a la que se llama para el socket ya conectado. |
| WSAEACCES10013<br/>        | La aplicación de conexión solicitó la autenticación, pero no se pudo establecer la autenticación.        |
| WSAENOBUFS10055<br/>       | Error de memoria fuera de memoria irrecuperable.                                                 |
| WSAEADDRINUSE10048<br/>    | El número de puerto o canal solicitado está en uso.                                       |
| WSAETIMEDOUT10060<br/>     | Se agote el tiempo de espera de E/S en el Bluetooth de radio (TIEMPO DE ESPERA DE \_ PÁGINA).                    |
| WSAEDISCON10101<br/>       | Canal RFCOMM desconectado por el mismo nivel remoto.                                    |
| WSAECONNRESET10054<br/>    | Multiplexor RFCOMM (sesión) desconectado por el par remoto.                      |
| WSAECOBORTED10053<br/>  | Socket cerrado por la aplicación.                                                   |
| WSAENETUNREACH10051<br/>   | Error distinto del tiempo de espera en L2CAP o Bluetooth de radio.                       |
| WSAEHOSTDOWN10064<br/>     | El RFCOMM recibió la respuesta dm.                                                   |
| WSAENETDOWN10050<br/>      | Error de red inesperado.                                                          |
| WSAESHUTDOWN10058<br/>     | Canal L2CAP desconectado por el mismo nivel remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Bluetooth puerto, canal o dirección del dispositivo no son válidos.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento de pila de controladores u otro error produjo un error.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

