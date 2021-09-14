---
description: Todos los punteros que devuelven las funciones de infraestructura del mismo nivel deben liberarse mediante PeerGraphFreeData o PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Liberar datos del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073925"
---
# <a name="freeing-peer-data"></a>Liberar datos del mismo nivel

Todos los punteros que devuelven las funciones de infraestructura del mismo nivel deben liberarse mediante [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) [**o PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Solo se debe llamar a estas funciones para las estructuras devueltas directamente por una función de infraestructura del mismo nivel. No llame a otra función FreeData para liberar punteros anidados; por ejemplo, no llame a una función FreeData en los punteros de una [**estructura \_ PEER RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record)

## <a name="example-of-freeing-data"></a>Ejemplo de liberar datos

El siguiente fragmento de código muestra cómo recuperar las propiedades asociadas a un gráfico y, a continuación, liberar los datos que se devuelven.


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



 

 



