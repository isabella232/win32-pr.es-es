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
# <a name="using-one-time-initialization"></a><span data-ttu-id="21a05-103">Usar la inicialización de One-Time</span><span class="sxs-lookup"><span data-stu-id="21a05-103">Using One-Time Initialization</span></span>

<span data-ttu-id="21a05-104">En los siguientes ejemplos se muestra el uso de las funciones de inicialización de una sola vez.</span><span class="sxs-lookup"><span data-stu-id="21a05-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="21a05-105">Ejemplo sincrónico</span><span class="sxs-lookup"><span data-stu-id="21a05-105">Synchronous Example</span></span>

<span data-ttu-id="21a05-106">En este ejemplo, la `g_InitOnce` variable global es la estructura de inicialización única.</span><span class="sxs-lookup"><span data-stu-id="21a05-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="21a05-107">Se inicializa de forma estática mediante **init \_ una vez \_ \_** el inicializador estático.</span><span class="sxs-lookup"><span data-stu-id="21a05-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="21a05-108">La `OpenEventHandleSync` función devuelve un identificador para un evento que se crea solo una vez.</span><span class="sxs-lookup"><span data-stu-id="21a05-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="21a05-109">Llama a la función [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) para ejecutar el código de inicialización contenido en la `InitHandleFunction` función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="21a05-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="21a05-110">Si la función de devolución de llamada se ejecuta correctamente, `OpenEventHandleSync` devuelve el identificador de evento devuelto en *lpContext*; de lo contrario, devuelve un **\_ \_ valor de identificador no válido**.</span><span class="sxs-lookup"><span data-stu-id="21a05-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="21a05-111">La `InitHandleFunction` función es la [función de devolución de llamada de inicialización única](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span><span class="sxs-lookup"><span data-stu-id="21a05-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="21a05-112">`InitHandleFunction` llama a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear el evento y devuelve el identificador de evento en el parámetro *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="21a05-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


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



## <a name="asynchronous-example"></a><span data-ttu-id="21a05-113">Ejemplo asincrónico</span><span class="sxs-lookup"><span data-stu-id="21a05-113">Asynchronous Example</span></span>

<span data-ttu-id="21a05-114">En este ejemplo, la `g_InitOnce` variable global es la estructura de inicialización única.</span><span class="sxs-lookup"><span data-stu-id="21a05-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="21a05-115">Se inicializa de forma estática mediante **init \_ una vez \_ \_** el inicializador estático.</span><span class="sxs-lookup"><span data-stu-id="21a05-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="21a05-116">La `OpenEventHandleAsync` función devuelve un identificador para un evento que se crea solo una vez.</span><span class="sxs-lookup"><span data-stu-id="21a05-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="21a05-117">`OpenEventHandleAsync` llama a la función [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) para entrar en el estado de inicialización.</span><span class="sxs-lookup"><span data-stu-id="21a05-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="21a05-118">Si la llamada se realiza correctamente, el código comprueba el valor del parámetro *fPending* para determinar si se debe crear el evento o simplemente devolver un identificador para el evento creado por otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="21a05-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="21a05-119">Si *fPending* es **false**, ya se ha completado la inicialización, por lo que `OpenEventHandleAsync` devuelve el identificador de evento devuelto en el parámetro *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="21a05-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="21a05-120">De lo contrario, llama a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para crear el evento y la función [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) para completar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="21a05-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="21a05-121">Si la llamada a [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) se realiza correctamente, `OpenEventHandleAsync` devuelve el nuevo controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="21a05-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="21a05-122">De lo contrario, cierra el identificador de eventos y llama a [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una vez \_ \_ solo** para determinar si otro subproceso ha producido un error de inicialización o ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="21a05-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="21a05-123">Si otro subproceso ha completado la inicialización, `OpenEventHandleAsync` devuelve el identificador de evento devuelto en *lpContext*.</span><span class="sxs-lookup"><span data-stu-id="21a05-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="21a05-124">De lo contrario, devuelve un **\_ \_ valor de identificador no válido**.</span><span class="sxs-lookup"><span data-stu-id="21a05-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="21a05-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21a05-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a05-126">Inicialización única</span><span class="sxs-lookup"><span data-stu-id="21a05-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 
