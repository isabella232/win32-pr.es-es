---
title: Quitar un origen de eventos de una suscripción iniciada por el recopilador
description: Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin eliminar toda la suscripción.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903625"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a><span data-ttu-id="663f7-103">Quitar un origen de eventos de una suscripción iniciada por el recopilador</span><span class="sxs-lookup"><span data-stu-id="663f7-103">Removing an Event Source from a Collector Initiated Subscription</span></span>

<span data-ttu-id="663f7-104">Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin eliminar toda la suscripción.</span><span class="sxs-lookup"><span data-stu-id="663f7-104">You can remove an event source from a collector initiated subscription without deleting the entire subscription.</span></span> <span data-ttu-id="663f7-105">Debe conocer la dirección del origen de eventos que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="663f7-105">You must know the address of the event source that you want to delete.</span></span> <span data-ttu-id="663f7-106">Puede encontrar la dirección de un origen de eventos que está asociada a una suscripción mediante el ejemplo de C++ que se muestra en [Mostrar las propiedades de una suscripción del recopilador de eventos](displaying-the-properties-of-an-event-collector-subscription.md)o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="663f7-106">You can find the address of an event source that is associated to a subscription by using the C++ example shown in [Displaying the Properties of an Event Collector Subscription](displaying-the-properties-of-an-event-collector-subscription.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="663f7-107">**wecutil GS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="663f7-107">**wecutil gs** *SubscriptionName*</span></span>

<span data-ttu-id="663f7-108">Para enumerar las suscripciones actuales en un equipo local, puede utilizar el ejemplo de código de C++ que se muestra en [enumerar las suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="663f7-108">To list the current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="663f7-109">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="663f7-109">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="663f7-110">Puede usar este ejemplo para quitar un origen de eventos de una suscripción iniciada por el Recopilador o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="663f7-110">You can use this example to remove an event source from a collector initiated subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="663f7-111">**wecutil SS** *SubscriptionName*  \* */esa: \* \* \* EventSourceAddress* **/res**</span><span class="sxs-lookup"><span data-stu-id="663f7-111">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/res**</span></span>
>
> <span data-ttu-id="663f7-112">*EventSourceAddress* puede ser localhost para el equipo local o un nombre de dominio completo para un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="663f7-112">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="663f7-113">Este ejemplo sigue una serie de pasos para quitar un origen de eventos de una suscripción iniciada por el recopilador.</span><span class="sxs-lookup"><span data-stu-id="663f7-113">This example follows a series of steps to remove an event source from a collector-initiated subscription.</span></span>

<span data-ttu-id="663f7-114">**Para quitar un origen de eventos de una suscripción iniciada por el recopilador**</span><span class="sxs-lookup"><span data-stu-id="663f7-114">**To remove an event source from a collector-initiated subscription**</span></span>

1.  <span data-ttu-id="663f7-115">Para abrir la suscripción existente, proporcione el nombre y los derechos de acceso de la suscripción como parámetros para la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="663f7-115">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="663f7-116">Para obtener más información sobre los derechos de acceso, consulte [**constantes del recopilador de eventos de Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="663f7-116">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="663f7-117">Obtiene la matriz de orígenes de eventos de la suscripción mediante una llamada a la función [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="663f7-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="663f7-118">Para obtener más información sobre las propiedades de suscripción que se pueden recuperar, consulte la enumeración de [**identificador de propiedad de suscripción de EC \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="663f7-118">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="663f7-119">Busque el origen de eventos especificado en la matriz de orígenes de eventos de la suscripción mediante una llamada a la función [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) .</span><span class="sxs-lookup"><span data-stu-id="663f7-119">Search for the specified event source in the event sources array of the subscription by calling the [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) function.</span></span> <span data-ttu-id="663f7-120">El valor de la propiedad **EcSubscriptionEventSourceAddress** será localhost para el equipo local o será un nombre de dominio completo para un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="663f7-120">The value of the **EcSubscriptionEventSourceAddress** property will be either Localhost for the local computer or will be a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="663f7-121">Para obtener más información sobre las propiedades de origen de eventos que se pueden recuperar, vea la enumeración ID. de **\_ propiedad de suscripción de \_ \_ EC** .</span><span class="sxs-lookup"><span data-stu-id="663f7-121">For more information about event source properties that can be retrieved, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
4.  <span data-ttu-id="663f7-122">Elimine el origen de eventos de la suscripción mediante una llamada a la función [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) .</span><span class="sxs-lookup"><span data-stu-id="663f7-122">Delete the event source from the subscription by calling the [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) function.</span></span>
5.  <span data-ttu-id="663f7-123">Guarde la suscripción mediante una llamada a la función [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="663f7-123">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="663f7-124">Cierre la suscripción mediante una llamada a la función [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="663f7-124">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="663f7-125">En el ejemplo de código de C++ siguiente se muestra cómo quitar un origen de eventos de una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="663f7-125">The following C++ code example shows how to remove an event source from an Event Collector subscription.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="663f7-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="663f7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663f7-127">Mostrar las propiedades de una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="663f7-127">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="663f7-128">Enumerar las suscripciones del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="663f7-128">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="663f7-129">Referencia del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="663f7-129">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




