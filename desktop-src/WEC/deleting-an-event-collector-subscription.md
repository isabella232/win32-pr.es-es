---
title: Eliminar una suscripción del recopilador de eventos
description: Puede eliminar una suscripción del recopilador de eventos de un equipo local.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775667"
---
# <a name="deleting-an-event-collector-subscription"></a>Eliminar una suscripción del recopilador de eventos

Puede eliminar una suscripción del recopilador de eventos de un equipo local. Debe conocer el nombre de la suscripción para poder eliminarla. Para obtener más información acerca de cómo enumerar las suscripciones actuales en un equipo local, vea [enumerar las suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)o escriba el siguiente comando en el símbolo del sistema:

**wecutil es**

> [!Note]
>
> Puede usar este ejemplo para eliminar una suscripción del recopilador de eventos o puede escribir el siguiente comando en el símbolo del sistema:
>
> **wecutil DS** *SubscriptionName*

 

Después de recuperar el nombre de la suscripción del recopilador de eventos que se va a eliminar, puede proporcionar el nombre de la suscripción como un parámetro a [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

En el ejemplo de código de C++ siguiente se muestra cómo eliminar una suscripción del recopilador de eventos.


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

[Enumerar las suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)
</dt> <dt>

[Referencia del recopilador de eventos de Windows](windows-event-collector-reference.md)
</dt> </dl>

 

 




