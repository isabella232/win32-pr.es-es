---
description: El envío y la recepción de datos PGM es similar al envío o la recepción de datos en cualquier socket. Hay consideraciones específicas para PGM, que se describen en los párrafos siguientes.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Envío y recepción de datos PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156013"
---
# <a name="sending-and-receiving-pgm-data"></a>Envío y recepción de datos PGM

El envío y la recepción de datos PGM es similar al envío o la recepción de datos en cualquier socket. Hay consideraciones específicas para PGM, que se describen en los párrafos siguientes.

## <a name="sending-pgm-data"></a>Envío de datos PGM

Una vez que se crea una sesión de remitente PGM, los datos se envían mediante las distintas funciones de envío de Windows Sockets: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Como los identificadores de Windows Sockets son identificadores del sistema de archivos, otras funciones como las funciones [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) y CRT también pueden transmitir datos. En el fragmento de código siguiente se muestra una operación de remitente PGM:


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



Cuando se usa el modo de mensaje (SOCK \_ RDM), cada llamada a una función Send da como resultado un mensaje discreto, que a veces no es deseable; una aplicación puede querer enviar un mensaje de 2 megabytes con varias llamadas a [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send). En tales circunstancias, el remitente puede establecer la opción [RM \_ set \_ Message \_ BOUNDARY](socket-options.md) socket para indicar el tamaño del mensaje que se indica a continuación.

Si la ventana de envío está llena, no se aceptará un nuevo envío desde la aplicación hasta que se haya avanzado la ventana. Se produce un error al intentar enviar un socket que no es de bloqueo con WSAEWOULDBLOCK; un socket de bloqueo simplemente se bloquea hasta que la ventana avanza hasta el punto en el que los datos solicitados se pueden almacenar en búfer y enviar. En e/s superpuestas, la operación no se completa hasta que la ventana avanza lo suficiente para alojar los datos nuevos.

## <a name="receiving-pgm-data"></a>Recibir datos PGM

Una vez creada la sesión del receptor PGM, se reciben los datos mediante las distintas funciones de recepción de Windows Sockets: [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)y [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). Como los identificadores de Windows Sockets también son identificadores de archivo, las funciones [**readfile**](/windows/win32/api/fileapi/nf-fileapi-readfile) y CRT también se pueden usar para recibir datos de sesión PGM. El transporte reenvía los datos al receptor a medida que llegan, siempre y cuando los datos estén en secuencia. El transporte garantiza que los datos devueltos son contiguos y están libres de duplicados. En el fragmento de código siguiente se muestra una operación de recepción PGM:


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



Al usar el modo de mensaje (SOCK \_ RDM), el transporte indica cuándo se recibe un mensaje parcial, bien con el error WSAEMSGSIZE, o bien estableciendo la \_ marca parcial MSG al volver de las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) y [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) . Cuando el último fragmento del mensaje completo se devuelve al cliente, no se indica el error o la marca.

Cuando la sesión finaliza correctamente, se produce un error en la operación de recepción con WSAEDISCON. Cuando se produce la pérdida de datos en el transporte, PGM almacena temporalmente en búfer los paquetes fuera de secuencia e intenta recuperar los datos perdidos. Si la pérdida de datos es irrecuperable, se produce un error en la operación de recepción con WSAECONNRESET y se termina la sesión. La sesión se puede restablecer debido a diversas condiciones, entre las que se incluyen las siguientes:

-   El receptor o la velocidad de conexión entrante es demasiado lento para mantenerse al ritmo de la velocidad de datos de entrada.
-   Se produce una pérdida de datos excesiva, posiblemente debido a condiciones de red transitorias, como problemas de enrutamiento, inestabilidad de red, etc.
-   Se produce un error irrecuperable en el remitente.
-   Se produce un uso excesivo de los recursos en el equipo local, por ejemplo, si se supera el almacenamiento de búfer interno máximo permitido o si se encuentra una condición de recursos insuficientes.
-   Se produce un error de comprobación de coherencia de datos.
-   Un error en un componente PGM depende de, como TCP/IP o Windows Sockets.

Tanto el primer como el segundo elemento de la lista anterior pueden dar lugar a que el receptor realice un almacenamiento en búfer excesivo antes de quedarse sin recursos o antes de moverse más allá de la ventana del remitente.

## <a name="terminating-a-pgm-session"></a>Finalizar una sesión PGM

El remitente o receptor PGM puede detener el envío o la recepción de datos llamando a [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). El receptor debe llamar a **closesocket** en los sockets de escucha y recepción para evitar pérdidas de identificadores. Llamar a [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) en el remitente antes de llamar a **closesocket** garantiza que se envíen todos los datos y garantiza que los datos de reparación se mantengan hasta que la ventana de envío avance más allá de la última secuencia de datos, incluso si la propia aplicación finaliza.

 

 
