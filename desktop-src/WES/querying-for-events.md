---
title: Consulta de eventos
description: Puede consultar eventos desde un canal o un archivo de registro.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e4a8c39daebbce641c79e7d26331b9b36845d3c71fd1902ea667ca85c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587806"
---
# <a name="querying-for-events"></a>Consulta de eventos

Puede consultar eventos desde un canal o un archivo de registro. El canal o el archivo de registro pueden existir en el equipo local o en un equipo remoto. Para especificar los eventos que desea obtener del canal o archivo de registro, use una consulta XPath o una consulta XML de estructura. Para obtener más información sobre cómo escribir la consulta, vea [Consumo de eventos](consuming-events.md).

Para consultar eventos, llame a la [**función EvtQuery.**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) Puede especificar el orden en el que se devuelven los eventos (de más antiguo a más reciente (el valor predeterminado) o el más reciente al más antiguo) y si se toleran expresiones XPath con formato correcto en la consulta (para más información sobre cómo la función omite las expresiones con formato anterior, consulte la marca [**EvtQueryTolerateQueryErrors).**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)

En el ejemplo siguiente se muestra cómo consultar eventos desde un canal mediante una expresión XPath.


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



En el ejemplo siguiente se muestra cómo consultar eventos desde un canal mediante una consulta XML estructurada. Los eventos se devuelven en orden de más reciente a más antiguo.


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



Si usa una consulta XML estructurada y pasa la marca EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), la función se realiza correctamente aunque una o varias de las consultas de la consulta estructurada puedan haber fallado realmente. Para determinar qué consultas de la consulta estructurada se realizaron correctamente o no, llame a la [**función EvtGetQueryInfo.**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) Si no pasa la marca EvtQueryTolerateQueryErrors, se producirá un error en la función **EvtQuery** con el primer error que encuentre en la consulta. Si se produce un error en la consulta con ERROR EVT INVALID QUERY, llame a la función \_ \_ \_ [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) para obtener una cadena de mensaje que describa el error XPath.

En el ejemplo siguiente se muestra cómo determinar el éxito o el error de cada consulta en una consulta estructurada al pasar la marca EvtQueryTolerateQueryErrors a [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).


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



## <a name="reading-events-from-the-result-set"></a>Lectura de eventos del conjunto de resultados

Para enumerar los eventos del conjunto de resultados, llame a la función [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) en un bucle hasta que la función devuelva **FALSE** y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelva ERROR \_ NO MORE \_ \_ ITEMS. Los eventos del conjunto de resultados no son estáticos; Los nuevos eventos que se escriben en el canal se incluirán en el conjunto de resultados hasta que no se establezca ERROR \_ NO \_ MORE \_ ITEMS. Para mejorar el rendimiento, obtenga eventos del conjunto de resultados en lotes (teniendo en cuenta el tamaño de cada evento al determinar el número de eventos que se capturarán).

En el ejemplo siguiente se muestra cómo enumerar los eventos de un conjunto de resultados.


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



Para obtener más información sobre cómo representar los eventos que obtiene del conjunto de resultados, vea [Representación de eventos](rendering-events.md).

Si desea consultar eventos desde donde lo dejó, cree un marcador del último evento que lea y úselo la próxima vez que ejecute la consulta. Para obtener más información, [vea Bookmarking Events](bookmarking-events.md).

 

 