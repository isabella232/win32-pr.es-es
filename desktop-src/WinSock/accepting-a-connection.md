---
description: Una vez que el socket escucha una conexión, el programa debe controlar las solicitudes de conexión en ese socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Aceptar una conexión (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dcdebb660ec290ee5723b569ca358e0317777300a479e17a516e594744b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996895"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>Aceptar una conexión (Windows sockets 2)

Una vez que el socket escucha una conexión, el programa debe controlar las solicitudes de conexión en ese socket.

**Para aceptar una conexión en un socket**

1.  Cree un objeto **SOCKET temporal** denominado ClientSocket para aceptar conexiones de clientes.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalmente, una aplicación de servidor se diseñaría para escuchar las conexiones de varios clientes. En el caso de los servidores de alto rendimiento, se usan normalmente varios subprocesos para controlar las conexiones de varios clientes.

    Hay varias técnicas de programación diferentes que usan Winsock que se pueden usar para escuchar varias conexiones de cliente. Una técnica de programación consiste en crear un bucle continuo que comprueba si hay solicitudes de conexión mediante la función [**de**](/windows/desktop/api/Winsock2/nf-winsock2-listen) escucha (vea [Listening on a Socket](listening-on-a-socket.md)). Si se produce una solicitud de conexión, la aplicación llama a la función [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) y pasa el trabajo a otro subproceso para controlar la solicitud. Otras técnicas de programación son posibles.

    Tenga en cuenta que este ejemplo básico es muy sencillo y no usa varios subprocesos. El ejemplo también solo escucha y acepta una sola conexión.

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  Cuando se ha aceptado la conexión de cliente, una aplicación de servidor normalmente pasaría el socket de cliente aceptado (la variable ClientSocket en el código de ejemplo anterior) a un subproceso de trabajo o a un puerto de finalización de E/S y seguiría aceptando conexiones adicionales. En este ejemplo básico, el servidor continúa con el paso siguiente.

    Hay una serie de otras técnicas de programación que se pueden usar para escuchar y aceptar varias conexiones. Entre ellas se incluyen el uso [**de las**](/windows/desktop/api/Winsock2/nf-winsock2-select) funciones [**select o WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) Algunos ejemplos de algunas de estas diversas técnicas de programación se muestran en advanced [Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK) (Ejemplos avanzados de Winsock incluidos con el Kit de desarrollo de software (SDK) de Microsoft Windows).

    > [!Note]  
    > En sistemas Unix, una técnica de programación común para los servidores era que una aplicación escuchara las conexiones. Cuando se aceptó una conexión,  el proceso primario llamaría a la función de bifurcación para crear un nuevo proceso secundario para controlar la conexión de cliente, heredando el socket del elemento primario. Esta técnica de programación no se admite en Windows, ya que **no** se admite la función de bifurcación. Esta técnica tampoco suele ser adecuada para servidores de alto rendimiento, ya que los recursos necesarios para crear un nuevo proceso son mucho mayores que los necesarios para un subproceso.

     

Paso siguiente: [Recepción y envío de datos en el servidor](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Escuchar en un socket](listening-on-a-socket.md)
</dt> </dl>

 

 
