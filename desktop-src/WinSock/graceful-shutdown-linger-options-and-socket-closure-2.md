---
description: El siguiente material se proporciona como aclaración para el asunto de apagar las conexiones de socket que cierran los sockets. Es importante distinguir la diferencia entre apagar una conexión de socket y cerrar un socket.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Cierre estable, opciones de Linger y cierre de sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063979"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Cierre estable, opciones de Linger y cierre de sockets

El siguiente material se proporciona como aclaración para el asunto de apagar las conexiones de socket que cierran los sockets. Es importante distinguir la diferencia entre apagar una conexión de socket y cerrar un socket.

Apagar una conexión de socket implica un intercambio de mensajes de protocolo entre los dos puntos de conexión, lo que en adelante se conoce como una secuencia de apagado. Se definen dos clases generales de secuencias de apagado: estables y abortivas (también denominadas duras). En una secuencia de cierre estable, los datos que se han puesto en cola, pero que aún no se han transmitido, se pueden enviar antes de cerrar la conexión. En un apagado abortivo, se pierden los datos no reenviados. La aparición de una secuencia de apagado (estable o abortiva) también se puede usar para proporcionar una indicación FD CLOSE a las aplicaciones asociadas que indican que hay un apagado \_ en curso.

Por otro lado, el cierre de un socket hace que el identificador de socket se desasigne para que la aplicación ya no pueda hacer referencia al socket ni usarlo de ninguna manera.

En Windows Sockets, tanto la función [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) como la función [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) se pueden usar para iniciar una secuencia de apagado, mientras que la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) se usa para desasignar los identificadores de socket y liberar los recursos asociados. Sin embargo, se produce cierta confusión a partir del hecho de que la función **closesocket** provoca implícitamente que se produzca una secuencia de apagado si aún no se ha producido. De hecho, se ha convertido en una práctica de programación bastante común confiar en esta característica y usar **closesocket** para iniciar la secuencia de apagado y desasignar el identificador del socket.

Para facilitar este uso, la interfaz de sockets proporciona controles a través del mecanismo de opción de socket que permiten al programador indicar si la secuencia de apagado implícito debe ser correcta o abortiva, y también si la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) debe persistir (que no se completa inmediatamente) para permitir que se complete una secuencia de cierre estable. Estas diferencias importantes y las ramificaciones de usar **closesocket** de esta manera todavía no se comprenden ampliamente.

Al establecer los valores adecuados para las opciones de socket SO LINGER y SO DONTLINGER, se pueden obtener los siguientes tipos de comportamiento con la \_ \_ función [**closesocket:**](/windows/desktop/api/winsock/nf-winsock-closesocket)

-   Secuencia de apagado abortiva, devolución inmediata de [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Cierre estable, retrasando la devolución hasta que se complete la secuencia de apagado o hasta que transcurra un intervalo de tiempo especificado. Si el intervalo de tiempo expira antes de que se complete la secuencia de cierre estable, se produce una secuencia de apagado abortiva y [**se devuelve closesocket.**](/windows/desktop/api/winsock/nf-winsock-closesocket)
-   Cierre estable, devolución inmediata, lo que permite que la secuencia de apagado se complete en segundo plano. Aunque este es el comportamiento predeterminado, la aplicación no tiene forma de saber cuándo (o si) se completa realmente la secuencia de cierre estable.

El uso de las opciones de socket SO LINGER y SO DONTLINGER y la estructura de linger asociada se describe con más detalle en las secciones de referencia sobre las opciones de socket DE SOL y la estructura \_ \_ de **linger.** [**\_**](sol-socket-socket-options.md) [](/windows/desktop/api/winsock/ns-winsock-linger)

Una técnica que se puede usar para minimizar la posibilidad de que se produzcan problemas durante el desmontaje de la conexión es evitar confiar en que closesocket inicie un cierre [**implícito.**](/windows/desktop/api/winsock/nf-winsock-closesocket) En su lugar, use una de las dos funciones de apagado [**explícitas, shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Esto, a su vez, hace que la aplicación del mismo nivel reciba una indicación FD CLOSE que indica que se han recibido todos los \_ datos pendientes. Para ilustrar esto, en la tabla siguiente se muestran las funciones que invocarían los componentes de cliente y servidor de una aplicación, donde el cliente es responsable de iniciar un cierre estable.

| En el cliente                                                                                                                | En el servidor                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) Invoca [**el**](/windows/desktop/api/winsock/nf-winsock-shutdown)apagado (s, SD SEND) para indicar el final de la sesión y ese cliente no tiene más \_ datos que enviar. |                                                                                                       |
|                                                                                                                            | (2) Recibe FD CLOSE, lo que indica un cierre correcto en curso y que se han recibido todos \_ los datos. |
|                                                                                                                            | (3) Envía los datos de respuesta restantes.                                                                |
| (solo importancia de tiempo local) Obtiene FD \_ READ y llama a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) para obtener los datos de respuesta enviados por el servidor .  | (4) Invoca el [**apagado**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD SEND) para indicar que el \_ servidor no tiene más datos que enviar.  |
| (5) Recibe la indicación FD \_ CLOSE.                                                                                         | (solo importancia de tiempo local) Invoca [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .                       |
| (6) Invoca [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                          |                                                                                                       |



 

 

 



