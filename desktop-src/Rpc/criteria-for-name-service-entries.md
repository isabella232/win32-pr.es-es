---
title: Criterios para las entradas del servicio de nombres
description: Criterios para las entradas del servicio de nombres con llamada a procedimiento remoto (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486890"
---
# <a name="criteria-for-name-service-entries"></a>Criterios para las entradas del servicio de nombres

Cuando se procesan entradas de servicio de nombres, se usan los siguientes criterios:

-   Si proporciona un nombre de entrada que no sea **null** para [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), esa entrada será la única entrada buscada para los identificadores de enlace. Si pasa **null**, se buscarán todas las entradas del dominio de inicio de sesión. Tenga en cuenta que esto no incluye dominios de confianza.
-   Si proporciona un identificador de interfaz, solo se devuelven los identificadores de enlace de una entrada si la sección de la interfaz de la entrada contiene una versión compatible de ese UUID de interfaz. Es decir, el número de versión principal debe ser el mismo que el UUID de la interfaz, mientras que el número de versión secundaria debe ser igual o mayor que el suyo.
-   Si proporciona un UUID de objeto, solo se devuelven los identificadores de enlace de una entrada si la sección de UUID del objeto de la entrada contiene ese UUID de objeto concreto.

Si una entrada del servicio de nombres sobrevive los criterios descritos anteriormente, se recopilan todos los identificadores de enlace de esas entradas. Los identificadores con una secuencia de protocolo que no es compatible con el cliente se descartan y se devuelven los controladores restantes como resultado de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).

 

 




