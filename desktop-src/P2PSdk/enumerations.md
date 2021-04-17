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
# <a name="enumerations-peer-infrastructure"></a>Enumeraciones (infraestructura del mismo nivel)

Mediante el uso de enumeraciones, puede obtener una lista de todas las entidades del mismo nivel específicas que coincidan con los criterios.

**Para obtener una enumeración y recuperar los resultados**

1.  Obtener un identificador de la enumeración. Llame a una función **PeerEnum** , por ejemplo, llame a la función de gráficos del mismo nivel de [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) . Las funciones **PeerEnum** crean la enumeración y devuelven un identificador a esa enumeración a la aplicación que realiza la llamada. Este identificador debe usarse para recuperar los resultados.
2.  Opcionalmente, obtenga el número de entidades en la enumeración. Llame a una función **GetItemCount** , por ejemplo, llame a [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) o [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).
    > [!Note]  
    > Puede usar el valor devuelto por la función **GetItemCount** para determinar el número de elementos disponibles para recuperar.

     

3.  Recupera un grupo de resultados. Llame a una función **GetNextItem** , por ejemplo, llame a [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Cuando una aplicación llama a una función **GetNextItem** , especifica el número de entidades que se van a devolver y, a continuación, la función devuelve un puntero a una matriz de punteros a las entidades y el número de entidades, que es siempre menor o igual que el número especificado. Es posible que una aplicación necesite llamar a esta función muchas veces, hasta que el número de entidades devueltas sea menor que el número solicitado.

     

4.  Después de que no se necesiten los datos, libere el puntero a los datos. Llame a una función **FreeData** , por ejemplo, llame a [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).
    > [!Note]  
    > Para obtener más información, vea [liberar datos del mismo nivel](freeing-peer-data.md).

     

5.  Después de que la aplicación no necesite el identificador de la enumeración, suéltelo. Llame a una función **EndEnumeration** , por ejemplo, llame a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) o [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Ejemplo de una enumeración

El siguiente fragmento de código muestra cómo enumerar a través de identidades disponibles.


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



 

 



