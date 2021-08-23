---
title: Enumerar suscripciones del recopilador de eventos
description: Puede recuperar una lista de nombres de suscripciones del Recopilador de eventos que están habilitadas en un equipo local.
ms.assetid: b44fc694-b94a-4fc5-95d1-72afb016ad72
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f67e888ba62b225603cd47293936b7010ce9f730238119d2b5d36ca9ed6dbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997925"
---
# <a name="listing-event-collector-subscriptions"></a>Enumerar suscripciones del recopilador de eventos

Puede recuperar una lista de nombres de suscripciones del Recopilador de eventos que están habilitadas en un equipo local. Con la [**función EcOpenSubscriptionEnum,**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum) puede obtener un identificador para un enumerador de suscripciones. Una vez creado el identificador, se [**usa la función EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription) para enumerar las suscripciones en el equipo local.

> [!Note]
>
> Puede usar el siguiente ejemplo de código para recuperar una lista de suscripciones o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil es**

 

En el siguiente ejemplo de código de C++ se muestra cómo enumerar las suscripciones del recopilador de eventos.


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    // Lists the Event Collector subscriptions that are available 
    // on the local computer.
    DWORD dwBufferSizeUsed, dwError = ERROR_SUCCESS;
    BOOL bRetVal = true;
    std::vector<WCHAR> buffer(MAX_PATH);
    EC_HANDLE hEnumerator;
    DWORD dwRetVal;

    // Create a handle to access the subscriptions.
    hEnumerator = EcOpenSubscriptionEnum(NULL);

    if (hEnumerator)
    {
        while (bRetVal)
        {
            // Get the next subscription.
            bRetVal = EcEnumNextSubscription(hEnumerator, 
                (DWORD) buffer.size(),
                (LPWSTR) &buffer[0],
                &dwBufferSizeUsed);
            dwError = GetLastError();

            // If the buffer is not large enough, resize it to accommodate the
            // subscription information.
            if (!bRetVal && ERROR_INSUFFICIENT_BUFFER == dwError)
            {
                dwError = ERROR_SUCCESS;
                buffer.resize(dwBufferSizeUsed);

                bRetVal = EcEnumNextSubscription(hEnumerator,
                    (DWORD) buffer.size(),
                    (LPWSTR) &buffer[0],
                    &dwBufferSizeUsed);
                dwError = GetLastError();
            }

            if (!bRetVal && ERROR_NO_MORE_ITEMS == dwError)
            {
                dwError = ERROR_SUCCESS;
                break;
            }

            if (bRetVal && ERROR_SUCCESS != dwError)
            {
                break;
            }
            
            // Output the subscription name.
            wprintf(L"%s\n", (LPCWSTR) &buffer[0]);    
        }
    }
    else
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u. Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\nError Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }

    EcClose(hEnumerator);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia del recopilador de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 




