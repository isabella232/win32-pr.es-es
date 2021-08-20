---
description: Una vez que el cliente ha completado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Desconectar el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9689a1877ee015188583ef4a530dbd054cd47a2b7ecf2da1c89d4f341e90bc8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927884"
---
# <a name="disconnecting-the-client"></a>Desconectar el cliente

Una vez que el cliente ha completado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.

**Para desconectar y apagar un socket**

1.  Cuando el cliente haya terminado de enviar datos al servidor, se puede llamar a la función [**de**](/windows/desktop/api/winsock/nf-winsock-shutdown) apagado especificando SD SEND para apagar el lado \_ de envío del socket. Esto permite que el servidor libere algunos de los recursos para este socket. La aplicación cliente todavía puede recibir datos en el socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Cuando la aplicación cliente ha terminado de recibir datos, se llama a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para cerrar el socket.

    Cuando la aplicación cliente se completa mediante el archivo DLL Windows Sockets, se llama a la función [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) para liberar recursos.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Completar código fuente de cliente

-   [Completar código de cliente](complete-client-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente winsock](winsock-client-application.md)
</dt> <dt>

[Envío y recepción de datos en el cliente](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



