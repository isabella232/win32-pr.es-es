---
description: 'Hay varias opciones disponibles para recibir indicaciones de finalización, lo que proporciona a las aplicaciones los niveles adecuados de flexibilidad. Estos incluyen: espera (o bloqueo) en objetos de evento, objetos de evento de sondeo y rutinas de finalización de E/S de socket.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Recepción de indicaciones de finalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0ea3d46707eb31d803362f327c309d3c9d948812c0eb3a810e31b896e895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569255"
---
# <a name="receiving-completion-indications"></a>Recepción de indicaciones de finalización

Hay varias opciones disponibles para recibir indicaciones de finalización, lo que proporciona a las aplicaciones los niveles adecuados de flexibilidad. Estos incluyen: espera (o bloqueo) en objetos de evento, objetos de evento de sondeo y rutinas de finalización de E/S de socket.

## <a name="blocking-and-waiting-for-completion-indication"></a>Indicación de bloqueo y espera de finalización

Las aplicaciones pueden bloquearse mientras esperan a que uno o varios objetos de evento se establezcan mediante la [**función WSAWaitForMultipleEvents.**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) En Windows implementaciones, el proceso o subproceso se bloquea realmente. Puesto Windows los objetos de evento sockets 2 se implementan como eventos Windows, la función Windows nativa [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) también se puede usar para este propósito. Esto es especialmente útil si el subproceso debe esperar en eventos de socket y nonsocket.

## <a name="polling-for-completion-indication"></a>Sondeo para indicación de finalización

Las aplicaciones que prefieren no bloquear pueden usar la función [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para sondear el estado de finalización asociado a cualquier objeto de evento determinado. Esta función indica si se ha completado o no la operación superpuesta y, si se ha completado, se organiza para que la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) recupere el estado de error de la operación superpuesta.

## <a name="using-socket-io-completion-routines"></a>Uso de rutinas de finalización de E/S de socket

Las funciones usadas para iniciar E/S superpuestas ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) toman *lpCompletionRoutine como* parámetro de entrada opcional. Se trata de un puntero a una función específica de la aplicación a la que se llama después de que se complete correctamente una operación de E/S superpuesta iniciada correctamente (correctamente o de otro modo). La rutina de finalización sigue las mismas reglas que se han establecido para las Windows de finalización de E/S de archivos. Es decir, la rutina de finalización no se invoca hasta que el subproceso se encuentra en un estado de espera que se puede alertar, como cuando se invoca la función [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) con la marca `fAlertable` establecida. Una aplicación que usa la opción de rutina de finalización para una solicitud de E/S superpuesta determinada puede no usar la opción de espera [**de WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para esa misma solicitud de E/S superpuesta.

Los transportes permiten a una aplicación invocar operaciones de envío y recepción desde dentro del contexto de la rutina de finalización de E/S de socket y garantizan que, para un socket determinado, las rutinas de finalización de E/S no se anidarán. Esto permite que las transmisiones de datos sensibles al tiempo se produzcan completamente dentro de un contexto preferente.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Resumen de los mecanismos de indicación de finalización superpuesta

La indicación de finalización de E/S superpuesta concreta que se va a usar para una operación superpuesta determinada viene determinada por si la aplicación proporciona un puntero a una función de finalización, si se hace referencia a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) y por el valor del **miembro hEvent** dentro de la estructura **WSAOVERLAPPED** (si se proporciona). En la tabla siguiente se resume la semántica de finalización de un socket superpuesto y se muestran las distintas combinaciones de *lpOverlapped*, **hEvent** y *lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Indicación de finalización                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | No aplicable | Omitido               | La operación se completa sincrónicamente. Se comporta como si fuera un socket no cubierto.                                                                                                                                      |
| ! Null          | NULL           | NULL                  | La operación se completa superpuesta, pero no hay ningún Windows de finalización compatible con Sockets 2. El mecanismo de puerto de finalización (si se admite) se puede usar en este caso. De lo contrario, no hay ninguna notificación de finalización. |
| ! Null          | ! Null          | NULL                  | La operación se completa superpuesta y se envía una notificación mediante la señalización del objeto de evento.                                                                                                                                                  |
| ! Null          | Omitido        | ! Null                 | La operación se completa superpuesta y se realiza la notificación mediante la programación de la rutina de finalización.                                                                                                                                           |



 

 

 
