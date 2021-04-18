---
description: Una vez que el socket está escuchando una conexión, el programa debe controlar las solicitudes de conexión en ese socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Aceptación de una conexión (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652423"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>Aceptación de una conexión (Windows Sockets 2)

Una vez que el socket está escuchando una conexión, el programa debe controlar las solicitudes de conexión en ese socket.

**Para aceptar una conexión en un socket**

1.  Cree un objeto de **socket** temporal denominado ClientSocket para aceptar conexiones de los clientes.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalmente, una aplicación de servidor se diseñaría para escuchar las conexiones de varios clientes. En el caso de los servidores de alto rendimiento, se suelen usar varios subprocesos para administrar varias conexiones de cliente.

    Hay varias técnicas de programación diferentes con Winsock que se pueden usar para realizar escuchas de varias conexiones de cliente. Una técnica de programación consiste en crear un bucle continuo que compruebe las solicitudes de conexión mediante la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (consulte [escucha en un socket](listening-on-a-socket.md)). Si se produce una solicitud de conexión, la aplicación llama a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) y pasa el trabajo a otro subproceso para controlar la solicitud. Son posibles otras técnicas de programación.

    Tenga en cuenta que este ejemplo básico es muy sencillo y no utiliza varios subprocesos. El ejemplo también simplemente escucha y acepta una única conexión.

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

    

3.  Una vez aceptada la conexión de cliente, una aplicación de servidor pasaría normalmente el socket de cliente aceptado (la variable ClientSocket del código de ejemplo anterior) a un subproceso de trabajo o a un puerto de finalización de e/s y seguir aceptando conexiones adicionales. En este ejemplo básico, el servidor continúa con el paso siguiente.

    Existen otras técnicas de programación que se pueden utilizar para realizar escuchas y aceptar varias conexiones. Esto incluye el uso de las funciones [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . En los [ejemplos avanzados de Winsock](getting-started-with-winsock.md) que se incluyen con el kit de desarrollo de software (SDK) de Microsoft Windows se muestran ejemplos de algunas de estas técnicas de programación.

    > [!Note]  
    > En los sistemas UNIX, una técnica de programación común para los servidores era que una aplicación escuche conexiones. Cuando se aceptó una conexión, el proceso primario llamaría a la función **Fork** para crear un nuevo proceso secundario con el fin de controlar la conexión de cliente, heredando el socket del elemento primario. Esta técnica de programación no se admite en Windows, ya que la función **Fork** no se admite. Esta técnica tampoco suele ser adecuada para los servidores de alto rendimiento, ya que los recursos necesarios para crear un nuevo proceso son mucho mayores que los necesarios para un subproceso.

     

Siguiente paso: [recibir y enviar datos en el servidor](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación Winsock Server](winsock-server-application.md)
</dt> <dt>

[Escuchar en un socket](listening-on-a-socket.md)
</dt> </dl>

 

 
