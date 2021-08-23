---
description: LSA proporciona funciones que puede usar para recibir notificaciones cuando hay un cambio en la directiva en el sistema local.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Recepción de eventos de cambio de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1fc2328d0467dcfe5b6f85b9b8384cf4c8271d35fcda106a61ae5bb068f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005053"
---
# <a name="receiving-policy-change-events"></a>Recepción de eventos de cambio de directiva

LSA proporciona funciones que puede usar para recibir notificaciones cuando hay un cambio en la directiva en el sistema local.

Para recibir una notificación, cree un nuevo objeto de evento mediante una llamada a la [**función CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) y, a continuación, llame a la función [**LsaRegisterPolicyChangeNotification.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) A continuación, la aplicación puede llamar a una función wait como [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)o [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) para esperar a que se produzca el evento. La función wait devuelve cuando se produce el evento o cuando expira el período de tiempo de espera. Normalmente, los eventos de notificación se usan en aplicaciones multiproceso, en las que un subproceso espera un evento, mientras que otros subprocesos continúan procesando.

Cuando la aplicación ya no necesite recibir notificaciones, debe llamar a [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) y, a continuación, llamar a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar el identificador del objeto de evento.

En el ejemplo siguiente se muestra cómo una aplicación de un solo subproceso puede recibir eventos de notificación cuando cambia la directiva de auditoría del sistema.


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



Para obtener más información sobre los objetos de evento, las funciones de espera y la sincronización, vea [Using Event Objects](/windows/desktop/Sync/using-event-objects).

 

 
