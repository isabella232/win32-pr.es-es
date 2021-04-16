---
description: La \_ opción de socket so EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opción de socket de SO_EXCLUSIVEADDRUSE (WinSock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705595"
---
# <a name="so_exclusiveaddruse-socket-option"></a>\_EXCLUSIVEADDRUSE socket, opción

La \_ opción de socket so EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto.

## <a name="syntax"></a>Sintaxis

La \_ opción for EXCLUSIVEADDRUSE impide que otros Sockets se enlacen a la misma dirección y puerto, una práctica habilitada por la \_ opción de socket for REUSEADDR. Las aplicaciones malintencionadas pueden ejecutar esta reutilización para interrumpir la aplicación. La \_ opción for EXCLUSIVEADDRUSE es muy útil para los servicios del sistema que requieren alta disponibilidad.

En el ejemplo de código siguiente se muestra la configuración de esta opción.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



Para que surta efecto, se \_ debe establecer la opción for EXCLUSIVADDRUSE antes de llamar a la función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) (esto también se aplica a la \_ opción for REUSEADDR). En la tabla 1 se muestran los efectos de establecer la \_ opción for EXCLUSIVEADDRUSE. El carácter comodín indica el enlace a la dirección comodín, como 0.0.0.0 para IPv4 y:: para IPv6. Específico indica el enlace a una interfaz específica, como enlazar una dirección IP asignada a un adaptador. Specific2 indica el enlace a una dirección específica diferente de la dirección enlazada a en el caso específico.

> [!Note]  
> El caso Specific2 solo es aplicable cuando el primer enlace se realiza con una dirección específica; en el caso en el que el primer socket está enlazado al carácter comodín, la entrada de cubre todos los casos de direcciones específicas.

 

Por ejemplo, Imagine un equipo con dos interfaces IP: 10.0.0.1 y 10.99.99.99. Si el primer enlace es 10.0.0.1 y el puerto 5150 con la \_ opción for EXCLUSIVEADDRUSE establecida, el segundo enlace a 10.99.99.99 y el puerto 5150 con una o ninguna de las opciones establecidas se realiza correctamente. Sin embargo, si el primer socket se enlaza a la dirección comodín (0.0.0.0) y al puerto 5150 por lo que se \_ establece EXCLUSIVEADDRUSE, se producirá un error en cualquier enlace subsiguiente al mismo puerto, independientemente de la dirección IP, con WSAEADDRINUSE (10048) o WSAEACCESS (10013), en función de las opciones que se hayan establecido en el segundo socket BIND.

### <a name="bind-behavior-with-various-options-set"></a>Comportamiento de enlace con varias opciones establecidas



Segundo enlace

Primer enlace

*\_EXCLUSIVEADDRUSE*

*Ninguna opción* o *\_ REUSEADDR*

*Wildcard (Carácter comodín)*

*Cuestión*

*Wildcard (Carácter comodín)*

*Cuestión*

$ {ROWSPAN3} $*so \_ EXCLUSIVEADDRUSE*$ {Remove} $  

*Wildcard (Carácter comodín)*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Cuestión*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Specific2*

N/D

Correcto

N/D

Correcto

$ {ROWSPAN3} $*no hay opciones*$ {Remove} $  

*Wildcard (Carácter comodín)*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Cuestión*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Specific2*

N/D

Correcto

N/D

Correcto

$ {ROWSPAN3} $*so \_ REUSEADDR*$ {Remove} $  

*Wildcard (Carácter comodín)*

Error (10013)

Error (10013)

Correcto\*

Correcto

*Cuestión*

Error (10013)

Error (10013)

Correcto

Correcto\*

*Specific2*

N/D

Correcto

N/D

Correcto

\* El comportamiento no está definido en cuanto al socket que recibirá los paquetes.



 

En el caso en el que el primer enlace no establece ninguna opción, por lo que \_ REUSEADDR, y el segundo enlace realiza una, de modo que \_ REUSEADDR, el segundo socket ha sobrecargado el puerto y el comportamiento con respecto a qué socket recibirá los paquetes sin determinar. Por lo tanto, \_ se presentó EXCLUSIVEADDRUSE para abordar esta situación.

\_No siempre se puede volver a usar un socket con EXCLUSIVEADDRUSE Set inmediatamente después del cierre del socket. Por ejemplo, si un socket de escucha con el conjunto de marcas exclusivo acepta una conexión después de la cual se cierra el socket de escucha, otro socket no puede enlazar con el mismo puerto que el primer socket de escucha con la marca exclusiva hasta que la conexión aceptada ya no esté activa.

Esta situación puede ser bastante complicada; Aunque el socket se ha cerrado, es posible que el transporte subyacente no termine su conexión. Incluso después de cerrar el socket, el sistema debe enviar todos los datos almacenados en búfer, transmitir una desconexión correcta al elemento del mismo nivel y esperar a que se desconecten correctamente del elemento del mismo nivel. Por lo tanto, es posible que el transporte subyacente nunca libere la conexión, por ejemplo, cuando el elemento del mismo nivel anuncia una ventana de tamaño cero u otros ataques de este tipo. En el ejemplo anterior, el socket de escucha se cerró después de aceptar una conexión de cliente. Ahora incluso si la conexión de cliente está cerrada, es posible que el puerto todavía no se reutilice si la conexión de cliente permanece en estado activo debido a datos no confirmados, etc.

Para evitar esta situación, las aplicaciones deben garantizar un cierre estable: llamar a [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con la \_ marca de envío SD y, después, esperar en un bucle [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) hasta que se devuelvan cero bytes. De este modo, se evita el problema asociado a la reutilización de puertos, se garantiza que todos los datos los recibió el elemento del mismo nivel y se garantiza que todos sus datos se recibieron correctamente.

La \_ opción so persistente se puede establecer en un socket para evitar que el puerto pase a uno de los Estados de espera activos; sin embargo, no se recomienda hacerlo porque puede provocar efectos no deseados, ya que puede provocar que se restablezca la conexión. Por ejemplo, si los datos se han recibido pero aún no han sido confirmados por el elemento del mismo nivel y el equipo local cierra el socket con este \_ conjunto de permanencia, se restablece la conexión y el elemento del mismo nivel descarta los datos no confirmados. Además, es difícil elegir un período de permanencia adecuado. un valor demasiado pequeño resulta en muchas conexiones anuladas, mientras que un tiempo de espera grande puede dejar que el sistema sea vulnerable a ataques de denegación de servicio mediante el establecimiento de muchas conexiones y, por tanto, la detención de numerosos subprocesos de aplicación.

> [!Note]  
> Un socket que use la opción for \_ EXCLUSIVEADDRUSE debe cerrarse correctamente antes de cerrarlo. Si no lo hace, puede producirse un ataque de denegación de servicio si el servicio asociado tiene que reiniciarse.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinSock2. h</dt> </dl> |



 

 




