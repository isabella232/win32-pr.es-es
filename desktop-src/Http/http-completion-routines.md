---
title: Rutinas de finalización HTTP
description: Las aplicaciones tienen varias opciones para recibir indicaciones de finalización y proporcionar cierta flexibilidad a los desarrolladores.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee05efc8284cb29130efae4bcaefb4834a3fb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995239"
---
# <a name="http-completion-routines"></a>Rutinas de finalización HTTP

Las aplicaciones tienen varias opciones para recibir indicaciones de finalización y proporcionar cierta flexibilidad a los desarrolladores. Las opciones se bloquean mientras se espera a que se complete una llamada API o se usan rutinas de finalización para las operaciones asincrónicas. La ventaja de usar operaciones asincrónicas es un aumento de la capacidad de respuesta de la aplicación.

## <a name="blocked-io"></a>E/s bloqueada

Las aplicaciones pueden bloquear mientras esperan a que se complete la llamada a la API estableciendo la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en **null**. Esto bloquea realmente todas las operaciones en el subproceso. Por ejemplo, en las llamadas a [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), la llamada se bloquea hasta que se interrumpe la conexión.

## <a name="asynchronous-io"></a>E/s asincrónica

Las aplicaciones que prefieren no bloquearse pueden utilizar la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para obtener los resultados de finalización. La aplicación proporciona un puntero a una estructura **superpuesta** , que se utiliza con un objeto de evento o un puerto de finalización. Con un puerto de finalización de e/s, se usa un identificador HTTP como identificador de archivo en una operación asincrónica de e/s de archivos. En la tabla siguiente se resumen las opciones de finalización disponibles para las aplicaciones.



| Estructura superpuesta | Objeto de evento   | Puerto de finalización | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | No es aplicable | Omitido         | La operación se completa de forma sincrónica.                                                                           |
| No **null**         | No **null**   | **NULL**        | La operación se completa de forma asincrónica. La notificación superpuesta se realiza mediante la señalización de un objeto de evento.       |
| No **null**         | Omitido        | No **null**    | La operación se completa de forma asincrónica. La notificación superpuesta se realiza mediante la programación de una rutina de finalización. |



 

## <a name="returning-the-number-of-bytes-read"></a>Devolver el número de bytes leídos

Algunas de las funciones que usan la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) para la finalización asincrónica devuelven un parámetro *PBytesReceived* (o *pBytesSent* o *pBytesRead*) que indica el número de bytes transferidos sincrónicamente. En el caso de las llamadas asincrónicas, este parámetro debe establecerse en **null**. En el caso de las llamadas sincrónicas, el parámetro *pBytesReceived* es opcional y puede ser **null** o no **null**.

Si el objeto de evento se utiliza para la finalización asincrónica, se llama a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar el número de bytes leídos. Si se usa el puerto de finalización (el parámetro *hFile* está asociado a un puerto de finalización de e/s), la aplicación llama a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para determinar el número de bytes leídos. Si no se han completado las operaciones asincrónicas, las aplicaciones pueden llamar a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener información de error extendida.

En la tabla siguiente se resume el comportamiento de finalización de la finalización sincrónica y asincrónica de funciones como [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) que usan el parámetro *pBytesReceived* .



| pBytesReceived\* | pOverlapped  | Descripción                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | La aplicación no recibe información sobre el número de bytes devueltos.           |
| **NULL**         | No **null** | Operación asincrónica, *pBytesReceived* no tiene sentido.                                |
| No **null**     | **NULL**     | Operación sincrónica, número de bytes devueltos en *pBytesReceived*.                    |
| No **null**     | No **null** | Operación asincrónica, *pBytesReceived* se omite aunque no sea **null**.\*\* |



 

> [!Note]  
> \*Este parámetro también puede ser *pBytesSent* o *pBytesRead*.

 

> [!Note]  
> \*\*Se recomienda que las aplicaciones pasen un **valor null** en *pBytesReceived* para las operaciones asincrónicas y obtengan el número de bytes recibidos de [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

 

## <a name="return-codes"></a>Códigos de retorno

La API del servidor HTTP devuelve tres clases de códigos para las llamadas de función asincrónicas.

-   SIN \_ errores
-   \_e/s de errores \_ pendientes
-   Cualquier otro [código de error del sistema](/windows/desktop/Debug/system-error-codes).

Cuando \_ se produce un error de e/s \_ pendiente o no \_ se devuelve ningún error de la llamada de función asincrónica, los usuarios deben esperar que se señale el evento o la rutina de finalización. La llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para el evento o la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para el puerto de finalización devuelve el estado de finalización. Además, si NO \_ se devuelve ningún error, las aplicaciones pueden realizar el procesamiento posterior en el mismo subproceso que realizó la llamada API.

Si la API del servidor HTTP devuelve algo distinto del ERROR de \_ e/s \_ pendiente o NO hay ningún \_ error, de la llamada de función asincrónica, la rutina de finalización no se señala y el error lo devuelve directamente la API.

 

 