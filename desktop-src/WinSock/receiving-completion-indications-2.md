---
description: 'Hay varias opciones disponibles para recibir indicaciones de finalización, lo que proporciona a las aplicaciones con los niveles de flexibilidad adecuados. Entre ellos se incluyen: en espera (o bloqueo) en objetos de eventos, objetos de eventos de sondeo y rutinas de finalización de e/s de socket.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Recibir indicaciones de finalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd05d8297af17c26393b5db113fac283b39fcbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706982"
---
# <a name="receiving-completion-indications"></a>Recibir indicaciones de finalización

Hay varias opciones disponibles para recibir indicaciones de finalización, lo que proporciona a las aplicaciones con los niveles de flexibilidad adecuados. Entre ellos se incluyen: en espera (o bloqueo) en objetos de eventos, objetos de eventos de sondeo y rutinas de finalización de e/s de socket.

## <a name="blocking-and-waiting-for-completion-indication"></a>Indicación de bloqueo y espera de finalización

Las aplicaciones se pueden bloquear mientras se espera a que uno o varios objetos de evento se establezcan con la función [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . En las implementaciones de Windows, el proceso o subproceso realmente se bloquea. Dado que los objetos de evento de Windows Sockets 2 se implementan como eventos de Windows, la función nativa de Windows, [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) también puede usarse para este fin. Esto es especialmente útil si el subproceso tiene que esperar en los eventos socket y no Socket.

## <a name="polling-for-completion-indication"></a>Indicación de finalización de sondeo

Las aplicaciones que prefieren no bloquearse pueden utilizar la función [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para sondear el estado de finalización asociado a cualquier objeto de evento determinado. Esta función indica si se ha completado la operación superpuesta, y si se ha completado, organiza la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) para recuperar el estado de error de la operación superpuesta.

## <a name="using-socket-io-completion-routines"></a>Usar rutinas de finalización de e/s de socket

Las funciones que se usan para iniciar operaciones de e/s superpuestas ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) toman *lpCompletionRoutine* como parámetro de entrada opcional. Es un puntero a una función específica de la aplicación a la que se llama después de que se complete una operación de e/s superpuesta correctamente iniciada (correcta o incorrectamente). La rutina de finalización sigue las mismas reglas indicadas para las rutinas de finalización de e/s de archivos de Windows. Es decir, no se invoca la rutina de finalización hasta que el subproceso se encuentra en un estado de espera de alerta, por ejemplo, cuando se invoca la función [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) con la `fAlertable` marca establecida. Una aplicación que usa la opción de rutina de finalización para una solicitud de e/s superpuesta determinada no puede usar la opción wait de [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para esa misma solicitud de e/s superpuesta.

Los transportes permiten a una aplicación invocar operaciones de envío y recepción desde dentro del contexto de la rutina de finalización de e/s de socket y garantizar que, para un socket determinado, las rutinas de finalización de e/s no estarán anidadas. Esto permite que las transmisiones de datos que dependen del tiempo se produzcan por completo en un contexto preferente.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Resumen de mecanismos de indicación de finalización superpuestos

La indicación de finalización de e/s superpuestas determinada que se va a utilizar para una operación superpuesta determinada está determinada por si la aplicación proporciona un puntero a una función de finalización, si se hace referencia a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) y por el valor del miembro **hEvent** dentro de la estructura **WSAOVERLAPPED** (si se proporciona). En la tabla siguiente se resume la semántica de finalización de un socket superpuesto y se muestran las distintas combinaciones de *lpOverlapped*, **hEvent** y *lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Indicación de finalización                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | No aplicable | Omitido               | La operación se completa de forma sincrónica. Se comporta como si fuera un socket nonoverlapped.                                                                                                                                      |
| ! ACEPTA          | NULL           | NULL                  | La operación se completa superpuesta, pero no hay ningún mecanismo de finalización compatible con Windows Sockets 2. En este caso, se puede usar el mecanismo de puerto de finalización (si se admite). De lo contrario, no hay ninguna notificación de finalización. |
| ! ACEPTA          | ! ACEPTA          | NULL                  | La operación se completa y se notifica mediante un objeto de evento de señalización.                                                                                                                                                  |
| ! ACEPTA          | Omitido        | ! ACEPTA                 | La operación se completa y se notifica mediante la programación de la rutina de finalización.                                                                                                                                           |



 

 

 
