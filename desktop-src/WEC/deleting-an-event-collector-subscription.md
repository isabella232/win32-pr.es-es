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
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="97402-103">Eliminar una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="97402-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="97402-104">Puede eliminar una suscripción del recopilador de eventos de un equipo local.</span><span class="sxs-lookup"><span data-stu-id="97402-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="97402-105">Debe conocer el nombre de la suscripción para poder eliminarla.</span><span class="sxs-lookup"><span data-stu-id="97402-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="97402-106">Para obtener más información acerca de cómo enumerar las suscripciones actuales en un equipo local, vea [enumerar las suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)o escriba el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="97402-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="97402-107">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="97402-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="97402-108">Puede usar este ejemplo para eliminar una suscripción del recopilador de eventos o puede escribir el siguiente comando en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="97402-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="97402-109">**wecutil DS** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="97402-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="97402-110">Después de recuperar el nombre de la suscripción del recopilador de eventos que se va a eliminar, puede proporcionar el nombre de la suscripción como un parámetro a [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span><span class="sxs-lookup"><span data-stu-id="97402-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="97402-111">En el ejemplo de código de C++ siguiente se muestra cómo eliminar una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="97402-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="97402-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97402-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97402-113">Enumerar las suscripciones del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="97402-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="97402-114">Referencia del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="97402-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




