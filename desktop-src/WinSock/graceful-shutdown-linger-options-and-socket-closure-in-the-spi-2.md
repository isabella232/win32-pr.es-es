---
description: Es importante distinguir entre apagar una conexión de socket y cerrar un socket.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Cierre estable, opciones de Linger y cierre de sockets en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5791732404948fe59d3f5c15c2ac46cdbba8d8327fb3dc5f794be1f070a9eeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132138"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Cierre estable, opciones de Linger y cierre de sockets en spi

Es importante distinguir entre apagar una conexión de socket y cerrar un socket. Apagar una conexión de socket implica un intercambio de mensajes de protocolo entre los dos puntos de conexión, lo que se conoce a continuación como una secuencia de apagado. Se definen dos clases generales de secuencias de apagado: estables y abortivas. En una secuencia de apagado estable, los datos que se han puesto en cola pero que aún no se han transmitido se pueden enviar antes de que se cierre la conexión. En un apagado abortivo, se pierden los datos no reenviados. La aparición de una secuencia de apagado (estable o abortiva) también se puede usar para proporcionar una indicación FD CLOSE a las aplicaciones asociadas que indican que hay un apagado \_ en curso. Por otro lado, el cierre de un socket hace que el identificador de socket se desasigne para que la aplicación ya no pueda hacer referencia ni usar el socket de ninguna manera.

En Windows Sockets, tanto la función [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) como la función [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) se pueden usar para iniciar una secuencia de apagado, mientras que la función [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) se usa para desasignar los identificadores de socket y liberar los recursos asociados. Sin embargo, surge cierta confusión por el hecho de que la función **WSPCloseSocket** provocará implícitamente que se produzca una secuencia de apagado si aún no se ha producido. De hecho, se ha convertido en una práctica de programación bastante común confiar en esta característica y usar **WSPCloseSocket para** iniciar la secuencia de cierre y desasignar el identificador de socket.

Para facilitar este uso, la interfaz de sockets proporciona controles a través del mecanismo de opción de socket que permite al programador indicar si la secuencia de apagado implícito debe ser correcta o abortiva, y también si la función debe persistir, es decir, no completarse inmediatamente) para permitir que se complete una secuencia de apagado estable.

Al establecer los valores adecuados para las opciones de socket SO LINGER y SO DONTLINGER, se pueden obtener los siguientes tipos de comportamiento con la función \_ \_ [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))

-   Secuencia de apagado abortiva, devolución inmediata [**de WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Apagado estable, retraso de la devolución hasta que se complete la secuencia de apagado o hasta que transcurra un intervalo de tiempo especificado. Si el intervalo de tiempo expira antes de que se complete la secuencia de apagado estable, se produce una secuencia de apagado abortiva y [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) devuelve .
-   Cierre estable, vuelva inmediatamente y permita que la secuencia de apagado se complete en segundo plano. Este es el comportamiento predeterminado. Sin embargo, tenga en cuenta que la aplicación no tiene ninguna manera de saber cuándo (o si) se completa la secuencia de cierre correcto.

Una técnica que se puede usar para minimizar la posibilidad de que se produzcan problemas durante el desmontaje de la conexión es no confiar en un apagado implícito iniciado por [**WSPCloseSocket.**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) En su lugar, se usa una de las dos funciones de apagado explícitas [**(WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPSendDisconnect).**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) Esto, a su vez, hará que la aplicación del mismo nivel reciba una indicación FD CLOSE que indica que se han recibido todos los datos \_ pendientes. Para ilustrar esto, en la tabla siguiente se muestran las funciones que invocarían los componentes de cliente y servidor de una aplicación, donde el cliente es responsable de iniciar un cierre correcto.

| En el cliente                                                                                                                         | En el servidor                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) Invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD SEND) para señalar el final de la sesión y ese cliente no tiene más datos \_ para enviar. |                                                                                                              |
|                                                                                                                                     | (2) Recibe FD CLOSE, lo que indica un cierre estable \_ en curso y que se han recibido todos los datos.        |
|                                                                                                                                     | (3) Envía los datos de respuesta restantes.                                                                       |
| (5') Obtiene FD \_ READ e invoca recv para obtener los datos de respuesta enviados por el servidor.                                                         | (4) Invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD SEND) para indicar que el servidor \_ no tiene más datos que enviar. |
| (5) Recibe la indicación FD \_ CLOSE.                                                                                                  | (4') Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

La secuencia de tiempo se mantiene del paso (1) al paso (6) entre el cliente y el servidor, excepto en los pasos (4') y (5') que solo tienen importancia de tiempo local en el sentido de que el paso (5) sigue el paso (5') en el lado cliente, mientras que el paso (4') sigue el paso (4) en el lado servidor, sin relación de tiempo con la entidad remota.

 

 
