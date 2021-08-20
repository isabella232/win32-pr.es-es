---
title: Reintentar una suscripción del recopilador de eventos
description: Si se produce un problema con un origen de eventos asociado a una suscripción del recopilador de eventos, puede volver a intentar la suscripción una vez resuelto el problema.
ms.assetid: 8a3570af-bde3-40e5-8129-84ec313d853f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a15d6898fb99bf6b8cbe0e6f26605dec08967382375eb53447ac474466493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937237"
---
# <a name="retrying-an-event-collector-subscription"></a>Reintentar una suscripción del recopilador de eventos

Si se produce un problema con un origen de eventos asociado a una suscripción del recopilador de eventos, puede volver a intentar la suscripción una vez resuelto el problema.

> [!Note]
>
> Puede usar este ejemplo para reintentar una suscripción o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil rs** *SubscriptionName*

 

Necesitará el nombre de una suscripción para volver a intentarlo. Para enumerar los nombres de las suscripciones actuales en un equipo local, puede usar el ejemplo de código de C++ que se muestra en Enumerar suscripciones del recopilador de eventos [o](listing-event-collector-subscriptions.md)puede escribir el siguiente comando en el símbolo del sistema:

**wecutil es**

> [!Note]  
> En este ejemplo se muestra cómo reintentar individualmente cada origen de eventos de una suscripción iniciada por el recopilador y cómo reintentar una suscripción iniciada por el origen.

 

En el ejemplo de código siguiente se sigue un procedimiento para reintentar todos los orígenes de eventos de una suscripción del recopilador de eventos.

**Para volver a intentar una suscripción del recopilador de eventos**

1.  Abra la suscripción proporcionando el nombre de la suscripción y los derechos de acceso como parámetros para la [**función EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) Para obtener más información sobre los derechos de acceso, vea Windows event collector constants (Constantes [**del recopilador de eventos).**](windows-event-collector-constants.md)
2.  Vuelva a intentar el origen del evento llamando a la **función EcRetrySubscription.**
3.  Cierre la suscripción mediante una llamada a la [**función EcClose.**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)

En el siguiente ejemplo de código de C++ se muestra cómo reintentar una suscripción del recopilador de eventos.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Referencia del recopilador de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 




