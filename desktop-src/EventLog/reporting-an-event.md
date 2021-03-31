---
description: Para notificar eventos, debe definir primero los eventos en un archivo de texto de mensaje. Para obtener más información sobre cómo escribir un archivo de texto de mensaje, vea archivos de texto de mensaje. A continuación se muestra el archivo de texto del mensaje que se usa en este ejemplo.
ms.assetid: ace31e17-a638-414f-8518-9b944118047b
title: Informes de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644163c5838b703d28db628c643c5cd12c73c22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812883"
---
# <a name="reporting-events"></a><span data-ttu-id="1a1cc-105">Informes de eventos</span><span class="sxs-lookup"><span data-stu-id="1a1cc-105">Reporting Events</span></span>

<span data-ttu-id="1a1cc-106">Para notificar eventos, debe definir primero los eventos en un archivo de texto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-106">To report events, you must first define the events in a message text file.</span></span> <span data-ttu-id="1a1cc-107">Para obtener más información sobre cómo escribir un archivo de texto de mensaje, vea [archivos de texto de mensaje](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="1a1cc-107">For details on writing a message text file, see [Message Text Files](message-text-files.md).</span></span> <span data-ttu-id="1a1cc-108">A continuación se muestra el archivo de texto del mensaje que se usa en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-108">The following shows the message text file used in this example.</span></span>


```C++
; // MyEventProvider.mc 

; // This is the header section.


SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )


FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )

LanguageNames=(English=0x409:MSG00409)


; // The following are the categories of events.

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=NETWORK_CATEGORY
Language=English
Network Events
.

MessageId=0x2
SymbolicName=DATABASE_CATEGORY
Language=English
Database Events
.

MessageId=0x3
SymbolicName=UI_CATEGORY
Language=English
UI Events
.


; // The following are the message definitions.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_INVALID_COMMAND
Language=English
The command is not valid.
.


MessageId=0x101
Severity=Error
Facility=System
SymbolicName=MSG_BAD_FILE_CONTENTS
Language=English
File %1 contains content that is not valid.
.

MessageId=0x102
Severity=Warning
Facility=System
SymbolicName=MSG_RETRIES
Language=English
There have been %1 retries with %2 success! Disconnect from
the server and try again later.
.

MessageId=0x103
Severity=Informational
Facility=System
SymbolicName=MSG_COMPUTE_CONVERSION
Language=English
%1 %%4096 = %2 %%4097. 
.


; // The following are the parameter strings */


MessageId=0x1000
Severity=Success
Facility=System
SymbolicName=QUARTS_UNITS
Language=English
quarts%0
.

MessageId=0x1001
Severity=Success
Facility=System
SymbolicName=GALLONS_UNITS
Language=English
gallons%0
.
```



<span data-ttu-id="1a1cc-109">Para compilar el archivo de texto del mensaje, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="1a1cc-109">To compile the message text file, use the following command:</span></span>

<span data-ttu-id="1a1cc-110">**MC-U provider.mc**</span><span class="sxs-lookup"><span data-stu-id="1a1cc-110">**mc -U provider.mc**</span></span>

<span data-ttu-id="1a1cc-111">Para compilar los recursos generados por el compilador de mensajes, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="1a1cc-111">To compile the resources that the message compiler generated, use the following command:</span></span>

<span data-ttu-id="1a1cc-112">**proveedor RC. RC**</span><span class="sxs-lookup"><span data-stu-id="1a1cc-112">**rc provider.rc**</span></span>

<span data-ttu-id="1a1cc-113">Para crear la DLL solo de recursos que contiene los recursos de la cadena de tabla de mensajes, use el siguiente comando (puede ejecutar el comando desde un símbolo del sistema de Visual Studio):</span><span class="sxs-lookup"><span data-stu-id="1a1cc-113">To create the resource-only DLL that contains the message table string resources, use the following command (you can run the command from a Visual Studio Command Prompt):</span></span>

<span data-ttu-id="1a1cc-114">**Link-dll-NOENTRY Provider. res**</span><span class="sxs-lookup"><span data-stu-id="1a1cc-114">**link -dll -noentry provider.res**</span></span>

