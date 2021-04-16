---
title: Límite de tiempo de cliente con IDirectorySearch
description: Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda y volver a intentarlo más tarde.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Límite de tiempo de cliente con IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tiempo de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656191"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Límite de tiempo de cliente con IDirectorySearch

Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda y volver a intentarlo más tarde.

La preferencia de límite de tiempo de cliente es útil cuando un cliente solicita una búsqueda asincrónica. En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados. Es posible que el servidor se quede sin conexión sin notificar al cliente. En este caso, el cliente no recibirá ninguna notificación de si el servidor sigue procesando la consulta o si ya no lo está. La preferencia de límite de tiempo de cliente proporciona al cliente cierto control de situaciones como esta.

El valor predeterminado para el límite de tiempo de cliente es sin límite. Para establecer un límite de tiempo de cliente, establezca una opción de búsqueda de SEARCHPREF de tiempo de **\_ \_ espera de ADS** con un valor **\_ entero de ADSTYPE** que contenga el límite de tiempo de cliente, en segundos, en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Un límite de tiempo de cliente de cero indica que no hay ningún límite de tiempo.

En el ejemplo de código siguiente se muestra cómo establecer el límite de tiempo del cliente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




