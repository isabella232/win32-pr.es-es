---
description: Una vez que el cliente ha finalizado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Desconectar el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360305"
---
# <a name="disconnecting-the-client"></a>Desconectar el cliente

Una vez que el cliente ha finalizado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.

**Para desconectar y apagar un socket**

1.  Cuando el cliente ha terminado de enviar datos al servidor, se puede llamar a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) especificando el \_ envío de SD para apagar el lado de envío del socket. Esto permite al servidor liberar algunos de los recursos de este socket. La aplicación cliente todavía puede recibir datos en el socket.
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

    Cuando la aplicación cliente se completa mediante el archivo DLL de Windows Sockets, se llama a la función [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) para liberar recursos.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Completar código fuente de cliente

-   [Completar el código de cliente](complete-client-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Enviar y recibir datos en el cliente](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



