---
title: Suscripción a eventos
description: Para suscribirse a eventos, llame a la función EvtSubscribe.
ms.assetid: 1e86deeb-fc59-4658-9353-e4ced7ace89a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889c4ff440a17696fe6d908ff98d632ff7058ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695640"
---
# <a name="subscribing-to-events"></a><span data-ttu-id="c01ea-103">Suscripción a eventos</span><span class="sxs-lookup"><span data-stu-id="c01ea-103">Subscribing to Events</span></span>

<span data-ttu-id="c01ea-104">Para suscribirse a eventos, llame a la función [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="c01ea-104">To subscribe to events, call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span> <span data-ttu-id="c01ea-105">Puede suscribirse a eventos de uno o varios canales operativos o de administrador.</span><span class="sxs-lookup"><span data-stu-id="c01ea-105">You can subscribe to events from one or more Admin or Operational channels.</span></span> <span data-ttu-id="c01ea-106">El canal puede existir en el equipo local o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c01ea-106">The channel can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="c01ea-107">Para especificar los eventos a los que desea suscribirse, puede utilizar una consulta XPath o una consulta XML de estructura.</span><span class="sxs-lookup"><span data-stu-id="c01ea-107">To specify the events that you want to subscribe to, you can use an XPath query or a structure XML query.</span></span> <span data-ttu-id="c01ea-108">Para obtener más información sobre cómo escribir la consulta, vea [consumir eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="c01ea-108">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="c01ea-109">El registro de eventos de Windows proporciona dos modelos para la suscripción a eventos:</span><span class="sxs-lookup"><span data-stu-id="c01ea-109">Windows Event Log provides two models for event subscription:</span></span>

-   <span data-ttu-id="c01ea-110">El modelo de inserciones envía eventos de forma asincrónica a una devolución de llamada que se implementa.</span><span class="sxs-lookup"><span data-stu-id="c01ea-110">The push model pushes events asynchronously to a callback that you implement.</span></span>
-   <span data-ttu-id="c01ea-111">El modelo de extracción utiliza un identificador de eventos que se crea para indicar cuándo hay eventos disponibles que coinciden con los criterios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c01ea-111">The pull model uses an event handle that you create to signal you when there are events available that match your query criteria.</span></span> <span data-ttu-id="c01ea-112">A continuación, se enumeran los eventos en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c01ea-112">You then enumerate the events in the result set.</span></span>

<span data-ttu-id="c01ea-113">Puede suscribirse a eventos pasados y futuros, solo a eventos futuros o a eventos pasados y futuros que empiecen después del evento marcado.</span><span class="sxs-lookup"><span data-stu-id="c01ea-113">You can subscribe to past and future events, future events only, or past and future events beginning after the bookmarked event.</span></span>

<span data-ttu-id="c01ea-114">Para obtener más información sobre cómo suscribirse a eventos, consulte suscripciones de [inserción](#push-subscriptions) o [suscripciones de extracción](#pull-subscriptions).</span><span class="sxs-lookup"><span data-stu-id="c01ea-114">For details on subscribing to events, see [Push Subscriptions](#push-subscriptions) or [Pull Subscriptions](#pull-subscriptions).</span></span>

<span data-ttu-id="c01ea-115">Para obtener más información sobre cómo representar los eventos, vea [representar eventos](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="c01ea-115">For details on rendering the events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="c01ea-116">Si desea suscribirse a eventos desde donde lo dejó, cree un marcador antes de finalizar la suscripción y úselo la próxima vez que se suscriba a eventos.</span><span class="sxs-lookup"><span data-stu-id="c01ea-116">If you want to subscribe to events from where you left off, create a bookmark before ending your subscription and use it the next time you subscribe to events.</span></span> <span data-ttu-id="c01ea-117">Para obtener más información, vea [marcar eventos](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="c01ea-117">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

## <a name="push-subscriptions"></a><span data-ttu-id="c01ea-118">Suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="c01ea-118">Push Subscriptions</span></span>

<span data-ttu-id="c01ea-119">En el ejemplo siguiente se muestra cómo suscribirse a eventos, implementar la devolución de llamada de la suscripción y representar los eventos.</span><span class="sxs-lookup"><span data-stu-id="c01ea-119">The following example shows how to subscribe to events, implement the subscription callback, and render the events.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Subscribe to events beginning with the oldest event in the channel. The subscription
    // will return all current events in the channel and any future events that are raised
    // while the application is active.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, NULL, NULL, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call EvtGetExtendedStatus to get information as to why the query is not valid.
            wprintf(L"The query \"%s\" is not valid.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);
}

// The callback that receives the events that match the query criteria. 
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    UNREFERENCED_PARAMETER(pContext);
    
    DWORD status = ERROR_SUCCESS;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }
            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }
            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



## <a name="pull-subscriptions"></a><span data-ttu-id="c01ea-120">Suscripciones de extracción</span><span class="sxs-lookup"><span data-stu-id="c01ea-120">Pull Subscriptions</span></span>

<span data-ttu-id="c01ea-121">El modelo de suscripción de extracción utiliza un objeto de evento (vea la función [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) ) para indicar a la aplicación que hay eventos en el conjunto de resultados que coinciden con los criterios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c01ea-121">The pull subscription model uses an event object (see the [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) function) to signal the application that there are events in the result set that match the query criteria.</span></span> <span data-ttu-id="c01ea-122">Cree una construcción de bucle que espere en el objeto de evento hasta que se señale el evento.</span><span class="sxs-lookup"><span data-stu-id="c01ea-122">Create a loop construct that waits on the event object until the event is signaled.</span></span> <span data-ttu-id="c01ea-123">A continuación, llame a la función [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) en un bucle para enumerar los eventos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c01ea-123">Then, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events in the result set.</span></span> <span data-ttu-id="c01ea-124">Cuando se produce un error en la función **EvtNext** y se establece el último error en \_ no hay \_ más \_ elementos, restablezca el objeto de evento y espere a que el servicio señale de nuevo el objeto cuando haya eventos en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c01ea-124">When the **EvtNext** function fails and sets the last error to ERROR\_NO\_MORE\_ITEMS, reset the event object and wait for the service to signal the object again when there are events in the result set.</span></span>

<span data-ttu-id="c01ea-125">En el ejemplo siguiente se muestra cómo usar el modelo de suscripción de extracción.</span><span class="sxs-lookup"><span data-stu-id="c01ea-125">The following example shows how to use the pull subscription model.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD EnumerateResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);
BOOL IsKeyEvent(HANDLE hStdIn);

void __cdecl wmain()
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"*";
    HANDLE aWaitHandles[2];
    DWORD dwWait = 0;

    // Get a handle for console input, so you can break out of the loop.
    aWaitHandles[0] = GetStdHandle(STD_INPUT_HANDLE);
    if (INVALID_HANDLE_VALUE == aWaitHandles[0])
    {
        wprintf(L"GetStdHandle failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Get a handle to a manual reset event object that the subscription will signal
    // when events become available that match your query criteria.
    aWaitHandles[1] = CreateEvent(NULL, TRUE, TRUE, NULL);
    if (NULL == aWaitHandles[1])
    {
        wprintf(L"CreateEvent failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Subscribe to events.
    hSubscription = EvtSubscribe(NULL, aWaitHandles[1], pwsPath, pwsQuery, NULL, NULL, NULL, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            wprintf(L"The query %s was not found.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Press any key to quit.\n");

    // Loop until the user presses a key or there is an error.
    while (true)
    {
        dwWait = WaitForMultipleObjects(sizeof(aWaitHandles)/sizeof(HANDLE), aWaitHandles, FALSE, INFINITE);

        if (0 == dwWait - WAIT_OBJECT_0)  // Console input
        {
            if (IsKeyEvent(aWaitHandles[0]))
                break;
        }
        else if (1 == dwWait - WAIT_OBJECT_0) // Query results
        {
            if (ERROR_NO_MORE_ITEMS != (status = EnumerateResults(hSubscription)))
            {
                break;
            }

            ResetEvent(aWaitHandles[1]);
        }
        else
        {
            if (WAIT_FAILED == dwWait)
            {
                wprintf(L"WaitForSingleObject failed with %lu\n", GetLastError());
            }
            break;
        }
    }

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (aWaitHandles[0])
        CloseHandle(aWaitHandles[0]);

    if (aWaitHandles[1])
        CloseHandle(aWaitHandles[1]);
}

// Enumerate the events in the result set.
DWORD EnumerateResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    // Closes any events in case an error occurred above.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}

// Determines whether the console input was a key event.
BOOL IsKeyEvent(HANDLE hStdIn)
{
    INPUT_RECORD Record[128];
    DWORD dwRecordsRead = 0;
    BOOL fKeyPress = FALSE;

    if (ReadConsoleInput(hStdIn, Record, 128, &dwRecordsRead))
    {
        for (DWORD i = 0; i < dwRecordsRead; i++)
        {
            if (KEY_EVENT == Record[i].EventType)
            {
                fKeyPress = TRUE;
                break;
            }
        }
    }

    return fKeyPress;
}
```



 

 