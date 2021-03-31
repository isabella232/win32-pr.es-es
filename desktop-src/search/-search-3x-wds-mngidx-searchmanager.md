---
description: La interfaz ISearchManager proporciona métodos que realizan cambios en los catálogos.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Usar el administrador de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001003"
---
# <a name="using-the-search-manager"></a>Usar el administrador de búsqueda

La interfaz [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) proporciona métodos que realizan cambios en los catálogos. Los cambios realizados en el nivel **ISearchManager** se aplican globalmente a todos los catálogos usados por el indexador, mientras que los cambios realizados en el nivel [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) se aplican a catálogos específicos. Sin embargo, actualmente, Windows Search solo usa un catálogo, SystemIndex. Puede usar el administrador de búsqueda para hacer lo siguiente:

- Obtener una instancia del administrador de catálogo para el catálogo de búsqueda.
- Obtiene la información de versión del motor de búsqueda de Windows.

Los siguientes métodos de la interfaz [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) pueden ayudarle a administrar los catálogos de búsqueda:

| Método                                                                      | Descripción                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Obtiene un catálogo por nombre y devuelve una instancia de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) para ese catálogo. Esto le permite administrar un catálogo de búsqueda individual.                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Devuelve la versión del indexador en dos enteros: versión principal y versión secundaria. Por ejemplo, el número de versión principal de la búsqueda de Windows 10 es "10" y el número de versión secundaria es "0". En Windows Vista Search y Windows Search 3,0 en Windows XP, el número de versión principal es "3" y el número de versión secundaria es "0". |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Devuelve el número de versión completo del indexador como una cadena: por ejemplo, "10.0.18309.1000". Para Windows 10, esto normalmente coincidirá con el número de versión del sistema operativo. En Windows XP, vista y 7 será diferente.                                                                                                                                        |


Para obtener más información sobre estos métodos, vea la documentación de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .

Los siguientes métodos de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) se reservan para uso futuro. Sin embargo, se implementan y no afectan al indexador o catálogo, ya que solo hay un catálogo para Windows Search en este momento.

- **obtener \_ BypassList**
- **obtener \_ LocalBypass**
- **obtener \_ númeroDePuerto**
- **obtener \_ ProxyName**
- **obtener \_ UseProxy**
- **obtener \_ UserAgent**
- **asignar \_ UserAgent**
- **SetProxy**

**GetParameter** y **SetParameter** también se reservan para uso futuro, pero no se implementan.

## <a name="related-topics"></a>Temas relacionados

[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para administrar el índice](interfaces-for-managing-the-index.md)

[Usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)

[Usar el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md)
