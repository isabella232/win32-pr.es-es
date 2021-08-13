---
title: Búsquedas sincrónicas y asincrónicas con IDirectorySearch
description: Al realizar una búsqueda mediante la interfaz IDirectorySearch, el método IDirectorySearch ExecuteSearch no envía la solicitud de búsqueda al servidor.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Búsquedas sincrónicas y asincrónicas con ADSI de IDirectorySearch
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Búsquedas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3891351bc7ebb9872938f3022f5397100e0be74ca6cd2d86d21a2535f010cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690202"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Búsquedas sincrónicas y asincrónicas con IDirectorySearch

Cuando se realiza una búsqueda mediante la [**interfaz IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) el método [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) no envía la solicitud de búsqueda al servidor. Este método solo guarda los parámetros de búsqueda. La solicitud de búsqueda se envía realmente cuando se llama a [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

Para Active Directory búsquedas, la diferencia principal entre sincrónico y asincrónico es cuando se devuelve la primera fila del resultado, es decir, cuando se devuelve la primera llamada [**a GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)

En una búsqueda sincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido y devuelto todo el conjunto de resultados al cliente. Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.

En una búsqueda asincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido la primera fila del conjunto de resultados. Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.

El tipo de búsqueda predeterminado es sincrónico. Para especificar una búsqueda asincrónica, establezca una opción de búsqueda **\_ ADS SEARCHPREF \_ ASYNCHRONOUS** con un valor **\_ BOOLEANo ADSTYPE** **de TRUE** en la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Esta operación se muestra en el ejemplo de código siguiente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




