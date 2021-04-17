---
description: Después de enlazar el socket a una dirección IP y un puerto del sistema, el servidor debe escuchar en esa dirección IP y el puerto para las solicitudes de conexión entrantes.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Escuchar en un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696374"
---
# <a name="listening-on-a-socket"></a>Escuchar en un socket

Después de enlazar el socket a una dirección IP y un puerto del sistema, el servidor debe escuchar en esa dirección IP y el puerto para las solicitudes de conexión entrantes.

## <a name="to-listen-on-a-socket"></a>Para escuchar en un socket

Llame a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , pasando como parámetros el socket creado y un valor para el *trabajo pendiente*, la longitud máxima de la cola de conexiones pendientes que se va a aceptar. En este ejemplo, el parámetro de *trabajo pendiente* se estableció en **SOMAXCONN**. Este valor es una constante especial que indica al proveedor Winsock de este socket que permita un número máximo razonable de conexiones pendientes en la cola. Compruebe si hay errores generales en el valor devuelto.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Siguiente paso: [aceptar una conexión](accepting-a-connection.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación Winsock Server](winsock-server-application.md)
</dt> <dt>

[Enlazar un socket](binding-a-socket.md)
</dt> </dl>

 

 



