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
# <a name="freeing-peer-data"></a>Liberando datos del mismo nivel

Todos los punteros que devuelven las funciones de infraestructura del mismo nivel deben liberarse mediante [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Solo se debe llamar a estas funciones para las estructuras que se devuelven directamente mediante una función de infraestructura del mismo nivel. No llame a una función FreeData diferente para liberar punteros anidados, por ejemplo, no llame a una función FreeData en los punteros de una estructura de [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) .

## <a name="example-of-freeing-data"></a>Ejemplo de liberación de datos

En el fragmento de código siguiente se muestra cómo recuperar las propiedades asociadas a un gráfico y, a continuación, liberar los datos que se devuelven.


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



 

 



