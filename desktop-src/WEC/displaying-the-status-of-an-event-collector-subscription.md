---
title: Mostrar el estado de una suscripción del recopilador de eventos
description: Puede mostrar el estado de una suscripción del recopilador de eventos. El estado incluye la disponibilidad de la suscripción, el último error que se produjo para la suscripción, la hora del último error y la próxima vez que se vuelva a intentar la suscripción.
ms.assetid: e1c3c3ed-2f7c-433d-a51d-66c2abd2e961
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7c806d72d4945e2e45384b91bc94fbef3ed08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357037"
---
# <a name="displaying-the-status-of-an-event-collector-subscription"></a><span data-ttu-id="49241-104">Mostrar el estado de una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="49241-104">Displaying the Status of an Event Collector Subscription</span></span>

<span data-ttu-id="49241-105">Puede mostrar el estado de una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="49241-105">You can display the status of an Event Collector subscription.</span></span> <span data-ttu-id="49241-106">El estado incluye la disponibilidad de la suscripción, el último error que se produjo para la suscripción, la hora del último error y la próxima vez que se vuelva a intentar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="49241-106">The status includes the availability of the subscription, the last error that occurred for the subscription, the time of the last error, and the next time the subscription will be retried.</span></span>

> [!Note]
>
> <span data-ttu-id="49241-107">Puede usar este ejemplo para mostrar el estado de una suscripción o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="49241-107">You can use this example to display the status of a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="49241-108">**wecutil gr** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="49241-108">**wecutil gr** *SubscriptionName*</span></span>

 

