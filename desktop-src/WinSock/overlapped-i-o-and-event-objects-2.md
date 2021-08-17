---
description: Windows Sockets 2 admite E/S superpuesta y todos los proveedores de transporte admiten esta funcionalidad.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Objetos de E/S y eventos superpuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ae2ee17036275183518bfd444b9317bcdc05145a9fcb327ad48388618a66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741062"
---
# <a name="overlapped-io-and-event-objects"></a>Objetos de E/S y eventos superpuestos

Windows Sockets 2 admite E/S superpuesta y todos los proveedores de transporte admiten esta funcionalidad. La E/S superpuesta sigue el modelo establecido en Windows y se puede realizar en sockets creados con la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o sockets creados con la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la marca **\_ \_ OVERLAPPED de WSA FLAG** establecida en el parámetro *dwFlags.*

> [!Note]  
> La creación de un socket con el atributo superpuesto no afecta a si un socket está actualmente en modo de bloqueo o de no bloqueo. Los sockets creados con el atributo superpuesto se pueden usar para realizar operaciones de E/S superpuestas, lo que no cambia el modo de bloqueo de un socket. Puesto que las operaciones de E/S superpuestas no se bloquean, el modo de bloqueo de un socket es irrelevante para estas operaciones.

 

Para recibir, las aplicaciones usan las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) para proporcionar búferes en los que se recibirán los datos. Si uno o varios búferes se publican antes del momento en que la red ha recibido los datos, los datos podrían colocarse en los búferes del usuario inmediatamente a medida que llegan. Por lo tanto, puede evitar la operación de copia que, de lo contrario, se produciría en el momento en que se invoca la función [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) o [**recvfrom.**](/windows/desktop/api/winsock/nf-winsock-recvfrom) Si los datos ya están presentes cuando se publican búferes de recepción, se copian inmediatamente en los búferes del usuario.

Si llegan datos cuando la aplicación no ha publicado búferes de recepción, la red pasa al conocido estilo sincrónico de operación. Es decir, los datos entrantes se almacenan en búfer internamente hasta que la aplicación emite una llamada de recepción y, por tanto, proporciona un búfer en el que se pueden copiar los datos. Una excepción a esto es cuando la aplicación usa [**setsockopt para**](/windows/desktop/api/winsock/nf-winsock-setsockopt) establecer el tamaño del búfer de recepción en cero. En este caso, los protocolos confiables solo permitirían recibir datos cuando se publicaran búferes de aplicación y se perdiera información sobre protocolos no confiables.

En el lado de envío, las aplicaciones usan [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) para proporcionar punteros a búferes rellenos y, a continuación, aceptan no alterar los búferes de ninguna manera hasta que la red haya consumido el contenido del búfer.

Las llamadas de envío y recepción superpuestas se devuelven inmediatamente. Un valor devuelto de cero indica que la operación de E/S se completó inmediatamente y que ya se ha producido la indicación de finalización correspondiente. Es decir, se ha señalado el objeto de evento asociado o se ha puesto en cola una rutina de finalización y se ejecutará cuando el subproceso que realiza la llamada llegue al estado de espera que se puede alertar.

Un valor devuelto de SOCKET ERROR junto con un código de error de \_ [WSA \_ IO \_ PENDING](windows-sockets-error-codes-2.md) indica que la operación superpuesta se ha iniciado correctamente y que se proporciona una indicación posterior cuando se han consumido los búferes de envío o cuando se ha completado una operación de recepción. Sin embargo, para los sockets que tienen un estilo de secuencia de bytes, la indicación de finalización se produce cada vez que se agotan los datos entrantes, independientemente de si los búferes están llenos. Cualquier otro código de error indica que la operación superpuesta no se inició correctamente y que no habrá ninguna indicación de finalización próxima.

Las operaciones de envío y recepción se pueden superponer. Las funciones de recepción se pueden invocar varias veces para publicar búferes de recepción como preparación para los datos entrantes, y las funciones de envío se pueden invocar varias veces para poner en cola varios búferes que se enviarán. Aunque la aplicación puede basarse en una serie de búferes de envío superpuestos que se envían en el orden proporcionado, las indicaciones de finalización correspondientes pueden producirse en un orden diferente. Del mismo modo, en el lado receptor, los búferes se pueden rellenar en el orden en que se proporcionan, pero las indicaciones de finalización pueden producirse en un orden diferente.

En muchos casos, las operaciones de Winsock superpuestas mediante [**AcceptEx,**](/windows/win32/api/mswsock/nf-mswsock-acceptex) [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)y funciones similares se pueden cancelar. Sin embargo, el comportamiento no está definido para el uso continuado de un socket que ha cancelado las operaciones pendientes. Se [**debe llamar a la función closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) después de cancelar una operación superpuesta. Por lo tanto, para obtener mejores resultados, en lugar de cancelar la E/S directamente, se debe llamar a la función **closesocket** para cerrar el socket, lo que finalmente interrumpirá todas las operaciones pendientes.

La característica de finalización diferida de E/S superpuesta también está disponible para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), que es una versión mejorada de [**ioctlsocket.**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

 

 
