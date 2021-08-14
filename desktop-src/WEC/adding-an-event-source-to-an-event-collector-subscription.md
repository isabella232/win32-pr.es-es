---
title: Agregar un origen de eventos a una suscripción iniciada por el recopilador
description: Para recibir un evento reenviado de una suscripción de eventos, puede crear una suscripción iniciada por el recopilador en el equipo local.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905dd9b5a250f9ab12397f851f79a8374c6847235acb34013972dea445f3622b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344224"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Agregar un origen de eventos a una suscripción iniciada por el recopilador

Para recibir un evento reenviado de una suscripción de eventos, puede crear una suscripción iniciada por el recopilador en el equipo local. Para obtener más información sobre cómo crear una suscripción iniciada por el recopilador, vea el ejemplo de código de C++ que se muestra en [Creación de una suscripción del recopilador de eventos](creating-an-event-collector-subscription.md).

Una vez creada una suscripción iniciada por el recopilador, puede agregar orígenes de eventos a la suscripción. Debe agregar al menos un origen de eventos a una suscripción para recopilar eventos.

> [!Note]
>
> Puede usar este ejemplo de código para agregar un origen de eventos a una suscripción o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil ss** *SubscriptionName* **/esa:**_EventSourceAddress_ **/aes /ese**
>
> *EventSourceAddress* puede ser localhost para el equipo local o un nombre de dominio completo para un equipo remoto.

 

Para obtener más información sobre cómo agregar orígenes de eventos a una suscripción iniciada por el origen, vea [Configurar una suscripción iniciada por origen.](setting-up-a-source-initiated-subscription.md)

Este ejemplo sigue una serie de pasos para agregar un origen de eventos a una suscripción iniciada por el recopilador.

**Para agregar un origen de eventos a una suscripción iniciada por el recopilador**

1.  Abra la suscripción existente proporcionando el nombre de la suscripción y los derechos de acceso como parámetros para la [**función EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) Para obtener más información sobre los derechos de acceso, vea Windows event collector constants (Constantes [**del recopilador de eventos).**](windows-event-collector-constants.md)
2.  Obtenga la matriz de orígenes de eventos de la suscripción mediante una llamada a la [**función EcGetSubscriptionProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) Para obtener más información sobre las propiedades de suscripción que se pueden recuperar, vea la [**\_ enumeración EC SUBSCRIPTION \_ PROPERTY \_ ID.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)
3.  Agregue un nuevo origen de eventos a la matriz de orígenes de eventos de la suscripción mediante una llamada a la [**función EcInsertObjectArrayElement.**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
4.  Establezca las propiedades de origen del evento llamando a la [**función EcSetObjectArrayProperty.**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) La **propiedad EcSubscriptionEventSourceAddress** se establece en una dirección para el equipo local (Localhost) o en un nombre de dominio completo para un equipo remoto. Para obtener más información sobre las propiedades de origen de eventos que se pueden establecer, vea la **\_ enumeración EC SUBSCRIPTION \_ PROPERTY \_ ID.**
5.  Guarde la suscripción mediante una llamada a [**la función EcSaveSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
6.  Cierre la suscripción mediante una llamada a la [**función EcClose.**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)

En el siguiente ejemplo de código de C++ se muestra cómo agregar un origen de eventos a una suscripción iniciada por el recopilador:


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
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
                &dwBufferSize) )
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

[Configurar equipos para reenviar y recopilar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Creación de una suscripción del recopilador de eventos](creating-an-event-collector-subscription.md)
</dt> <dt>

[Windows Referencia del recopilador de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 