<span data-ttu-id="1a1cc-115">A continuación se muestra el archivo de encabezado generado por el compilador para el archivo de texto del mensaje anterior.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-115">The following shows the header file that the compiler generated for the above message text file.</span></span> <span data-ttu-id="1a1cc-116">Incluya el archivo de encabezado en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-116">Include the header file in your project.</span></span>


```C++
// MyEventProvider.mc 
// This is the header section.
// The following are categories of events.
//
//  Values are 32 bit values laid out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: NETWORK_CATEGORY
//
// MessageText:
//
// Network Events
//
#define NETWORK_CATEGORY                 ((WORD)0x00000001L)

//
// MessageId: DATABASE_CATEGORY
//
// MessageText:
//
// Database Events
//
#define DATABASE_CATEGORY                ((WORD)0x00000002L)

//
// MessageId: UI_CATEGORY
//
// MessageText:
//
// UI Events
//
#define UI_CATEGORY                      ((WORD)0x00000003L)

 // The following are message definitions.
//
// MessageId: MSG_INVALID_COMMAND
//
// MessageText:
//
// The command is not valid.
//
#define MSG_INVALID_COMMAND              ((DWORD)0xC0020100L)

//
// MessageId: MSG_BAD_FILE_CONTENTS
//
// MessageText:
//
// File %1 contains content that is not valid.
//
#define MSG_BAD_FILE_CONTENTS            ((DWORD)0xC0000101L)

//
// MessageId: MSG_RETRIES
//
// MessageText:
//
// There have been %1 retries with %2 success! Disconnect from
// the server and try again later.
//
#define MSG_RETRIES                      ((DWORD)0x80000102L)

//
// MessageId: MSG_COMPUTE_CONVERSION
//
// MessageText:
//
// %1 %%4096 = %2 %%4097. 
//
#define MSG_COMPUTE_CONVERSION           ((DWORD)0x40000103L)

 // The following are the parameter strings */
//
// MessageId: QUARTS_UNITS
//
// MessageText:
//
// quarts%0
//
#define QUARTS_UNITS                     ((DWORD)0x00001000L)

//
// MessageId: GALLONS_UNITS
//
// MessageText:
//
// gallons%0
//
#define GALLONS_UNITS                    ((DWORD)0x00001001L)

```



