---
description: En el ejemplo siguiente se escriben datos de rendimiento en tiempo real en un archivo de registro.
ms.assetid: a1bc40ea-d928-495a-abc0-daf097202a12
title: Escribir datos de rendimiento en un archivo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97bce7d5256db5ebeaee659a12809535b9718bc6fdadc807c9d9ffdc8b67c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033085"
---
# <a name="writing-performance-data-to-a-log-file"></a>Escribir datos de rendimiento en un archivo de registro

En el ejemplo siguiente se escriben datos de rendimiento en tiempo real en un archivo de registro. En el ejemplo se llama a las funciones [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) y [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para crear una consulta para recopilar datos de contadores de tiempo de procesador. A continuación, en el ejemplo se [**llama a la función PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) para crear el archivo de registro en el que se escribirán los datos. En el ejemplo se llama a [**la función PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) para recopilar un ejemplo y actualizar el archivo de registro una vez por segundo durante 20 segundos.

Para obtener un ejemplo en el que se lee el archivo de registro generado, vea [Lectura de datos de rendimiento de un archivo de registro.](reading-performance-data-from-a-log-file.md)


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";
CONST ULONG SAMPLE_INTERVAL_MS = 1000;

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must include a valid log file name.\n"); 
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hLog = NULL;
    PDH_STATUS pdhStatus;
    DWORD dwLogType = PDH_LOG_TYPE_CSV;
    HCOUNTER hCounter;
    DWORD dwCount;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Open a query object.
    pdhStatus = PdhOpenQuery(NULL, 0, &hQuery);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Add one counter that will provide the data.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Open the log file for write access.
    pdhStatus = PdhOpenLog(argv[1], 
        PDH_LOG_WRITE_ACCESS | PDH_LOG_CREATE_ALWAYS,
        &dwLogType,
        hQuery,
        0, 
        NULL,
        &hLog);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
 
    // Write 10 records to the log file.
    for (dwCount = 0; dwCount < 10; dwCount++) 
    {
        wprintf(L"Writing record %d\n", dwCount);

        pdhStatus = PdhUpdateLog (hLog, NULL);
        if (ERROR_SUCCESS != pdhStatus)
        {
            wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
            goto cleanup;
        }

        // Wait one second between samples for a counter update.
        Sleep(SAMPLE_INTERVAL_MS); 
    }

cleanup:

    // Close the log file.
    if (hLog)
        PdhCloseLog (hLog, 0);

    // Close the query object.
    if (hQuery)
        PdhCloseQuery (hQuery);
}
```



 

 



