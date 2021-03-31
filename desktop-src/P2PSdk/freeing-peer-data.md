---
description: Todos los punteros que devuelven las funciones de infraestructura del mismo nivel deben liberarse mediante PeerGraphFreeData o PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Liberando datos del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082657"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="06eb2-103">Liberando datos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="06eb2-103">Freeing Peer Data</span></span>

<span data-ttu-id="06eb2-104">Todos los punteros que devuelven las funciones de infraestructura del mismo nivel deben liberarse mediante [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="06eb2-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="06eb2-105">Solo se debe llamar a estas funciones para las estructuras que se devuelven directamente mediante una función de infraestructura del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="06eb2-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="06eb2-106">No llame a una función FreeData diferente para liberar punteros anidados, por ejemplo, no llame a una función FreeData en los punteros de una estructura de [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="06eb2-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="06eb2-107">Ejemplo de liberación de datos</span><span class="sxs-lookup"><span data-stu-id="06eb2-107">Example of Freeing Data</span></span>

<span data-ttu-id="06eb2-108">En el fragmento de código siguiente se muestra cómo recuperar las propiedades asociadas a un gráfico y, a continuación, liberar los datos que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="06eb2-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



