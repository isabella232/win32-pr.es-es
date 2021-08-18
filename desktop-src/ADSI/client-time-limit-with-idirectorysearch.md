---
title: Límite de tiempo de cliente con IDirectorySearch
description: Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda e intentarlo de nuevo más adelante.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Límite de tiempo de cliente con IDirectorySearch
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Límite de tiempo de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692514"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Límite de tiempo de cliente con IDirectorySearch

Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda e intentarlo de nuevo más adelante.

La preferencia de límite de tiempo de cliente es útil cuando un cliente solicita una búsqueda asincrónica. En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados. Es posible que el servidor pueda desconectarse sin notificar al cliente. En este caso, el cliente no tendrá ninguna notificación de si el servidor sigue procesando la consulta o si ya no está disponible. La preferencia de límite de tiempo de cliente proporciona al cliente cierto control de situaciones como esta.

El valor predeterminado para el límite de tiempo de cliente no es ningún límite. Para establecer un límite de tiempo de cliente, establezca una opción de búsqueda **\_ SEARCHPREF \_ TIMEOUT** de ADS con un valor **DE ADSTYPE \_ INTEGER** que contenga el límite de tiempo de cliente, en segundos, en la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Un límite de tiempo de cliente de cero indica que no hay límite de tiempo.

En el ejemplo de código siguiente se muestra cómo establecer el límite de tiempo del cliente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




