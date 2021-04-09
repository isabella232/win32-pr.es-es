---
title: Especificar otras opciones de búsqueda con IDirectorySearch
description: La interfaz IDirectorySearch proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificar otras opciones de búsqueda con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch y otras opciones de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993838"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Especificar otras opciones de búsqueda con IDirectorySearch

La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda. Estas opciones de búsqueda se establecen al rellenar una matriz de estructuras de [**\_ \_ información SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) y llamar al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Para obtener más información, vea los temas siguientes:

-   [Usar el método SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Búsquedas sincrónicas y asincrónicas con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paginación con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Almacenamiento en caché de resultados con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Realización de una consulta de ámbito de atributo](performing-an-attribute-scoped-query.md)
-   [Ordenar los resultados de la búsqueda con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Referencia sobre el seguimiento con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Límite de tamaño con IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Límite de tiempo del servidor con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Límite de tiempo de cliente con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Devolver solo nombres de atributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




