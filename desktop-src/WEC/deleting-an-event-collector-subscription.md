---
title: Eliminación de una suscripción del recopilador de eventos
description: Puede eliminar una suscripción del recopilador de eventos desde un equipo local.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006095"
---
# <a name="deleting-an-event-collector-subscription"></a>Eliminación de una suscripción del recopilador de eventos

Puede eliminar una suscripción del recopilador de eventos desde un equipo local. Debe conocer el nombre de la suscripción para poder eliminarla. Para obtener más información sobre cómo enumerar las suscripciones actuales en un equipo local, vea [Enumerar](listing-event-collector-subscriptions.md)suscripciones del recopilador de eventos o escriba el siguiente comando en el símbolo del sistema:

**wecutil es**

> [!Note]
>
> Puede usar este ejemplo para eliminar una suscripción del recopilador de eventos o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil ds** *SubscriptionName*

 

Después de recuperar el nombre de la suscripción del recopilador de eventos que se va a eliminar, puede proporcionar el nombre de la suscripción como parámetro a [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

En el siguiente ejemplo de código de C++ se muestra cómo eliminar una suscripción del recopilador de eventos.


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Referencia del recopilador de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 