<span data-ttu-id="49241-109">Necesitará el nombre de una suscripción para mostrar su estado.</span><span class="sxs-lookup"><span data-stu-id="49241-109">You will need the name of a subscription to display its status.</span></span> <span data-ttu-id="49241-110">Para enumerar los nombres de las suscripciones actuales en un equipo local, puede usar el ejemplo de C++ de que se muestra en [enumerar suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="49241-110">To list the names of current subscriptions on a local computer, you can use the C++ example in shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="49241-111">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="49241-111">**wecutil es**</span></span>

<span data-ttu-id="49241-112">En el ejemplo siguiente se sigue un procedimiento para mostrar el estado de una suscripción del recopilador de eventos:</span><span class="sxs-lookup"><span data-stu-id="49241-112">The following example follows a procedure to display the status of an Event Collector subscription:</span></span>

<span data-ttu-id="49241-113">**Para mostrar el estado de una suscripción del recopilador de eventos**</span><span class="sxs-lookup"><span data-stu-id="49241-113">**To display the status of an Event Collector subscription**</span></span>

1.  <span data-ttu-id="49241-114">Abra la suscripción proporcionando el nombre de la suscripción y los derechos de acceso como parámetros a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="49241-114">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="49241-115">Para obtener más información sobre los derechos de acceso, consulte [**constantes del recopilador de eventos de Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="49241-115">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="49241-116">Obtenga el estado de la suscripción mediante una llamada a la función [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) (no especifique un origen de eventos al llamar a la función).</span><span class="sxs-lookup"><span data-stu-id="49241-116">Get the status of the subscription by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function (do not specify an event source when calling the function).</span></span>
3.  <span data-ttu-id="49241-117">Obtenga la matriz de orígenes de eventos de la suscripción mediante una llamada a la función [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) y pasando la marca EcSubscriptionRunTimeStatusEventSources.</span><span class="sxs-lookup"><span data-stu-id="49241-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function and passing in the EcSubscriptionRunTimeStatusEventSources flag.</span></span>
4.  <span data-ttu-id="49241-118">Para obtener la información de estado de cada origen de eventos, llame a la función [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) y pase el nombre del origen del evento.</span><span class="sxs-lookup"><span data-stu-id="49241-118">Get the status information for each event source by calling the [**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus) function and passing in the event source name.</span></span> <span data-ttu-id="49241-119">Para obtener más información sobre la información de estado que se puede recuperar, consulte la enumeración de ID. de [**información de estado de tiempo de ejecución de suscripción de EC \_ \_ \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id) .</span><span class="sxs-lookup"><span data-stu-id="49241-119">For more information about the status information that can be retrieved, see the [**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id) enumeration.</span></span>
5.  <span data-ttu-id="49241-120">Imprime la información de estado de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="49241-120">Print the status information for the subscription.</span></span>
6.  <span data-ttu-id="49241-121">Cierre la suscripción mediante una llamada a la función [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="49241-121">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="49241-122">En el ejemplo de código de C++ siguiente se muestra cómo mostrar el estado de una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="49241-122">The following C++ code example shows how to display the status of an Event Collector subscription.</span></span>


```C++
#include <iostream>
using namespace std;
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Track Runtime Status
typedef struct _RUNTIME_STATUS
{
    std::wstring ActiveStatus;
    DWORD LastError;
    std::wstring LastErrorMessage;
    std::wstring NextRetryTime;

} RUNTIME_STATUS;

// Subscription Information

DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus);

std::wstring ConvertEcDateTime( ULONGLONG code );



void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwEventSourceCount, dwRetVal = ERROR_SUCCESS;
    std::vector<BYTE> buffer;
    std::vector<BYTE> eventSourceBuffer;
    std::vector<BYTE>::iterator sourceNameIterator;
    PEC_VARIANT vStatus, vEventSources;
    EC_HANDLE hSubscription;
    LPCWSTR lpSubname = L"TestSubscription";
    RUNTIME_STATUS runtimeStatus;
    std::wstring eventSource;

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(lpSubname, 
        EC_READ_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the status values for the entire subscription.
    dwRetVal = GetStatus(lpSubname, NULL, 
        EcSubscriptionRunTimeStatusActive,
        0,
        buffer,
        vStatus);
    if (ERROR_SUCCESS != dwRetVal) {
        goto Cleanup;
    }
    wprintf(L"\nEvent Subscription: %s\n",  lpSubname);
    
    // Convert the status value to text.
    switch (vStatus->UInt32Val)
    {
        case EcRuntimeStatusActiveStatusActive:
            runtimeStatus.ActiveStatus = L"Active";
            break;
        case EcRuntimeStatusActiveStatusDisabled:
            runtimeStatus.ActiveStatus = L"Disabled";
            break;
        case EcRuntimeStatusActiveStatusInactive:
            runtimeStatus.ActiveStatus = L"Inactive";
            break;
        case EcRuntimeStatusActiveStatusTrying:
            runtimeStatus.ActiveStatus = L"Trying";
            break;
        default:
            runtimeStatus.ActiveStatus = L"Unknown Status";
        break;
    }
    wprintf(L"Runtime Status: %s\n", runtimeStatus.ActiveStatus.c_str());
    
    dwRetVal = GetStatus(lpSubname, NULL, 
        EcSubscriptionRunTimeStatusLastError,
        0,
        buffer,
        vStatus);
    if (ERROR_SUCCESS != dwRetVal) {
        goto Cleanup;
    }
    wprintf(L"Last Error: %u\n", vStatus->UInt32Val);
        
    

    // Step 2: Get the event sources array to query for event source status.
    dwRetVal = GetStatus(lpSubname, NULL, 
        EcSubscriptionRunTimeStatusEventSources, 
        0,
        eventSourceBuffer, 
        vEventSources);
    if (ERROR_SUCCESS != dwRetVal){
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vEventSources->Type != EcVarTypeNull && 
        vEventSources->Type != (EcVarTypeString | EC_VARIANT_TYPE_ARRAY) )
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    dwEventSourceCount = vEventSources->Count;
    
    // Step 3: Get the status of each event source.
    for (DWORD I = 0; I < dwEventSourceCount ; I++)
    {
        eventSource = vEventSources->StringArr[I];

        // Get the status of the subscription event source.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(),
            EcSubscriptionRunTimeStatusActive, 
            0, 
            buffer, 
            vStatus);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeUInt32)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }

        // Convert the status value to text.
        switch (vStatus->UInt32Val)
        {
            case EcRuntimeStatusActiveStatusActive:
                runtimeStatus.ActiveStatus = L"Active";
                break;
            case EcRuntimeStatusActiveStatusDisabled:
                runtimeStatus.ActiveStatus = L"Disabled";
                break;
            case EcRuntimeStatusActiveStatusInactive:
                runtimeStatus.ActiveStatus = L"Inactive";
                break;
            case EcRuntimeStatusActiveStatusTrying:
                runtimeStatus.ActiveStatus = L"Trying";
                break;
            default:
                runtimeStatus.ActiveStatus = L"Unknown Status";
            break;
        }

        // Get the last error that occurred for the subscription.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusLastError, 
            0, 
            buffer, 
            vStatus);
        if(ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeUInt32)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
        
        runtimeStatus.LastError = vStatus->UInt32Val;

        // Get the error message for the last error.
        dwRetVal = GetStatus(lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusLastErrorMessage, 
            0, 
            buffer, 
            vStatus);

        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
        if (vStatus->Type != EcVarTypeNull && vStatus->Type != EcVarTypeString)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
          
        if (vStatus->Type != EcVarTypeNull)
        {
            runtimeStatus.LastErrorMessage = vStatus->StringVal;
        }
        else
        {
            runtimeStatus.LastErrorMessage = L"";
        }

        // Get the time when the subscription will be retried.
        dwRetVal = GetStatus( lpSubname, 
            eventSource.c_str(), 
            EcSubscriptionRunTimeStatusNextRetryTime, 
            0, 
            buffer, 
            vStatus);

        if( ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }
         
        if (vStatus->Type != EcVarTypeNull && vStatus->Type != EcVarTypeDateTime)
        {
            dwRetVal = ERROR_INVALID_DATA;
            goto Cleanup;
        }
          
        if( vStatus->Type != EcVarTypeNull)
        {
            runtimeStatus.NextRetryTime = ConvertEcDateTime(vStatus->DateTimeVal);
        }
        else
        {
            runtimeStatus.NextRetryTime = L"";
        }

        // Step 4: Print the status information.
        wprintf(L"\nEventSource[%u]\n",  I);
        wprintf(L"    Address: %s\n", eventSource.c_str());
        wprintf(L"    Runtime Status: %s\n", runtimeStatus.ActiveStatus.c_str());
        wprintf(L"    Last Error: %u\n", runtimeStatus.LastError);
         
        if( 0 != runtimeStatus.LastError )
        {
            wprintf(L"    Last Error Message: %s\n", runtimeStatus.LastErrorMessage.c_str());
        }
        else
        {
            wprintf(L"    Last Error Message: No Error\n");
        }
         
        wprintf(L"    Next Retry Time: %s\n", runtimeStatus.NextRetryTime.c_str());
    }

    Cleanup:

       // Step 5: Close the subscription.
       if(hSubscription)
           EcClose(hSubscription);
   
       if (dwRetVal != ERROR_SUCCESS)
       {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

// Get the information for the specified EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus)
{
    DWORD dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.clear();
    buffer.resize(sizeof(EC_VARIANT));
    
    if ( !EcGetSubscriptionRunTimeStatus( subscriptionName,
        statusInfoID,
        eventSource,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT) &buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if( ERROR_INSUFFICIENT_BUFFER ==  dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);
            if(!EcGetSubscriptionRunTimeStatus( subscriptionName,
                statusInfoID,
                eventSource,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT) &buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if ( ERROR_SUCCESS == dwRetVal)
    {
        vStatus = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vStatus = NULL;
    }

    return dwRetVal;
}

std::wstring ConvertEcDateTime( ULONGLONG code )
{
    FILETIME ft;
    SYSTEMTIME utcTime;
    SYSTEMTIME localTime; 
    std::wstring timeString;
    std::vector<WCHAR> buffer(30);

    timeString = L"Error- Failed to Convert Date Time to String";

    ft.dwHighDateTime = (DWORD)((code >> 32) & 0xFFFFFFFF);
    ft.dwLowDateTime = (DWORD)(code & 0xFFFFFFFF);

    if( !FileTimeToSystemTime( &ft, &utcTime) )
    {
        return timeString;
    }

    if(!SystemTimeToTzSpecificLocalTime(NULL, &utcTime, &localTime))
    {
        return timeString;
    }

    HRESULT hr = StringCchPrintfW((LPWSTR) &buffer[0], 
        buffer.size(), 
        L"%4.4hd-%2.2hd-%2.2hdT%2.2hd:%2.2hd:%2.2hd.%3.3hdZ",
        localTime.wYear,
        localTime.wMonth,
        localTime.wDay,
        localTime.wHour,
        localTime.wMinute,
        localTime.wSecond,
        localTime.wMilliseconds);

    if (FAILED(hr)) 
    {
        return timeString;
    }

    timeString = (LPWSTR) &buffer[0];

    return timeString;
}
```



## <a name="related-topics"></a><span data-ttu-id="49241-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49241-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49241-124">Enumerar las suscripciones del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="49241-124">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="49241-125">Referencia del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="49241-125">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