<span data-ttu-id="1a1cc-117">En el ejemplo siguiente se muestra cómo usar la función [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para escribir los eventos definidos en el archivo de texto del mensaje anterior.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-117">The following example shows how to use the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write the events defined in the above message text file.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include "provider.h"

#pragma comment(lib, "advapi32.lib")

#define PROVIDER_NAME L"MyEventProvider"

// Hardcoded insert string for the event messages.
CONST LPWSTR pBadCommand = L"The command that was not valid";
CONST LPWSTR pFilename = L"c:\\folder\\file.ext";
CONST LPWSTR pNumberOfRetries = L"3";
CONST LPWSTR pSuccessfulRetries = L"0";
CONST LPWSTR pQuarts = L"8";
CONST LPWSTR pGallons = L"2";

void wmain(void)
{
    HANDLE hEventLog = NULL;
    LPWSTR pInsertStrings[2] = {NULL, NULL};
    DWORD dwEventDataSize = 0;

    // The source name (provider) must exist as a subkey of Application.
    hEventLog = RegisterEventSource(NULL, PROVIDER_NAME);
    if (NULL == hEventLog)
    {
        wprintf(L"RegisterEventSource failed with 0x%x.\n", GetLastError());
        goto cleanup;
    }

    // This event includes user-defined data as part of the event. The event message
    // does not use insert strings.
    dwEventDataSize = ((DWORD)wcslen(pBadCommand) + 1) * sizeof(WCHAR);
    if (!ReportEvent(hEventLog, EVENTLOG_ERROR_TYPE, UI_CATEGORY, MSG_INVALID_COMMAND, NULL, 0, dwEventDataSize, NULL, pBadCommand))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_INVALID_COMMAND);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pFilename;
    if (!ReportEvent(hEventLog, EVENTLOG_ERROR_TYPE, DATABASE_CATEGORY, MSG_BAD_FILE_CONTENTS, NULL, 1, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_BAD_FILE_CONTENTS);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pNumberOfRetries;
    pInsertStrings[1] = pSuccessfulRetries;
    if (!ReportEvent(hEventLog, EVENTLOG_WARNING_TYPE, NETWORK_CATEGORY, MSG_RETRIES, NULL, 2, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_RETRIES);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pQuarts;
    pInsertStrings[1] = pGallons;
    if (!ReportEvent(hEventLog, EVENTLOG_INFORMATION_TYPE, UI_CATEGORY, MSG_COMPUTE_CONVERSION, NULL, 2, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_COMPUTE_CONVERSION);
        goto cleanup;
    }

    wprintf(L"All events successfully reported.\n");

cleanup:

    if (hEventLog)
        DeregisterEventSource(hEventLog);
}
```



<span data-ttu-id="1a1cc-118">Antes de ejecutar este ejemplo, registre el proveedor en el registro.</span><span class="sxs-lookup"><span data-stu-id="1a1cc-118">Before running this example, register the provider in the registry.</span></span> <span data-ttu-id="1a1cc-119">Para obtener más información sobre la configuración del registro, consulte [orígenes de eventos](event-sources.md).</span><span class="sxs-lookup"><span data-stu-id="1a1cc-119">For details on the registry settings, see [Event Sources](event-sources.md).</span></span> <span data-ttu-id="1a1cc-120">Agregue "MyEventProvider" como una clave del registro en la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="1a1cc-120">Add "MyEventProvider" as a registry key under the following key:</span></span>

<span data-ttu-id="1a1cc-121">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application**</span><span class="sxs-lookup"><span data-stu-id="1a1cc-121">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application**</span></span>

<span data-ttu-id="1a1cc-122">A continuación se muestran los valores del registro que se van a establecer para la clave del registro "MyEventProvider".</span><span class="sxs-lookup"><span data-stu-id="1a1cc-122">The following shows the registry values to set for the "MyEventProvider" registry key.</span></span>

| <span data-ttu-id="1a1cc-123">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="1a1cc-123">Value name</span></span>           | <span data-ttu-id="1a1cc-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a1cc-124">Type</span></span>       | <span data-ttu-id="1a1cc-125">Datos de valor</span><span class="sxs-lookup"><span data-stu-id="1a1cc-125">Value data</span></span>           |
|----------------------|------------|----------------------|
| <span data-ttu-id="1a1cc-126">CategoryCount</span><span class="sxs-lookup"><span data-stu-id="1a1cc-126">CategoryCount</span></span>        | <span data-ttu-id="1a1cc-127">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="1a1cc-127">REG\_DWORD</span></span> | <span data-ttu-id="1a1cc-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1a1cc-128">0x00000003</span></span>           |
| <span data-ttu-id="1a1cc-129">CategoryMessageFile</span><span class="sxs-lookup"><span data-stu-id="1a1cc-129">CategoryMessageFile</span></span>  | <span data-ttu-id="1a1cc-130">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1a1cc-130">REG\_SZ</span></span>    | <span data-ttu-id="1a1cc-131">*ruta de acceso* \\provider.dll</span><span class="sxs-lookup"><span data-stu-id="1a1cc-131">*path*\\provider.dll</span></span> |
| <span data-ttu-id="1a1cc-132">EventMessageFile</span><span class="sxs-lookup"><span data-stu-id="1a1cc-132">EventMessageFile</span></span>     | <span data-ttu-id="1a1cc-133">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1a1cc-133">REG\_SZ</span></span>    | <span data-ttu-id="1a1cc-134">*ruta de acceso* \\provider.dll</span><span class="sxs-lookup"><span data-stu-id="1a1cc-134">*path*\\provider.dll</span></span> |
| <span data-ttu-id="1a1cc-135">ParameterMessageFile</span><span class="sxs-lookup"><span data-stu-id="1a1cc-135">ParameterMessageFile</span></span> | <span data-ttu-id="1a1cc-136">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1a1cc-136">REG\_SZ</span></span>    | <span data-ttu-id="1a1cc-137">*ruta de acceso* \\provider.dll</span><span class="sxs-lookup"><span data-stu-id="1a1cc-137">*path*\\provider.dll</span></span> |
| <span data-ttu-id="1a1cc-138">TypesSupported</span><span class="sxs-lookup"><span data-stu-id="1a1cc-138">TypesSupported</span></span>       | <span data-ttu-id="1a1cc-139">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="1a1cc-139">REG\_DWORD</span></span> | <span data-ttu-id="1a1cc-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="1a1cc-140">0x00000007</span></span>           |



 

 

 



