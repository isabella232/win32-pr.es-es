---
description: A continuación se describe el incidente de operaciones para apagar una conexión de socket establecida.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Cierre de la conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbd26716c255c83a8ecc17305d9e59676645739a6f90d18ac72b5bcda49241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898425"
---
# <a name="connection-shutdown"></a>Cierre de la conexión

A continuación se describe el incidente de operaciones para apagar una conexión de socket establecida.

## <a name="initiating-shutdown-sequence"></a>Iniciar la secuencia de apagado

Una conexión de socket se puede descargar de una de varias maneras. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (con el mismo valor que SD SEND o SD BOTH) y  \_ \_ [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) se pueden usar para iniciar un cierre de conexión estable. [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) se puede usar para iniciar un cierre estable o abortivo, en función de las opciones de persistente invocadas por el cierre de un socket. Consulte a continuación para obtener más información sobre los apagados estables y abortivos, y las opciones de persistente.

## <a name="indicating-remote-shutdown"></a>Indicando el apagado remoto

Los proveedores de servicios indican la desmontaje de la conexión iniciada por la parte remota a través del evento de red FD \_ CLOSE. El cierre estable también se indica a través de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) cuando el número de bytes leídos es 0 para los protocolos de secuencia de bytes o a través de un código de error devuelto de WSAEDISCON para protocolos orientados a mensajes. En cualquier caso, un código de error de retorno **WSPRecv** de WSAECONNRESET indica un apagado abortivo.

## <a name="exchanging-user-data-at-shutdown-time"></a>Intercambio de datos de usuario en tiempo de apagado

En el momento de la desmontaje de la conexión, también es posible (para los protocolos que lo admiten) intercambiar datos de usuario entre los puntos de conexión. El final que inicia la desmontaje puede llamar a [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para indicar que no se enviarán más datos y provocar que se inicie la secuencia de desmontaje de la conexión. Para determinados protocolos, parte de esta secuencia de desmontaje es la entrega de datos de desconexión del iniciador de la desmontaje. Después de recibir el aviso de que el extremo remoto ha iniciado la secuencia de desmontaje (normalmente a través de la indicación FD CLOSE), se puede llamar a la función \_ [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para recibir los datos de desconexión (si existen).

Para ilustrar cómo se pueden usar los datos de desconexión, considere el siguiente escenario. La mitad del cliente de una aplicación cliente/servidor es responsable de finalizar una conexión de socket. Coincidencia con la terminación que proporciona (a través de datos de desconexión) el número total de transacciones que procesó con el servidor. A su vez, el servidor responde con el total general acumulado de transacciones que ha procesado con todos los clientes. La secuencia de llamadas e indicaciones puede producirse como se muestra en la tabla siguiente.

| En el cliente                                                                                                               | En el servidor                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) Invoca [**WSPSendDisconnect para**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) finalizar la sesión y proporcionar el total de transacciones.            |                                                                                                                                         |
|                                                                                                                           | (2) Obtiene FD CLOSE o WSPRecv con un valor devuelto de cero o \_ WSAEDISCON que indica un cierre correcto en curso. [](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) |
|                                                                                                                           | (3) Invoca [**WSPRecvDisconnect para**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) obtener el total de transacciones del cliente.                                         |
|                                                                                                                           | (4) Calcula el total acumulado general de todas las transacciones.                                                                                |
|                                                                                                                           | (5) Invoca [**WSPSendDisconnect para**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) transmitir el total general.                                                   |
| (6) Recibe la indicación FD \_ CLOSE.                                                                                        | (5') Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) Invoca [**WSPRecvDisconnect para**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) recibir y almacenar el total acumulado de transacciones. |                                                                                                                                         |
|                                                                                                                           | (8) Invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

El paso (5") debe seguir el paso (5), pero no tiene ninguna relación de tiempo con los pasos (6), (7) o (8).

 

 
