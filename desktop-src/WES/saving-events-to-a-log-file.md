---
title: Guardar eventos en un archivo de registro
description: Para guardar eventos de un canal en un archivo de registro, llame a la función EvtClearLog o EvtExportLog.
ms.assetid: 6d71ed15-97e3-4888-b161-c7e31bf3fc6d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9bfafe5d1d9f75c85db4a0cc21fc3b9ae8d660aa08b542973b5e38b069158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031965"
---
# <a name="saving-events-to-a-log-file"></a>Guardar eventos en un archivo de registro

Para guardar eventos de un canal en un archivo de registro, llame a la [**función EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) o [**EvtExportLog.**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) La [**función EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) copia los eventos en el archivo de registro y los elimina del canal. La [**función EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) también copia los eventos en el archivo de registro, pero no los elimina del canal. Para borrar un canal, el usuario debe tener los permisos Leer y Borrar.

Puede consultar eventos desde el archivo de registro que ha creado; sin embargo, para representar los eventos, el proveedor debe estar registrado en el equipo. Para representar eventos de un archivo de registro cuando el proveedor no está registrado en el equipo, debe llamar a [**EvtArchiveExportedLog**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog), que copia los recursos del proveedor y los agrega al archivo de registro. A continuación, puede copiar el archivo de registro en cualquier equipo y consultar y representar correctamente sus eventos.

Además de usar [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) para copiar eventos de un canal, también puede usarlo para volver a registrar eventos de un archivo de registro a otro archivo de registro. También puede usarlo para combinar eventos de varios canales si usa una consulta XML estructurada, pero no puede usarla para combinar eventos de varios archivos de registro.

En el ejemplo siguiente se muestra cómo copiar eventos de un canal a un archivo de registro. A continuación, el ejemplo vuelve a registrar eventos específicos del archivo de registro recién creado en un nuevo archivo de registro.


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD DumpEvents(LPCWSTR pwsLogFile);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pPath = L"<path to channel goes here>";
    LPWSTR pQuery = NULL;
    LPWSTR pTargetLogFile = L".\\log.evtx";

    // Export all the events in the specified channel to the target log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogChannelPath))
    {
        wprintf(L"EvtExportLog failed for initial export with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

    // Create a new log file that will contain all events from the specified 
    // log file where the event ID is 2.
    pPath =  L".\\log.evtx";
    pQuery = L"Event/System[EventID=2]";
    pTargetLogFile = L".\\log2.evtx";

    // Export all events from the specified log file that have an ID of 2 and
    // write them to a new log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogFilePath))
    {
        wprintf(L"EvtExportLog failed for relog with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"\n\n\nEvents from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}


// Dump all the events in the from the log file.
DWORD DumpEvents(LPCWSTR pwsPath)
{
    EVT_HANDLE hResults = NULL;
    DWORD status = ERROR_SUCCESS;

    hResults = EvtQuery(NULL, pwsPath, NULL, EvtQueryFilePath);
    if (NULL == hResults)
    {
        wprintf(L"EvtQuery failed with %lu.\n", status = GetLastError());
        goto cleanup;
    }

    status = PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

    return status;
}


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

    // Executed only if there was an error.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}


// Print the event as an XML string.
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
```



En el ejemplo siguiente se muestra cómo combinar eventos de varios canales mediante una consulta XML estructurada. En el ejemplo se reemplaza el procedimiento principal del ejemplo anterior.


```C++
void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pTargetLogFile = L".\\log.evtx";
    LPWSTR pQuery = L"<QueryList>"
                    L"  <Query Id='0'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"  <Query Id='1'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"</QueryList>";

    if (!EvtExportLog(NULL, NULL, pQuery, pTargetLogFile, EvtExportLogChannelPath)) 
    {
        wprintf(L"EvtExportLog failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}
```



 

 




