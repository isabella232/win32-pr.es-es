---
description: LSA proporciona funciones que se pueden usar para recibir notificaciones cuando se produce un cambio en la Directiva en el sistema local.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Recepción de eventos de cambio de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686678"
---
# <a name="receiving-policy-change-events"></a><span data-ttu-id="14fab-103">Recepción de eventos de cambio de Directiva</span><span class="sxs-lookup"><span data-stu-id="14fab-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="14fab-104">LSA proporciona funciones que se pueden usar para recibir notificaciones cuando se produce un cambio en la Directiva en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="14fab-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="14fab-105">Para recibir una notificación, cree un nuevo objeto de evento llamando a la función [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) y, a continuación, llame a la función [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) .</span><span class="sxs-lookup"><span data-stu-id="14fab-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="14fab-106">A continuación, la aplicación puede llamar a una función wait, como [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)o [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) , para esperar a que se produzca el evento.</span><span class="sxs-lookup"><span data-stu-id="14fab-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="14fab-107">La función wait devuelve cuando se produce el evento o cuando expira el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="14fab-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="14fab-108">Normalmente, los eventos de notificación se utilizan en aplicaciones multiproceso, en las que un subproceso espera un evento, mientras que otros subprocesos continúan el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="14fab-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="14fab-109">Cuando la aplicación ya no necesita recibir notificaciones, debe llamar a [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) y, a continuación, llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar el identificador del objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="14fab-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="14fab-110">En el ejemplo siguiente se muestra cómo una aplicación de un solo subproceso puede recibir eventos de notificación cuando cambia la Directiva de auditoría del sistema.</span><span class="sxs-lookup"><span data-stu-id="14fab-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



<span data-ttu-id="14fab-111">Para obtener más información acerca de los objetos de evento, las funciones de espera y la sincronización, vea [usar objetos de evento](/windows/desktop/Sync/using-event-objects).</span><span class="sxs-lookup"><span data-stu-id="14fab-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 
