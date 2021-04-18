---
title: Consultar eventos
description: Puede consultar los eventos de un canal o un archivo de registro.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695738"
---
# <a name="querying-for-events"></a><span data-ttu-id="64508-103">Consultar eventos</span><span class="sxs-lookup"><span data-stu-id="64508-103">Querying for Events</span></span>

<span data-ttu-id="64508-104">Puede consultar los eventos de un canal o un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="64508-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="64508-105">El canal o el archivo de registro puede existir en el equipo local o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="64508-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="64508-106">Para especificar los eventos que desea obtener del archivo de registro o de canal, utilice una consulta XPath o una consulta XML de estructura.</span><span class="sxs-lookup"><span data-stu-id="64508-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="64508-107">Para obtener más información sobre cómo escribir la consulta, vea [consumir eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="64508-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="64508-108">Para consultar eventos, llame a la función [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) .</span><span class="sxs-lookup"><span data-stu-id="64508-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="64508-109">Puede especificar el orden en el que se devuelven los eventos (más antiguo a más reciente (valor predeterminado) o más reciente a más antiguo y si se toleran expresiones XPath con formato incorrecto en la consulta (para obtener detalles sobre cómo la función omite las expresiones con formato incorrecto, vea la marca [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).</span><span class="sxs-lookup"><span data-stu-id="64508-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="64508-110">En el ejemplo siguiente se muestra cómo consultar eventos desde un canal mediante una expresión XPath.</span><span class="sxs-lookup"><span data-stu-id="64508-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="64508-111">En el ejemplo siguiente se muestra cómo consultar eventos de un canal mediante una consulta XML estructurada.</span><span class="sxs-lookup"><span data-stu-id="64508-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="64508-112">Los eventos se devuelven en orden de más reciente a más antiguo.</span><span class="sxs-lookup"><span data-stu-id="64508-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="64508-113">Si está utilizando una consulta XML estructurada y pasa la marca EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la función se ejecutará correctamente aunque una o varias de las consultas de la consulta estructurada puedan haber producido un error en realidad.</span><span class="sxs-lookup"><span data-stu-id="64508-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="64508-114">Para determinar qué consultas de la consulta estructurada se han realizado correctamente o no, llame a la función [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) .</span><span class="sxs-lookup"><span data-stu-id="64508-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="64508-115">Si no pasa la marca EvtQueryTolerateQueryErrors, se producirá un error en la función **EvtQuery** con el primer error que encuentre en la consulta.</span><span class="sxs-lookup"><span data-stu-id="64508-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="64508-116">Si se produce un ERROR en la consulta con el ERROR \_ evt \_ consulta no válida \_ , llame a la función [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) para obtener una cadena de mensaje que describa el error XPath.</span><span class="sxs-lookup"><span data-stu-id="64508-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="64508-117">En el ejemplo siguiente se muestra cómo determinar el éxito o el error de cada consulta en una consulta estructurada al pasar la marca EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span><span class="sxs-lookup"><span data-stu-id="64508-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="64508-118">Leer eventos del conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="64508-118">Reading events from the result set</span></span>

<span data-ttu-id="64508-119">Para enumerar los eventos del conjunto de resultados, llame a la función [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) en un bucle hasta que la función devuelva **false** y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelva el error \_ no hay \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="64508-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="64508-120">Los eventos del conjunto de resultados no son estáticos; los nuevos eventos que se escriben en el canal se incluirán en el conjunto de resultados hasta que \_ no \_ \_ se establezcan los elementos.</span><span class="sxs-lookup"><span data-stu-id="64508-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="64508-121">Para mejorar el rendimiento, Capture los eventos del conjunto de resultados en lotes (teniendo en cuenta el tamaño de cada evento al determinar el número de eventos que se van a capturar).</span><span class="sxs-lookup"><span data-stu-id="64508-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="64508-122">En el ejemplo siguiente se muestra cómo enumerar los eventos en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="64508-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
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
        // event for display. PrintEvent is shown in RenderingEvents.
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

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="64508-123">Para obtener más información sobre la representación de los eventos que se obtienen del conjunto de resultados, vea [representar eventos](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="64508-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="64508-124">Si desea consultar eventos desde donde se quedó, cree un marcador del último evento que haya leído y úselo la próxima vez que ejecute la consulta.</span><span class="sxs-lookup"><span data-stu-id="64508-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="64508-125">Para obtener más información, vea [marcar eventos](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="64508-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 