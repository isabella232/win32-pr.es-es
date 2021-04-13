---
title: Bluetooth y conectar
description: Bluetooth usa la función Connect para conectarse a un dispositivo Bluetooth de destino mediante un Socket Bluetooth creado previamente.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- conectar Bluetooth
- Bluetooth y conexión Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488194"
---
# <a name="bluetooth-and-connect"></a>Bluetooth y conectar

Bluetooth usa la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para conectarse a un dispositivo Bluetooth de destino mediante un Socket Bluetooth creado previamente. El parámetro *Name* de la función **Connect** , que es una [**estructura \_ BTH de SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , debe especificar un dispositivo Bluetooth de destino. Se usan dos mecanismos para identificar el dispositivo de destino:

-   La estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar directamente el número de puerto al que se solicita una conexión. Este mecanismo requiere que la aplicación realice sus propias consultas SDP antes de intentar una operación de [**conexión**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   La estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) puede especificar el identificador único de la clase de servicio del servicio al que desea conectarse. Si el dispositivo del mismo nivel tiene más de un puerto que corresponde al identificador de clase de servicio, la llamada de función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) se conecta al primer servicio válido. Este mecanismo se puede usar sin consultas SDP anteriores.

Cuando se usa la estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , se aplican los requisitos siguientes:

-   El miembro **btAddr** debe ser una dirección de radio remota válida.
-   En el caso del miembro **serviceClassId** , si el miembro del puerto es cero, el sistema intenta usar **serviceClassId** para resolver el puerto remoto que corresponde al servicio. La clase de servicio es un GUID de 128 bits normalizado, definido por la especificación de Bluetooth. Los GUID comunes se definen en el documento números asignados de Bluetooth. Como alternativa, se puede usar un GUID único para una aplicación específica del dominio.
-   El miembro de **Puerto** debe ser un puerto remoto válido o cero si se especifica el miembro **serviceClassId** .

En la tabla siguiente se enumeran los códigos de resultado de Bluetooth y la función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Error/Error\#                    | Descripción                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | La función [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) llamada para el socket ya conectado. |
| WSAEACCES10013<br/>        | Conectando la autenticación solicitada de la aplicación, pero se produjo un error de autenticación.        |
| WSAENOBUFS10055<br/>       | Error irrecuperable de memoria insuficiente.                                                 |
| WSAEADDRINUSE10048<br/>    | El número de puerto o canal solicitado está en uso.                                       |
| WSAETIMEDOUT10060<br/>     | Se agotó el tiempo de espera de e/s en el nivel de radio Bluetooth (tiempo de espera de página \_ ).                    |
| WSAEDISCON10101<br/>       | Canal RFCOMM desconectado por el equipo remoto del mismo nivel.                                    |
| WSAECONNRESET10054<br/>    | Multiplexor de RFCOMM (sesión) desconectado por el equipo remoto del mismo nivel.                      |
| WSAECONNABORTED10053<br/>  | Socket apagado por aplicación.                                                   |
| WSAENETUNREACH10051<br/>   | Error distinto del tiempo de espera en el nivel de radio de L2CAP o Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | Respuesta de DM recibida de RFCOMM.                                                   |
| WSAENETDOWN10050<br/>      | Error de red inesperado.                                                          |
| WSAESHUTDOWN10058<br/>     | El canal L2CAP está desconectado por el equipo remoto del mismo nivel.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Puerto/canal Bluetooth o dirección de dispositivo no válido.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento de pila de controladores u otro error provocado por un error.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**conéctelo**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

