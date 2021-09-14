---
title: Enumeraciones (infraestructura del mismo nivel)
description: Mediante enumeraciones, puede obtener una lista de todas las entidades del mismo nivel específicas que coincidan con sus criterios.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073926"
---
# <a name="enumerations-peer-infrastructure"></a>Enumeraciones (infraestructura del mismo nivel)

Mediante enumeraciones, puede obtener una lista de todas las entidades del mismo nivel específicas que coincidan con sus criterios.

**Para obtener una enumeración y recuperar los resultados**

1.  Obtenga un identificador para la enumeración . Llame a **una función PeerEnum,** por ejemplo, llame a la [**función PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing. Las **funciones PeerEnum** crean la enumeración y devuelven un identificador a esa enumeración a la aplicación que realiza la llamada. Este identificador debe usarse para recuperar los resultados.
2.  Opcionalmente, obtenga el número de entidades de la enumeración . Llame a **una función GetItemCount,** por ejemplo, llame a [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) [**o PeerGetItemCount.**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)
    > [!Note]  
    > Puede usar el valor devuelto por la **función GetItemCount** para determinar el número de elementos disponibles para recuperar.

     

3.  Recupera un grupo de resultados. Llame a **una función GetNextItem,** por ejemplo, llame a [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Cuando una aplicación llama a una función **GetNextItem,** especifica el número de entidades que se devuelven y, a continuación, la función devuelve un puntero a una matriz de punteros a las entidades y el número de entidades, que siempre es menor o igual que el número especificado. Es posible que una aplicación tenga que llamar a esta función muchas veces, hasta que el número de entidades devueltas sea menor que el número solicitado.

     

4.  Una vez que no se necesiten los datos, libera el puntero a los datos. Llame a **una función FreeData,** por ejemplo, llame a [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData.**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)
    > [!Note]  
    > Para obtener más información, vea [Liberar datos del mismo nivel.](freeing-peer-data.md)

     

5.  Una vez que la aplicación no necesite el identificador de la enumeración, suéltelo. Llame a **una función EndEnumeration,** por ejemplo, llame a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) o [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Ejemplo de una enumeración

El siguiente fragmento de código muestra cómo enumerar las identidades disponibles.


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



 

 



