---
description: El error de SOCKET de la constante del manifiesto \_ se proporciona para comprobar el error de la función. Aunque el uso de esta constante no es obligatorio, se recomienda. En el ejemplo siguiente se muestra el uso de la \_ constante de error de socket.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valores devueltos en un error de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276153"
---
# <a name="return-values-on-function-failure"></a>Valores devueltos en un error de función

El error de **socket \_** de la constante del manifiesto se proporciona para comprobar el error de la función. Aunque el uso de esta constante no es obligatorio, se recomienda. En el ejemplo siguiente se muestra el uso de la constante de **\_ error de socket** .

Estilo BSD típico (no funcionará en Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Estilo de Windows


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error: errno, h \_ errno y WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Control de errores de Winsock](handling-winsock-errors.md)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



