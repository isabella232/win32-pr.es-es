---
title: Especificar otras opciones de búsqueda con IDirectorySearch
description: La interfaz IDirectorySearch proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificar otras opciones de búsqueda con IDirectorySearch ADSI
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178770"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Especificar otras opciones de búsqueda con IDirectorySearch

La [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona control adicional sobre cómo se realiza la búsqueda mediante el uso de opciones de búsqueda. Estas opciones de búsqueda se establecen rellenando una matriz de estructuras [**\_ DE ADS SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) y llamando al [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Para obtener más información, vea los temas siguientes:

-   [Usar el método SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Búsquedas sincrónicas y asincrónicas con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paginación con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Almacenamiento en caché de resultados con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Realización de una consulta de ámbito de atributo](performing-an-attribute-scoped-query.md)
-   [Ordenar los resultados de la búsqueda con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Búsqueda de referencias con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Límite de tamaño con IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Límite de tiempo del servidor con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Límite de tiempo de cliente con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Devolver solo nombres de atributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




