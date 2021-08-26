---
title: Rutinas de finalización HTTP
description: Las aplicaciones tienen varias opciones para recibir indicaciones de finalización y proporcionar cierta flexibilidad a los desarrolladores.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd80259d806d81153a649ad606e40c10986090442e3cab5e04bd864367441871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981675"
---
# <a name="http-completion-routines"></a>Rutinas de finalización HTTP

Las aplicaciones tienen varias opciones para recibir indicaciones de finalización y proporcionar cierta flexibilidad a los desarrolladores. Las opciones son bloquear mientras se espera a que se complete una llamada API o usar rutinas de finalización para operaciones asincrónicas. La ventaja de usar operaciones asincrónicas es un aumento de la capacidad de respuesta de la aplicación.

## <a name="blocked-io"></a>E/S bloqueada

Las aplicaciones pueden bloquearse mientras esperan a que se complete la llamada API estableciendo [**la estructura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en **NULL.** Esto bloquea realmente todas las operaciones en el subproceso. Por ejemplo, en las llamadas a [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), la llamada se bloquea hasta que se divide la conexión.

## <a name="asynchronous-io"></a>E/S asincrónica

Las aplicaciones que prefieren no bloquear pueden usar la [**estructura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para obtener los resultados de finalización. La aplicación proporciona un puntero a una **estructura OVERLAPPED,** que se usa con un objeto de evento o un puerto de finalización. Con un puerto de finalización de E/S, se usa un identificador HTTP, ya que un identificador de archivo estaría en una operación asincrónica de E/S de archivo. En la tabla siguiente se resumen las opciones de finalización disponibles para las aplicaciones.



| Estructura superpuesta | Objeto de evento   | Puerto de finalización | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | No es aplicable | Omitido         | La operación se completa sincrónicamente.                                                                           |
| Distinto de **NULL**         | Distinto de **NULL**   | **NULL**        | La operación se completa de forma asincrónica. La notificación superpuesta se realiza mediante la señalización de un objeto de evento.       |
| Distinto de **NULL**         | Omitido        | Distinto de **NULL**    | La operación se completa de forma asincrónica. La notificación superpuesta se realiza programando una rutina de finalización. |



 

## <a name="returning-the-number-of-bytes-read"></a>Devolver el número de bytes leídos

Algunas de las funciones que usan la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para la finalización asincrónica devuelven un parámetro *pBytesReceived* (o *pBytesSent* o *pBytesRead)* que indica el número de bytes transferidos sincrónicamente. Para las llamadas asincrónicas, este parámetro debe establecerse en **NULL.** Para las llamadas sincrónicas, el *parámetro pBytesReceived* es opcional y puede ser **NULL** o no **NULL.**

Si el objeto de evento se usa para la finalización asincrónica, se llama a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar el número de bytes leídos. Si se usa el puerto de finalización (el parámetro *hFile* está asociado a un puerto de finalización de E/S), la aplicación llama a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para determinar el número de bytes leídos. Si las operaciones asincrónicas no se han completado, las aplicaciones pueden llamar a la [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener información de error extendida.

En la tabla siguiente se resume el comportamiento de finalización para la finalización sincrónica y asincrónica en funciones como [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) que usan el *parámetro pBytesReceived.*



| pBytesReceived\* | pOverlapped  | Descripción                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | La aplicación no recibe información sobre el número de bytes devueltos.           |
| **NULL**         | Distinto de **NULL** | Operación asincrónica, *pBytesReceived* no tiene sentido.                                |
| Distinto de **NULL**     | **NULL**     | Operación sincrónica, número de bytes *devueltos en pBytesReceived*.                    |
| Distinto de **NULL**     | Distinto de **NULL** | Operación asincrónica, *pBytesReceived* se omite aunque no sea **NULL.**\*\* |



 

> [!Note]  
> \*Este parámetro también puede ser *pBytesSent* o *pBytesRead.*

 

> [!Note]  
> \*\*Se recomienda que las aplicaciones pasen un **valor NULL** en *pBytesReceived* para las operaciones asincrónicas y obtengan el número de bytes recibidos de [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

 

## <a name="return-codes"></a>Códigos de retorno

La API del servidor HTTP devuelve tres clases de códigos para las llamadas a funciones asincrónicas.

-   NO \_ ERROR
-   E/S DE ERROR \_ \_ PENDIENTE
-   Cualquier otro [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Cuando ERROR IO PENDING o NO ERROR se devuelven desde la llamada de función asincrónica, los usuarios deben esperar que se señale el evento o la rutina \_ \_ de \_ finalización. Al llamar [**a la función GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para el evento o a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para el puerto de finalización, se devuelve el estado de finalización. Además, si no se devuelve NINGÚN ERROR, las aplicaciones pueden realizar el procesamiento posterior \_ en el mismo subproceso que realizó la llamada API.

Si la API del servidor HTTP devuelve algo distinto de ERROR IO PENDING o NO ERROR, desde la llamada de función asincrónica, la rutina de finalización no se señala y la API devuelve directamente \_ \_ el \_ error.

 

 