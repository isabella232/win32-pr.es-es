---
title: Enumeraciones (infraestructura del mismo nivel)
description: Mediante el uso de enumeraciones, puede obtener una lista de todas las entidades del mismo nivel específicas que coincidan con los criterios.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667440"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="30eac-103">Enumeraciones (infraestructura del mismo nivel)</span><span class="sxs-lookup"><span data-stu-id="30eac-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="30eac-104">Mediante el uso de enumeraciones, puede obtener una lista de todas las entidades del mismo nivel específicas que coincidan con los criterios.</span><span class="sxs-lookup"><span data-stu-id="30eac-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="30eac-105">**Para obtener una enumeración y recuperar los resultados**</span><span class="sxs-lookup"><span data-stu-id="30eac-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="30eac-106">Obtener un identificador de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="30eac-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="30eac-107">Llame a una función **PeerEnum** , por ejemplo, llame a la función de gráficos del mismo nivel de [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) .</span><span class="sxs-lookup"><span data-stu-id="30eac-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="30eac-108">Las funciones **PeerEnum** crean la enumeración y devuelven un identificador a esa enumeración a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="30eac-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="30eac-109">Este identificador debe usarse para recuperar los resultados.</span><span class="sxs-lookup"><span data-stu-id="30eac-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="30eac-110">Opcionalmente, obtenga el número de entidades en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="30eac-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="30eac-111">Llame a una función **GetItemCount** , por ejemplo, llame a [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) o [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span><span class="sxs-lookup"><span data-stu-id="30eac-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="30eac-112">Puede usar el valor devuelto por la función **GetItemCount** para determinar el número de elementos disponibles para recuperar.</span><span class="sxs-lookup"><span data-stu-id="30eac-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="30eac-113">Recupera un grupo de resultados.</span><span class="sxs-lookup"><span data-stu-id="30eac-113">Retrieve a group of results.</span></span> <span data-ttu-id="30eac-114">Llame a una función **GetNextItem** , por ejemplo, llame a [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span><span class="sxs-lookup"><span data-stu-id="30eac-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="30eac-115">Cuando una aplicación llama a una función **GetNextItem** , especifica el número de entidades que se van a devolver y, a continuación, la función devuelve un puntero a una matriz de punteros a las entidades y el número de entidades, que es siempre menor o igual que el número especificado.</span><span class="sxs-lookup"><span data-stu-id="30eac-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="30eac-116">Es posible que una aplicación necesite llamar a esta función muchas veces, hasta que el número de entidades devueltas sea menor que el número solicitado.</span><span class="sxs-lookup"><span data-stu-id="30eac-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="30eac-117">Después de que no se necesiten los datos, libere el puntero a los datos.</span><span class="sxs-lookup"><span data-stu-id="30eac-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="30eac-118">Llame a una función **FreeData** , por ejemplo, llame a [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="30eac-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="30eac-119">Para obtener más información, vea [liberar datos del mismo nivel](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="30eac-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="30eac-120">Después de que la aplicación no necesite el identificador de la enumeración, suéltelo.</span><span class="sxs-lookup"><span data-stu-id="30eac-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="30eac-121">Llame a una función **EndEnumeration** , por ejemplo, llame a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) o [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span><span class="sxs-lookup"><span data-stu-id="30eac-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="30eac-122">Ejemplo de una enumeración</span><span class="sxs-lookup"><span data-stu-id="30eac-122">Example of an Enumeration</span></span>

<span data-ttu-id="30eac-123">El siguiente fragmento de código muestra cómo enumerar a través de identidades disponibles.</span><span class="sxs-lookup"><span data-stu-id="30eac-123">The following code snippet shows you how to enumerate through available identities.</span></span>


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



