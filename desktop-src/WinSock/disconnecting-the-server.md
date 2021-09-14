---
description: Una vez que el servidor ha completado la recepción de datos del cliente y el envío de datos al cliente, el servidor se desconecta del cliente y apaga el socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Desconectar el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068289"
---
# <a name="disconnecting-the-server"></a>Desconectar el servidor

Una vez que el servidor ha completado la recepción de datos del cliente y el envío de datos al cliente, el servidor se desconecta del cliente y apaga el socket.

**Para desconectar y apagar un socket**

1.  Cuando el servidor haya terminado de enviar datos al cliente, se puede llamar a la función [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) especificando SD SEND para apagar el lado de \_ envío del socket. Esto permite al cliente liberar algunos de los recursos para este socket. La aplicación de servidor todavía puede recibir datos en el socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Cuando la aplicación cliente ha terminado de recibir datos, se llama a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para cerrar el socket.

    Cuando la aplicación cliente se completa mediante el archivo DLL Windows Sockets, se llama a la función [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) para liberar recursos.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Completar código fuente del servidor

-   [Completar código de servidor](complete-server-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Recepción y envío de datos en el servidor](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Ejecución del ejemplo de código de cliente y servidor de Winsock](finished-server-and-client-code.md)
</dt> </dl>

 

 



