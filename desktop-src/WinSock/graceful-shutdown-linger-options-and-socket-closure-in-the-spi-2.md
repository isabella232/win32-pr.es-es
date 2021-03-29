---
description: Es importante distinguir entre apagar una conexión de socket y cerrar un socket.
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: Cierre estable, opciones de permanencia y cierre de sockets en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743cae48977421c08611c79053520799420e9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541579"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>Cierre estable, opciones de permanencia y cierre de sockets en el SPI

Es importante distinguir entre apagar una conexión de socket y cerrar un socket. Cerrar una conexión de socket implica un intercambio de mensajes de protocolo entre los dos extremos, lo que se conoce en adelante como una secuencia de cierre. Se definen dos clases generales de secuencias de cierre: correcto y anulación. En una secuencia de cierre correcto, cualquier dato que se haya puesto en cola pero que todavía no se haya transmitido se puede enviar antes de que se cierre la conexión. En un cierre anulado, se pierden los datos no enviados. La aparición de una secuencia de apagado (correcta o anulación) también se puede usar para proporcionar una \_ indicación de cierre FD a las aplicaciones asociadas, lo que significa que hay un apagado en curso. Al cerrar un socket, por otro lado, el controlador de socket se desasigna para que la aplicación ya no pueda hacer referencia o usar el socket de ninguna manera.

En Windows Sockets, la función [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) y la función [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) se pueden usar para iniciar una secuencia de apagado, mientras que la función [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) se usa para desasignar identificadores de socket y liberar los recursos asociados. Sin embargo, se produce cierto número de confusión, desde el hecho de que la función **WSPCloseSocket** provocará implícitamente que se produzca una secuencia de cierre si aún no se ha producido. De hecho, se ha convertido en una práctica de programación bastante común que se basa en esta característica y se usa **WSPCloseSocket** para iniciar la secuencia de apagado y desasignar el identificador de socket.

Para facilitar este uso, la interfaz de sockets proporciona controles a través del mecanismo de opción de socket que permite al programador indicar si la secuencia de apagado implícita debe ser correcta o anulada, y también si la función debe ser persistente, no completada inmediatamente, para dejar tiempo para que se complete una secuencia de cierre correcto.

Mediante el establecimiento de los valores adecuados para las opciones de socket, por lo tanto \_ \_ , DONTLINGER, se pueden obtener los siguientes tipos de comportamiento con la función [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) .

-   Secuencia de apagado anulada, devolución inmediata desde [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)).
-   Cierre estable, retrasar la devolución hasta que finalice la secuencia de cierre o transcurra un intervalo de tiempo especificado. Si el intervalo de tiempo expira antes de que se complete la secuencia de cierre correcto, se produce una secuencia de apagado anulado y [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) devuelve.
-   Cierre estable, vuelva inmediatamente y permita que la secuencia de apagado se complete en segundo plano. Este es el comportamiento predeterminado. Tenga en cuenta, sin embargo, que la aplicación no tiene ninguna manera de saber cuándo se completa la secuencia de cierre correcto.

Una técnica que se puede usar para minimizar la posibilidad de que se produzcan problemas durante la destrucción de la conexión no depende de que [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))inicie un cierre implícito. En su lugar, se usa una de las dos funciones de cierre explícitas ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))). Esto, a su vez, provocará que \_ la aplicación del mismo nivel reciba una indicación de cierre FD que indica que se han recibido todos los datos pendientes. Para ilustrar esto, en la tabla siguiente se muestran las funciones que invocarían los componentes de cliente y servidor de una aplicación, donde el cliente es responsable de iniciar un cierre estable.

| En el cliente                                                                                                                         | En el servidor                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| (1) invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*, SD \_ send) para señalar el final de la sesión y ese cliente no tiene más datos para enviar. |                                                                                                              |
|                                                                                                                                     | (2) recibe FD \_ Close, lo que indica un cierre correcto en curso y que se han recibido todos los datos.        |
|                                                                                                                                     | (3) envía los datos de respuesta restantes.                                                                       |
| (5 ') obtiene FD \_ Read e Invoke RECV para obtener los datos de respuesta enviados por el servidor.                                                         | (4) invoca [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))(*s*, SD \_ send) para indicar que el servidor no tiene más datos para enviar. |
| (5) recibe la \_ indicación FD de cierre.                                                                                                  | (4 ') invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
| (6) invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

La secuencia de tiempo se mantiene del paso (1) al paso (6) entre el cliente y el servidor. excepto en el caso de los pasos (4 ') y (5 '), que solo tienen una importancia en el tiempo local en el sentido de que el paso (5) sigue al paso (5 ') en el lado cliente mientras el paso (4 ') sigue el paso (4) en el lado servidor, sin relación de tiempo con la parte remota.

 

 
