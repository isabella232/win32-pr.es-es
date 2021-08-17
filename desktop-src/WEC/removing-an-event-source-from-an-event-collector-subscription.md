---
title: Quitar un origen de eventos de una suscripción iniciada por el recopilador
description: Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin eliminar toda la suscripción.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e155e4d8467722e9ac5eae04189ed3ba8333f65ec162ffb50f6b9268cf8a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751046"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a>Quitar un origen de eventos de una suscripción iniciada por el recopilador

Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin eliminar toda la suscripción. Debe conocer la dirección del origen del evento que desea eliminar. Puede encontrar la dirección de un origen de eventos asociado a una suscripción mediante el ejemplo de C++ que se muestra en [Mostrar](displaying-the-properties-of-an-event-collector-subscription.md)las propiedades de una suscripción del recopilador de eventos, o puede escribir el siguiente comando en el símbolo del sistema:

**wecutil gs** *SubscriptionName*

Para enumerar las suscripciones actuales en un equipo local, puede usar el ejemplo de código de C++ que se muestra en Enumerar suscripciones del recopilador de eventos [o](listing-event-collector-subscriptions.md)puede escribir el siguiente comando en el símbolo del sistema:

**wecutil es**

> [!Note]
>
> Puede usar este ejemplo para quitar un origen de eventos de una suscripción iniciada por el recopilador o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil ss** *SubscriptionName* **/esa:**_EventSourceAddress_ **/res**
>
> *EventSourceAddress* puede ser localhost para el equipo local o un nombre de dominio completo para un equipo remoto.

 

Este ejemplo sigue una serie de pasos para quitar un origen de eventos de una suscripción iniciada por el recopilador.

**Para quitar un origen de eventos de una suscripción iniciada por el recopilador**

1.  Abra la suscripción existente proporcionando el nombre de la suscripción y los derechos de acceso como parámetros para la [**función EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) Para obtener más información sobre los derechos de acceso, [**vea Windows Event Collector Constants**](windows-event-collector-constants.md).
2.  Obtenga la matriz de orígenes de eventos de la suscripción mediante una llamada a la [**función EcGetSubscriptionProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) Para obtener más información sobre las propiedades de suscripción que se pueden recuperar, vea la [**\_ enumeración EC SUBSCRIPTION \_ PROPERTY \_ ID.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)
3.  Busque el origen de eventos especificado en la matriz de orígenes de eventos de la suscripción llamando a la [**función EcGetObjectArrayProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) El valor de la **propiedad EcSubscriptionEventSourceAddress** será Localhost para el equipo local o será un nombre de dominio completo para un equipo remoto. Para obtener más información sobre las propiedades de origen de eventos que se pueden recuperar, vea la **enumeración EC \_ SUBSCRIPTION PROPERTY \_ \_ ID.**
4.  Elimine el origen del evento de la suscripción mediante una llamada a [**la función EcRemoveObjectArrayElement.**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
5.  Guarde la suscripción mediante una llamada a [**la función EcSaveSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
6.  Cierre la suscripción mediante una llamada a la [**función EcClose.**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)

En el siguiente ejemplo de código de C++ se muestra cómo quitar un origen de eventos de una suscripción del recopilador de eventos.


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
    Cleanup:
        if (hArray)
            EcClose(hArray);
        if (hSubscription)
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

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
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

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
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
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mostrar las propiedades de una suscripción del recopilador de eventos](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[Enumerar suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Referencia del recopilador de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 




