---
title: Volver a intentar una suscripción del recopilador de eventos
description: Si se produce un problema con un origen de eventos que está asociado a una suscripción del recopilador de eventos, puede volver a intentar la suscripción una vez que se haya resuelto el problema.
ms.assetid: 8a3570af-bde3-40e5-8129-84ec313d853f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0f29d485d36bb6f623cb67bd3e8598c4bb46b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777731"
---
# <a name="retrying-an-event-collector-subscription"></a><span data-ttu-id="698f0-103">Volver a intentar una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="698f0-103">Retrying an Event Collector Subscription</span></span>

<span data-ttu-id="698f0-104">Si se produce un problema con un origen de eventos que está asociado a una suscripción del recopilador de eventos, puede volver a intentar la suscripción una vez que se haya resuelto el problema.</span><span class="sxs-lookup"><span data-stu-id="698f0-104">If a problem occurs with an event source that is associated to an Event Collector subscription, you can retry the subscription after the problem has been solved.</span></span>

> [!Note]
>
> <span data-ttu-id="698f0-105">Puede usar este ejemplo para volver a intentar una suscripción o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="698f0-105">You can use this example to retry a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="698f0-106">**wecutil RS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="698f0-106">**wecutil rs** *SubscriptionName*</span></span>

 

<span data-ttu-id="698f0-107">Necesitará el nombre de una suscripción para volver a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="698f0-107">You will need the name of a subscription to retry it.</span></span> <span data-ttu-id="698f0-108">Para enumerar los nombres de las suscripciones actuales en un equipo local, puede utilizar el ejemplo de código de C++ que se muestra en [enumerar las suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="698f0-108">To list the names of current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="698f0-109">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="698f0-109">**wecutil es**</span></span>

> [!Note]  
> <span data-ttu-id="698f0-110">En este ejemplo se muestra cómo Reintentar individualmente cada origen de eventos de una suscripción iniciada por el recopilador y cómo Reintentar una suscripción iniciada por el origen.</span><span class="sxs-lookup"><span data-stu-id="698f0-110">This example shows how to individually retry each event source of a collector initiated subscription and how to retry a source initiated subscription.</span></span>

 

<span data-ttu-id="698f0-111">En el ejemplo de código siguiente se sigue un procedimiento para Reintentar todos los orígenes de eventos de una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="698f0-111">The following code example follows a procedure to retry all of the event sources of an Event Collector subscription.</span></span>

<span data-ttu-id="698f0-112">**Para volver a intentar una suscripción del recopilador de eventos**</span><span class="sxs-lookup"><span data-stu-id="698f0-112">**To retry an Event Collector subscription**</span></span>

1.  <span data-ttu-id="698f0-113">Abra la suscripción proporcionando el nombre de la suscripción y los derechos de acceso como parámetros a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="698f0-113">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="698f0-114">Para obtener más información sobre los derechos de acceso, consulte [**constantes del recopilador de eventos de Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="698f0-114">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="698f0-115">Vuelva a intentar el origen del evento llamando a la función **EcRetrySubscription** .</span><span class="sxs-lookup"><span data-stu-id="698f0-115">Retry the event source by calling the **EcRetrySubscription** function.</span></span>
3.  <span data-ttu-id="698f0-116">Cierre la suscripción mediante una llamada a la función [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="698f0-116">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="698f0-117">En el ejemplo de código de C++ siguiente se muestra cómo Reintentar una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="698f0-117">The following C++ code example shows how to retry an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetStatus(LPCWSTR subscriptionName, 
    LPCWSTR eventSource, 
    EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID statusInfoID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vStatus);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal, dwEventSourceCount;
    EC_HANDLE hSubscription;
    PEC_VARIANT vProperty, vEventSources;
    std::vector<BYTE> buffer, eventSourceBuffer;
    LPCWSTR lpSubname = L"SourceInit";

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS,
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Determine if the subscription is source initiated or
    // collector initiated.
    dwRetVal = GetProperty(hSubscription,
        EcSubscriptionType,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal){
        goto Cleanup;
    }

    if( vProperty->Type != EcVarTypeNull && vProperty->Type != EcVarTypeUInt32)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if( vProperty->UInt32Val == EcSubscriptionTypeSourceInitiated)
    {
        // Retry the subscription (event source parameter is NULL,
        // so the entire subscription is retried).
        if (!EcRetrySubscription(lpSubname, NULL, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
        wprintf(L"\nThe subscription was retried.\n");
    }
    else if ( vProperty->UInt32Val == EcSubscriptionTypeCollectorInitiated)
    {
        // Get the event sources array to retry each event source.
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
        
        for (DWORD I = 0; I < dwEventSourceCount ; I++)
        {
            LPCWSTR eventSource = vEventSources->StringArr[I];

            if (!eventSource)
                continue;

            // Retry the event source.
            if (!EcRetrySubscription(lpSubname, eventSource, 0))
            {
                dwRetVal =  GetLastError();
                goto Cleanup;
            }
            
        }
        wprintf(L"\nEach event source was retried.\n");
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

DWORD GetProperty(EC_HANDLE hSubscription,
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
        return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0], 
        &dwBufferSize))
    {
        dwRetVal = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
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
```



## <a name="related-topics"></a><span data-ttu-id="698f0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="698f0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="698f0-119">Enumerar las suscripciones del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="698f0-119">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="698f0-120">Referencia del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="698f0-120">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




