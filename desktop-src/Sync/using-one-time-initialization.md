---
description: En los siguientes ejemplos se muestra el uso de las funciones de inicialización de una sola vez.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Usar la inicialización de One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546382"
---
# <a name="using-one-time-initialization"></a>Usar la inicialización de One-Time

En los siguientes ejemplos se muestra el uso de las funciones de inicialización de una sola vez.

## <a name="synchronous-example"></a>Ejemplo sincrónico

En este ejemplo, la `g_InitOnce` variable global es la estructura de inicialización única. Se inicializa de forma estática mediante **init \_ una vez \_ \_** el inicializador estático.

La `OpenEventHandleSync` función devuelve un identificador para un evento que se crea solo una vez. Llama a la función [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) para ejecutar el código de inicialización contenido en la `InitHandleFunction` función de devolución de llamada. Si la función de devolución de llamada se ejecuta correctamente, `OpenEventHandleSync` devuelve el identificador de evento devuelto en *lpContext*; de lo contrario, devuelve un **\_ \_ valor de identificador no válido**.

La `InitHandleFunction` función es la [función de devolución de llamada de inicialización única](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn). `InitHandleFunction` llama a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear el evento y devuelve el identificador de evento en el parámetro *lpContext* .


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a>Ejemplo asincrónico

En este ejemplo, la `g_InitOnce` variable global es la estructura de inicialización única. Se inicializa de forma estática mediante **init \_ una vez \_ \_** el inicializador estático.

La `OpenEventHandleAsync` función devuelve un identificador para un evento que se crea solo una vez. `OpenEventHandleAsync` llama a la función [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) para entrar en el estado de inicialización.

Si la llamada se realiza correctamente, el código comprueba el valor del parámetro *fPending* para determinar si se debe crear el evento o simplemente devolver un identificador para el evento creado por otro subproceso. Si *fPending* es **false**, ya se ha completado la inicialización, por lo que `OpenEventHandleAsync` devuelve el identificador de evento devuelto en el parámetro *lpContext* . De lo contrario, llama a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear el evento y la función [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) para completar la inicialización.

Si la llamada a [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) se realiza correctamente, `OpenEventHandleAsync` devuelve el nuevo controlador de eventos. De lo contrario, cierra el identificador de eventos y llama a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una vez \_ \_ solo** para determinar si otro subproceso ha producido un error de inicialización o ha finalizado.

Si otro subproceso ha completado la inicialización, `OpenEventHandleAsync` devuelve el identificador de evento devuelto en *lpContext*. De lo contrario, devuelve un **\_ \_ valor de identificador no válido**.


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización única](one-time-initialization.md)
</dt> </dl>

 

 
