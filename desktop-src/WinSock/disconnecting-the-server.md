---
description: Una vez que el servidor ha finalizado la recepción de datos del cliente y el envío de datos de vuelta al cliente, el servidor se desconecta del cliente y apaga el socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Desconectar el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898365"
---
# <a name="disconnecting-the-server"></a>Desconectar el servidor

Una vez que el servidor ha finalizado la recepción de datos del cliente y el envío de datos de vuelta al cliente, el servidor se desconecta del cliente y apaga el socket.

**Para desconectar y apagar un socket**

1.  Cuando el servidor haya terminado de enviar datos al cliente, se puede llamar a la función [**de**](/windows/desktop/api/winsock/nf-winsock-shutdown) apagado especificando SD SEND para apagar el lado \_ de envío del socket. Esto permite al cliente liberar algunos de los recursos para este socket. La aplicación de servidor todavía puede recibir datos en el socket.
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

    

## <a name="complete-server-source-code"></a>Código fuente completo del servidor

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

 

 



