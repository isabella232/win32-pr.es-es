---
description: Después de enlazar el socket a una dirección IP y un puerto en el sistema, el servidor debe escuchar en esa dirección IP y puerto las solicitudes de conexión entrantes.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Escuchar en un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6d98a13fc6e994fb5a264827b6b93047fd24e03d3e3f9953203b1fa15140f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569785"
---
# <a name="listening-on-a-socket"></a>Escuchar en un socket

Después de enlazar el socket a una dirección IP y un puerto en el sistema, el servidor debe escuchar en esa dirección IP y puerto las solicitudes de conexión entrantes.

## <a name="to-listen-on-a-socket"></a>Para escuchar en un socket

Llame a [**la función de**](/windows/desktop/api/Winsock2/nf-winsock2-listen) escucha, pasando como parámetros el socket creado y un valor para el *trabajo* pendiente , longitud máxima de la cola de conexiones pendientes que se aceptará. En este ejemplo, el *parámetro de trabajo pendiente* se estableció en **SOMAXCONN.** Este valor es una constante especial que indica al proveedor winsock para este socket que permita un número máximo razonable de conexiones pendientes en la cola. Compruebe si hay errores generales en el valor devuelto.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Paso siguiente: [Aceptar una conexión](accepting-a-connection.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Enlazar un socket](binding-a-socket.md)
</dt> </dl>

 

 



