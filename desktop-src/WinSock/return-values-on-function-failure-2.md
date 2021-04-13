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
# <a name="return-values-on-function-failure"></a><span data-ttu-id="866c3-105">Valores devueltos en un error de función</span><span class="sxs-lookup"><span data-stu-id="866c3-105">Return Values on Function Failure</span></span>

<span data-ttu-id="866c3-106">El error de **socket \_** de la constante del manifiesto se proporciona para comprobar el error de la función.</span><span class="sxs-lookup"><span data-stu-id="866c3-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="866c3-107">Aunque el uso de esta constante no es obligatorio, se recomienda.</span><span class="sxs-lookup"><span data-stu-id="866c3-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="866c3-108">En el ejemplo siguiente se muestra el uso de la constante de **\_ error de socket** .</span><span class="sxs-lookup"><span data-stu-id="866c3-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="866c3-109">Estilo BSD típico (no funcionará en Windows)</span><span class="sxs-lookup"><span data-stu-id="866c3-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="866c3-110">Estilo de Windows</span><span class="sxs-lookup"><span data-stu-id="866c3-110">Windows Style</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="866c3-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="866c3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866c3-112">Códigos de error: errno, h \_ errno y WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="866c3-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="866c3-113">Control de errores de Winsock</span><span class="sxs-lookup"><span data-stu-id="866c3-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="866c3-114">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="866c3-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="866c3-115">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="866c3-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="866c3-116">Códigos de error de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="866c3-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



