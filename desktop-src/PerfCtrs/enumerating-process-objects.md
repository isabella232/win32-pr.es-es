---
description: En el ejemplo siguiente se llama a la función PdhEnumObjectItems para enumerar las instancias y los contadores de los objetos de proceso en el equipo local.
ms.assetid: d7518ba6-a0f1-4985-aa2c-1ca15a0ceb02
title: Enumerar objetos de proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329afb511a4551ba0449b826c7eece26d609816b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667329"
---
# <a name="enumerating-process-objects"></a><span data-ttu-id="95551-103">Enumerar objetos de proceso</span><span class="sxs-lookup"><span data-stu-id="95551-103">Enumerating Process Objects</span></span>

<span data-ttu-id="95551-104">En el ejemplo siguiente se llama a la función [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) para enumerar las instancias y los contadores de los objetos de proceso en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="95551-104">The following example calls the [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) function to enumerate the instances and counters of the process objects on the local computer.</span></span>


```C++
// This program needs only the essential Windows header files.
#define WIN32_LEAN_AND_MEAN 1

#include <windows.h>
#include <malloc.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_OBJECT = L"Process";

void main(void)
{
    PDH_STATUS status = ERROR_SUCCESS;
    LPWSTR pwsCounterListBuffer = NULL;
    DWORD dwCounterListSize = 0;
    LPWSTR pwsInstanceListBuffer = NULL;
    DWORD dwInstanceListSize = 0;
    LPWSTR pTemp = NULL;

    // Determine the required buffer size for the data. 
    status = PdhEnumObjectItems(
        NULL,                   // real-time source
        NULL,                   // local machine
        COUNTER_OBJECT,         // object to enumerate
        pwsCounterListBuffer,   // pass NULL and 0
        &dwCounterListSize,     // to get required buffer size
        pwsInstanceListBuffer, 
        &dwInstanceListSize, 
        PERF_DETAIL_WIZARD,     // counter detail level
        0); 

    if (status == PDH_MORE_DATA) 
    {
        // Allocate the buffers and try the call again.
        pwsCounterListBuffer = (LPWSTR)malloc(dwCounterListSize * sizeof(WCHAR));
        pwsInstanceListBuffer = (LPWSTR)malloc(dwInstanceListSize * sizeof(WCHAR));

        if (NULL != pwsCounterListBuffer && NULL != pwsInstanceListBuffer) 
        {
            status = PdhEnumObjectItems(
                NULL,                   // real-time source
                NULL,                   // local machine
                COUNTER_OBJECT,         // object to enumerate
                pwsCounterListBuffer, 
                &dwCounterListSize,
                pwsInstanceListBuffer, 
                &dwInstanceListSize, 
                PERF_DETAIL_WIZARD,     // counter detail level
                0); 
     
            if (status == ERROR_SUCCESS) 
            {
                wprintf(L"Counters that the Process objects defines:\n\n");

                // Walk the counters list. The list can contain one
                // or more null-terminated strings. The list is terminated
                // using two null-terminator characters.
                for (pTemp = pwsCounterListBuffer; *pTemp != 0; pTemp += wcslen(pTemp) + 1) 
                {
                     wprintf(L"%s\n", pTemp);
                }

                wprintf(L"\nInstances of the Process object:\n\n");

                // Walk the instance list. The list can contain one
                // or more null-terminated strings. The list is terminated
                // using two null-terminator characters.
                for (pTemp = pwsInstanceListBuffer; *pTemp != 0; pTemp += wcslen(pTemp) + 1) 
                {
                     wprintf(L"%s\n", pTemp);
                }
            }
            else 
            {
                wprintf(L"Second PdhEnumObjectItems failed with %0x%x.\n", status);
            }
        } 
        else 
        {
            wprintf(L"Unable to allocate buffers.\n");
            status = ERROR_OUTOFMEMORY;
        }
    } 
    else 
    {
        wprintf(L"\nPdhEnumObjectItems failed with 0x%x.\n", status);
    }

    if (pwsCounterListBuffer != NULL) 
        free (pwsCounterListBuffer);

    if (pwsInstanceListBuffer != NULL) 
        free (pwsInstanceListBuffer);
}
```



 

 



