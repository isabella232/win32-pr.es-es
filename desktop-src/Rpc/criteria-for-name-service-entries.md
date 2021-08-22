---
title: Criterios para las entradas del servicio de nombres
description: Criterios para las entradas del servicio de nombres con llamada a procedimiento remoto (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609c545c72687a0b9b73db56d2f08654941e464c790e091ee886159d9e9593ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931124"
---
# <a name="criteria-for-name-service-entries"></a>Criterios para las entradas del servicio de nombres

Los siguientes criterios se usan al procesar las entradas del servicio de nombres:

-   Si proporciona un nombre de entrada distinto de **NULL** para [**RpcNsBindingLookupBegin,**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)esa entrada será la única entrada en la que se busquen identificadores de enlace. Si pasa **NULL,** se buscarán todas las entradas del dominio de inicio de sesión. Tenga en cuenta que esto no incluye dominios de confianza.
-   Si proporciona un identificador de interfaz, los identificadores de enlace se devuelven desde una entrada solo si la sección de interfaz de la entrada contiene una versión compatible de ese UUID de interfaz. Es decir, el número de versión principal debe ser el mismo que el UUID de la interfaz, mientras que el número de versión secundaria debe ser igual o mayor que el de la interfaz.
-   Si proporciona un UUID de objeto, los identificadores de enlace se devuelven desde una entrada solo si la sección UUID del objeto de la entrada contiene ese UUID de objeto concreto.

Si una entrada del servicio de nombres sobrevive a los criterios descritos anteriormente, se recopilan todos los identificadores de enlace de esas entradas. Los identificadores con una secuencia de protocolo que no es compatible con el cliente se descartan y los identificadores restantes se devuelven como la salida de [**RpcNsBindingLookupNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)

 

 




