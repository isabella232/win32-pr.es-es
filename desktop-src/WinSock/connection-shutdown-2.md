---
description: A continuación se describe el incidente de operaciones para cerrar una conexión de socket establecida.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Cierre de la conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbde0cfe4c3a97435c2412d28970107f830308fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907956"
---
# <a name="connection-shutdown"></a>Cierre de la conexión

A continuación se describe el incidente de operaciones para cerrar una conexión de socket establecida.

## <a name="initiating-shutdown-sequence"></a>Iniciando secuencia de apagado

Una conexión de socket se puede desconectar de una de varias maneras. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (con *el mismo modo* que SD \_ send o SD \_ ) y [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) se puede usar para iniciar un cierre de conexión correcto. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) se puede usar para iniciar un apagado correcto o anulado, en función de las opciones de permanencia invocadas por el cierre de un socket. Vea a continuación para obtener más información acerca de los apagados correctos y anulados y las opciones de permanencia.

## <a name="indicating-remote-shutdown"></a>Indica apagado remoto

Los proveedores de servicios indican la destrucción de la conexión iniciada por la parte remota a través del \_ evento FD Close Network. El cierre estable también se indica a través de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) cuando el número de bytes leídos es 0 para los protocolos de secuencia de bytes o a través de un código de error devuelto de WSAEDISCON para los protocolos orientados a mensajes. En cualquier caso, un **WSPRecv** de error devuelto de WSAECONNRESET indica un cierre anulado.

## <a name="exchanging-user-data-at-shutdown-time"></a>Intercambio de datos de usuario en tiempo de apagado

En el momento de la destrucción de la conexión, también es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los extremos. El extremo que inicia el desmontaje puede llamar a [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para indicar que no se van a enviar más datos y que se inicie la secuencia de destrucción de la conexión. Para determinados protocolos, parte de esta secuencia de desmontaje es la entrega de datos de desconexión del iniciador de desmontaje. Después de recibir el aviso de que el extremo remoto ha iniciado la secuencia de desmontaje (normalmente mediante la indicación FD de \_ cierre), se puede llamar a la función [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para recibir los datos de desconexión (si los hubiera).

Para ilustrar cómo se pueden usar los datos de desconexión, considere el siguiente escenario. La mitad del cliente de una aplicación cliente/servidor es responsable de finalizar una conexión de socket. Coincidentes con la terminación que proporciona (a través de los datos de desconexión) el número total de transacciones que ha procesado con el servidor. A su vez, el servidor responde con el total general acumulado de transacciones que ha procesado con todos los clientes. La secuencia de llamadas e indicaciones podría producirse tal como se muestra en la tabla siguiente.

| En el cliente                                                                                                               | En el servidor                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) invoca [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para concluir la sesión y proporcionar el total de la transacción.            |                                                                                                                                         |
|                                                                                                                           | (2) obtiene FD \_ Close o [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con un valor devuelto de cero o WSAEDISCON que indica un cierre correcto en curso. |
|                                                                                                                           | (3) invoca [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para obtener el total de la transacción del cliente.                                         |
|                                                                                                                           | (4) calcula el total general acumulado de todas las transacciones.                                                                                |
|                                                                                                                           | (5) invoca [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para transmitir el total general.                                                   |
| (6) recibe la \_ indicación FD de cierre.                                                                                        | (5 ') invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) invoca [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para recibir y almacenar el total general acumulativo de transacciones. |                                                                                                                                         |
|                                                                                                                           | (8) invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

El paso (5 ') debe seguir el paso (5), pero no tiene ninguna relación de tiempo con los pasos (6), (7) o (8).

 

 
