---
title: Búsquedas sincrónicas y asincrónicas con IDirectorySearch
description: Cuando realiza una búsqueda mediante la interfaz IDirectorySearch, el método ExecuteSearch de IDirectorySearch no envía la solicitud de búsqueda al servidor.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Búsquedas sincrónicas y asincrónicas con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, búsquedas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418347"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Búsquedas sincrónicas y asincrónicas con IDirectorySearch

Cuando realiza una búsqueda mediante la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , el método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) no envía la solicitud de búsqueda al servidor. Este método solo guarda los parámetros de búsqueda. La solicitud de búsqueda se envía realmente cuando se llama a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

En el caso de las búsquedas de Active Directory, la diferencia principal entre sincrónicos y asincrónicos es cuando se devuelve la primera fila del resultado, es decir, cuando la primera llamada a [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) devuelve.

En una búsqueda sincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido y devuelto todo el conjunto de resultados al cliente. Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.

En una búsqueda asincrónica, si la paginación no está habilitada, se devuelve la primera fila cuando el servidor ha construido la primera fila del conjunto de resultados. Si la paginación está habilitada, se devuelve la primera fila cuando se devuelve la primera página del conjunto de resultados.

El tipo de búsqueda predeterminado es sincrónico. Para especificar una búsqueda asincrónica, establezca una opción de búsqueda **\_ \_ asincrónica de ADS SEARCHPREF** con un **valor \_ booleano ADSTYPE** de **true** en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Esta operación se muestra en el ejemplo de código siguiente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




