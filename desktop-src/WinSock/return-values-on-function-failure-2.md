---
description: La constante de manifiesto SOCKET \_ ERROR se proporciona para comprobar el error de la función. Aunque el uso de esta constante no es obligatorio, se recomienda. En el ejemplo siguiente se muestra el uso de la constante SOCKET \_ ERROR.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valores devueltos en caso de error de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476116"
---
# <a name="return-values-on-function-failure"></a>Valores devueltos en caso de error de función

La constante de **manifiesto SOCKET \_ ERROR** se proporciona para comprobar el error de la función. Aunque el uso de esta constante no es obligatorio, se recomienda. En el ejemplo siguiente se muestra el uso de la **constante SOCKET \_ ERROR.**

Estilo típico de BSD (no funcionará en Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows Estilo


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

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Windows Códigos de error de sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



