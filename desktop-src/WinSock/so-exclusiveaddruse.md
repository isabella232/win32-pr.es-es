---
description: La opción de socket SO EXCLUSIVEADDRUSE impide que otros sockets se enlazan forzadamente a \_ la misma dirección y puerto.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: SO_EXCLUSIVEADDRUSE de socket (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9d7b00cc2fcd01fc9d440ce2ef889a9e1be937d5d83af90cfa71bf6f83d14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927347"
---
# <a name="so_exclusiveaddruse-socket-option"></a>Opción \_ de socket SO EXCLUSIVEADDRUSE

La opción de socket SO EXCLUSIVEADDRUSE impide que otros sockets se enlazan forzadamente a \_ la misma dirección y puerto.

## <a name="syntax"></a>Syntax

La opción SO EXCLUSIVEADDRUSE impide que otros sockets se enlazan forzadamente a la misma dirección y puerto, una práctica habilitada por la opción de \_ socket SO \_ REUSEADDR. Dicha reutilización se puede ejecutar mediante aplicaciones malintencionadas para interrumpir la aplicación. La opción SO \_ EXCLUSIVEADDRUSE es muy útil para los servicios del sistema que requieren alta disponibilidad.

En el ejemplo de código siguiente se muestra cómo establecer esta opción.


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



Para tener cualquier efecto, se debe establecer la opción SO EXCLUSIVADDRUSE antes de llamar a la función de enlace (esto también se aplica a la opción \_ SO [](/windows/desktop/api/winsock/nf-winsock-bind) \_ REUSEADDR). En la tabla 1 se enumeran los efectos de establecer la opción SO \_ EXCLUSIVEADDRUSE. El carácter comodín indica el enlace a la dirección comodín, como 0.0.0.0 para IPv4 y :: para IPv6. Específico indica el enlace a una interfaz específica, como enlazar una dirección IP asignada a un adaptador. Specific2 indica el enlace a una dirección específica que no sea la dirección enlazada a en el caso específico.

> [!Note]  
> El caso Specific2 solo es aplicable cuando el primer enlace se realiza con una dirección específica; Para el caso en el que el primer socket está enlazado al carácter comodín, la entrada de Específico abarca todos los casos de direcciones específicos.

 

Por ejemplo, considere un equipo con dos interfaces IP: 10.0.0.1 y 10.99.99.99. Si el primer enlace es a 10.0.0.1 y al puerto 5150 con la opción SO EXCLUSIVEADDRUSE establecida, el segundo enlace a \_ 10.99.99.99 y al puerto 5150 con cualquiera o ningún conjunto de opciones se realiza correctamente. Sin embargo, si el primer socket está enlazado a la dirección comodín (0.0.0.0) y al puerto 5150 con SO EXCLUSIVEADDRUSE establecido, cualquier enlace posterior al mismo puerto (independientemente de la dirección IP) producirá un error con \_ WSAEADDRINUSE (10048) o WSAEACCESS (10013), en función de las opciones establecidas en el segundo socket de enlace.

### <a name="bind-behavior-with-various-options-set"></a>Enlazar el comportamiento con varias opciones establecidas



Segundo enlace

Primer enlace

*SO \_ EXCLUSIVEADDRUSE*

*Sin opciones o* *SO \_ REUSEADDR*

*Comodín*

*Específico*

*Comodín*

*Específico*

${ROWSPAN3}$*SO \_ EXCLUSIVEADDRUSE*${REMOVE}$  

*Comodín*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Específico*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Specific2*

N/D

Success

N/D

Success

${ROWSPAN3}$*Sin opciones*${REMOVE}$  

*Comodín*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Específico*

Error (10048)

Error (10048)

Error (10048)

Error (10048)

*Specific2*

N/D

Success

N/D

Success

${ROWSPAN3}$*SO \_ REUSEADDR*${REMOVE}$  

*Comodín*

Error (10013)

Error (10013)

Correcto\*

Success

*Específico*

Error (10013)

Error (10013)

Success

Correcto\*

*Specific2*

N/D

Success

N/D

Success

\* El comportamiento no está definido en cuanto a qué socket recibirá paquetes.



 

En el caso de que el primer enlace no establece ninguna opción o SO REUSEADDR, y el segundo enlace realiza so \_ REUSEADDR, el segundo socket ha superado el puerto y el comportamiento con respecto a qué socket recibirá paquetes no está \_ predeterminado. SO \_ EXCLUSIVEADDRUSE se introdujo para abordar esta situación.

Un socket con so EXCLUSIVEADDRUSE establecido no siempre se puede \_ reutilizar inmediatamente después del cierre del socket. Por ejemplo, si un socket de escucha con el conjunto de marcas exclusivo acepta una conexión después de la cual se cierra el socket de escucha, otro socket no se puede enlazar al mismo puerto que el primer socket de escucha con la marca exclusiva hasta que la conexión aceptada ya no esté activa.

Esta situación puede ser bastante complicada; aunque se haya cerrado el socket, es posible que el transporte subyacente no finalice su conexión. Incluso después de cerrar el socket, el sistema debe enviar todos los datos almacenados en búfer, transmitir una desconexión correcta al mismo nivel y esperar una desconexión correcta del mismo nivel. Por lo tanto, es posible que el transporte subyacente nunca libere la conexión, como cuando el mismo nivel anuncia una ventana de tamaño cero u otros ataques de este tipo. En el ejemplo anterior, el socket de escucha se cerró después de que se aceptara una conexión de cliente. Ahora, incluso si la conexión de cliente está cerrada, es posible que el puerto no se vuelva a usar si la conexión de cliente permanece en un estado activo debido a datos no reconocidos, etc.

Para evitar esta situación, las aplicaciones [](/windows/desktop/api/winsock/nf-winsock-shutdown) deben garantizar un apagado correcto: llamar al apagado con la marca SD SEND y, a continuación, esperar en un bucle recv hasta que \_ se devuelvan cero bytes. [](/windows/desktop/api/winsock/nf-winsock-recv) Al hacerlo, se evita el problema asociado con la reutilización de puertos, se garantizan todos los datos recibidos por el mismo nivel y se garantiza al mismo nivel que todos sus datos se han recibido correctamente.

La opción SO LINGER se puede establecer en un socket para evitar que el puerto entre en uno de los estados de espera activos; sin embargo, no se recomienda hacerlo porque puede provocar efectos no deseados, ya que puede hacer que se restablezca la \_ conexión. Por ejemplo, si los datos se han recibido pero aún no han sido reconocidos por el mismo nivel y el equipo local cierra el socket con SO LINGER establecido, la conexión se restablece y el mismo nivel descarta los datos no \_ reconocidos. Además, es difícil elegir un momento adecuado para quedarse. Un valor demasiado pequeño da como resultado muchas conexiones anuladas, mientras que un tiempo de espera grande puede hacer que el sistema sea vulnerable a ataques por denegación de servicio al establecer muchas conexiones y, por tanto, detener numerosos subprocesos de aplicación.

> [!Note]  
> Un socket que usa la opción SO EXCLUSIVEADDRUSE debe apagarse correctamente \_ antes de cerrarlo. Si no lo hace, puede producirse un ataque por denegación de servicio si es necesario reiniciar el servicio asociado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winsock2.h</dt> </dl> |



 

 




