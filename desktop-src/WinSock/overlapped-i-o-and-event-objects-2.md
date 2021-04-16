---
description: Windows Sockets 2 es compatible con e/s superpuestas y todos los proveedores de transporte admiten esta funcionalidad.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Objetos de eventos e/s superpuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705601"
---
# <a name="overlapped-io-and-event-objects"></a>Objetos de eventos e/s superpuestos

Windows Sockets 2 es compatible con e/s superpuestas y todos los proveedores de transporte admiten esta funcionalidad. La e/s superpuesta sigue el modelo establecido en Windows y se puede realizar en sockets creados con la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o sockets creados con la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la marca **\_ \_ OVERLAPPED de marca WSA** establecida en el parámetro *dwFlags* .

> [!Note]  
> La creación de un socket con el atributo OVERLAPPED no tiene ningún efecto sobre si un socket está actualmente en modo de bloqueo o de no bloqueo. Los sockets creados con el atributo OVERLAPPED se pueden usar para realizar operaciones de e/s superpuestas; al hacerlo, no se cambia el modo de bloqueo de un socket. Dado que las operaciones de e/s superpuestas no se bloquean, el modo de bloqueo de un socket es irrelevante para estas operaciones.

 

En el caso de la recepción, las aplicaciones usan las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) para proporcionar búferes en los que se van a recibir los datos. Si se publican uno o más búferes antes del momento en que la red ha recibido los datos, los datos se pueden colocar en los búferes del usuario inmediatamente a medida que llegan. Por lo tanto, puede evitar la operación de copia que, de lo contrario, se produciría en el momento en que se invoca la función [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) o [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) . Si los datos ya están presentes cuando se publican los búferes de recepción, se copian inmediatamente en los búferes del usuario.

Si los datos llegan cuando la aplicación no ha publicado ningún búfer de recepción, la red recurre al conocido estilo sincrónico de funcionamiento. Es decir, los datos entrantes se almacenan en búfer internamente hasta que la aplicación emite una llamada de recepción y, por tanto, proporciona un búfer en el que se pueden copiar los datos. Una excepción a esto es cuando la aplicación usa el valor de My para establecer el tamaño del búfer de [**recepción en cero**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . En esta instancia, los protocolos confiables solo permitirán que se reciban los datos cuando se publicaron los búferes de la aplicación y los datos de protocolos no confiables se perderían.

En el lado de envío, las aplicaciones usan [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) para proporcionar punteros a búferes rellenos y, después, acuerdan no molestar los búferes de ningún modo hasta que la red haya consumido el contenido del búfer.

Las llamadas de envío y recepción superpuestas se devuelven inmediatamente. Un valor devuelto de cero indica que la operación de e/s se completó inmediatamente y que ya se ha producido la indicación de finalización correspondiente. Es decir, se ha señalado el objeto de evento asociado, o una rutina de finalización se ha puesto en cola y se ejecutará cuando el subproceso de llamada entre en el estado de espera de alerta.

Un valor devuelto de \_ error de socket junto con un código de error de la [ \_ e/s de WSA \_ pendiente](windows-sockets-error-codes-2.md) indica que la operación superpuesta se ha iniciado correctamente y que se proporcionará una indicación posterior cuando se hayan consumido los búferes de envío o cuando se haya completado una operación de recepción. Sin embargo, para los sockets que son de estilo de secuencia de bytes, la indicación de finalización se produce cada vez que se agotan los datos entrantes, independientemente de si los búferes están llenos. Cualquier otro código de error indica que la operación superpuesta no se ha iniciado correctamente y que no habrá ninguna indicación de finalización próxima.

Las operaciones de envío y recepción se pueden superponer. Las funciones Receive se pueden invocar varias veces para publicar búferes de recepción como preparación para los datos entrantes, y las funciones send se pueden invocar varias veces para poner en cola varios búferes que se van a enviar. Aunque la aplicación puede basarse en una serie de búferes de envío superpuestos que se envían en el orden proporcionado, se pueden producir las indicaciones de finalización correspondientes en un orden diferente. Del mismo modo, en el lado receptor, los búferes se pueden rellenar en el orden en que se proporcionan, pero las indicaciones de finalización pueden aparecer en un orden diferente.

En muchos casos, las operaciones superpuestas de Winsock con las funciones [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)y similares se pueden cancelar. Sin embargo, el comportamiento no está definido para el uso continuado de un socket que ha cancelado las operaciones pendientes. Se debe llamar a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) después de cancelar una operación superpuesta. Por lo tanto, para obtener los mejores resultados, en lugar de cancelar la e/s directamente, se debe llamar a la función **closesocket** para cerrar el socket que finalmente interrumpirá todas las operaciones pendientes.

La característica de finalización diferida de e/s superpuesta también está disponible para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), que es una versión mejorada de [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
