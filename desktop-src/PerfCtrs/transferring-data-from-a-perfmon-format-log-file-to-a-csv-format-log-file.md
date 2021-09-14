---
description: En el ejemplo siguiente se transfieren datos de un archivo de registro de contadores creado por la herramienta Rendimiento a un formato separado por comas (.csv).
ms.assetid: 5adeda14-0312-45ce-af91-6888f3aa1c95
title: Convertir datos de un archivo de registro de formato binario en un archivo de registro con formato CSV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2748ef834b82de09ce0fa9f5ca8a36c85781eaa6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062874"
---
# <a name="converting-data-from-a-binary-format-log-file-to-a-csv-format-log-file"></a>Convertir datos de un archivo de registro de formato binario en un archivo de registro con formato CSV

En el ejemplo siguiente se transfieren datos de un archivo de registro de contadores creado por la herramienta Rendimiento a un formato separado por comas (.csv). En el ejemplo se transfieren los datos del contador de tiempo de procesador recopilados del equipo local. Para especificar otro tipo de datos de contador, cambie la variable szCounterPath. Si los datos del contador recopilados son de un equipo específico, agregue el nombre del equipo a la ruta de acceso (por ejemplo, "nombreDeEquipo \\ \\ \\ \\ &lt; &gt; \\ \\ Procesador(0) \\ \\ % tiempo de procesador").


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH = L"\\Processor(0)\\% Processor Time";

void DisplayCommandLineHelp(void)
{
    wprintf(L"Syntax: convertlog <input file name> <output file name>\n"
        L"\nThe input log file must be in the Perfmon format. The output\n"
        L"log file will written in the CSV file format, so specify a .csv extension.");
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hOutputLog = NULL;
    HCOUNTER hCounter = NULL;
    PDH_STATUS pdhStatus = ERROR_SUCCESS;
    DWORD dwOutputLogType = PDH_LOG_TYPE_CSV;

    if (3 != argc)
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Create the query object using the input log file.
    pdhStatus = PdhOpenQuery(argv[1], 0, &hQuery);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
   
    // Add the counter to the query object; identifies the counter
    // records from the log file that you are going to relog to 
    // the new log file.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Create and open the output log file.
    pdhStatus = PdhOpenLog(argv[2], 
        PDH_LOG_WRITE_ACCESS | 
        PDH_LOG_CREATE_ALWAYS,
        &dwOutputLogType,
        hQuery,
        0, 
        NULL,
        &hOutputLog);

    if (ERROR_SUCCESS != pdhStatus)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Transfer the log records from the input file to the output file.
    while (ERROR_SUCCESS == pdhStatus) 
    { 
        pdhStatus = PdhUpdateLog(hOutputLog, NULL);
    }

    if (PDH_NO_MORE_DATA != pdhStatus)
    {
        wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
    }

cleanup:

   // Close the output log file.
   if (hOutputLog)
      PdhCloseLog(hOutputLog, 0);

   // Close the query object and input log file.
   if (hQuery)
      PdhCloseQuery(hQuery);
}
```



 

 



