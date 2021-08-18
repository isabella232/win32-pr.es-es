---
description: El envío y recepción de datos PGM es similar al envío o recepción de datos en cualquier socket. Hay consideraciones específicas de PGM, que se describen en los párrafos siguientes.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Envío y recepción de datos PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 130b38ea52e5d0679b988e55f8292b9752a4bf15d0514a8277a2e0b3b2327001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740576"
---
# <a name="sending-and-receiving-pgm-data"></a>Envío y recepción de datos PGM

El envío y recepción de datos PGM es similar al envío o recepción de datos en cualquier socket. Hay consideraciones específicas de PGM, que se describen en los párrafos siguientes.

## <a name="sending-pgm-data"></a>Envío de datos PGM

Una vez creada una sesión de remitente PGM, los datos se envían mediante las distintas funciones de envío de sockets de Windows: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)y [**WSASendTo.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) Dado Windows sockets son identificadores del sistema de archivos, otras funciones como [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) y funciones CRT también pueden transmitir datos. El fragmento de código siguiente muestra una operación de remitente PGM:


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



Cuando se usa el modo de mensaje (SOCK RDM), cada llamada a una función de envío genera un mensaje discreto, que a veces no es deseable; es posible que una aplicación quiera enviar un mensaje de 2 megabytes con varias llamadas para \_ [**enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send). En tales circunstancias, el remitente puede establecer la opción de socket [RM \_ SET MESSAGE \_ \_ BOUNDARY](socket-options.md) para indicar el tamaño del mensaje siguiente.

Si la ventana de envío está llena, no se acepta un nuevo envío desde la aplicación hasta que se haya avanzado la ventana. Se produce un error al intentar enviar en un socket sin bloqueo con WSAEWOULDBLOCK; un socket de bloqueo simplemente se bloquea hasta que la ventana avanza hasta el punto donde se pueden almacenar en búfer y enviar los datos solicitados. En la E/S superpuesta, la operación no se completa hasta que la ventana avanza lo suficiente como para dar cabida a los nuevos datos.

## <a name="receiving-pgm-data"></a>Recepción de datos PGM

Una vez creada una sesión de receptor PGM, los datos se reciben mediante las distintas funciones de recepción de sockets de Windows: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv y**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Dado Windows identificadores de sockets de archivos también son identificadores de archivo, las funciones [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) y CRT también se pueden usar para recibir datos de sesión PGM. El transporte reenvía los datos hasta el receptor a medida que llegan mientras los datos están en secuencia. El transporte garantiza que los datos devueltos son contiguos y no tienen duplicados. El siguiente fragmento de código muestra una operación de recepción PGM:


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



Cuando se usa el modo de mensaje (SOCK RDM), el transporte indica cuándo se recibe un mensaje parcial, ya sea con el error WSAEMSGSIZE o estableciendo la marca MSG PARTIAL al devolverse de las funciones \_ \_ [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) y [**WSARecvFrom.**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) Cuando se devuelve el último fragmento del mensaje completo al cliente, no se indica el error o la marca.

Cuando la sesión finaliza correctamente, se produce un error en la operación de recepción con WSAEDISCON. Cuando se produce una pérdida de datos en el transporte, PGM almacena temporalmente en búfer los paquetes fuera de secuencia e intenta recuperar los datos perdidos. Si la pérdida de datos es irrecuperable, se producirá un error en la operación de recepción con WSAECONNRESET y se finalizará la sesión. La sesión se puede restablecer debido a una serie de condiciones, incluidas las siguientes:

-   El receptor o la velocidad de conexión entrante son demasiado lentos para mantener el ritmo de la velocidad de datos entrantes.
-   Se produce una pérdida excesiva de datos, posiblemente debido a condiciones de red transitorias, como problemas de enrutamiento, inestabilidad de red, etc.
-   Se produce un error irrecuperable en el remitente.
-   El uso excesivo de recursos se produce en el equipo local, como superar el almacenamiento de búfer interno máximo permitido o encontrar una condición de falta de recursos.
-   Se produce un error de comprobación de coherencia de datos.
-   El error en un componente PGM depende de, por ejemplo, TCP/IP o Windows sockets.

Tanto el primer como el segundo elemento de la lista anterior podrían dar lugar a que el receptor realizara un almacenamiento en búfer excesivo antes de que se quedándose sin recursos, o antes de ir más allá de la ventana del remitente.

## <a name="terminating-a-pgm-session"></a>Terminación de una sesión de PGM

El remitente o receptor de PGM puede dejar de enviar o recibir datos mediante una llamada [**a closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). El receptor debe llamar **a closesocket en** los sockets de escucha y recepción para evitar pérdidas de control. Al [](/windows/desktop/api/winsock/nf-winsock-shutdown) llamar a shutdown en el remitente antes de llamar **a closesocket,** se garantiza el envío de todos los datos y se garantiza que los datos de reparación se mantienen hasta que la ventana de envío avanza más allá de la última secuencia de datos, incluso si la propia aplicación finaliza.

 

 
