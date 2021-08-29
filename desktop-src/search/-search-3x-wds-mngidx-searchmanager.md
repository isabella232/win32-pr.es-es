---
description: La interfaz ISearchManager proporciona métodos que hacen cambios en los catálogos.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Uso del Administrador de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b23097078d8e6de4c23fce0f0ab368367d9f62247aae50c01d43c5ad17f3eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094976"
---
# <a name="using-the-search-manager"></a>Uso del Administrador de búsqueda

La [**interfaz ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) proporciona métodos que hacen cambios en los catálogos. Los cambios realizados en el nivel **de ISearchManager** se aplican globalmente a todos los catálogos usados por el indexador, mientras que los cambios realizados en el nivel [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) se aplican a catálogos específicos. Sin embargo, actualmente, Windows Search solo usa un catálogo, SystemIndex. Puede usar el Administrador de búsqueda para hacer lo siguiente:

- Obtenga una instancia del Administrador de catálogos para el catálogo de búsqueda.
- Obtenga información de versión sobre el motor Windows Search.

Los métodos siguientes de la [**interfaz ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) pueden ayudarle a administrar los catálogos de búsqueda:

| Método                                                                      | Descripción                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Obtiene un catálogo por nombre y devuelve una instancia de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) para ese catálogo. Esto le permite administrar un catálogo de búsqueda individual.                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Devuelve la versión del indexador en dos enteros: versión principal y versión secundaria. Por ejemplo, el número de versión principal de Windows 10 Search es "10" y el número de versión secundaria es "0". Por Windows Vista Search y Windows Search 3.0 en Windows XP, el número de versión principal es "3" y el número de versión secundaria es "0". |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Devuelve el número de versión completo del indexador como una cadena: por ejemplo, "10.0.18309.1000". Por Windows 10 normalmente coincidirá con el número de versión del sistema operativo. Para Windows XP, Vista y 7 será diferente.                                                                                                                                        |


Para obtener más información sobre estos métodos, vea la [**documentación de ISearchManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

Los siguientes [**métodos de ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) están reservados para su uso futuro. Sin embargo, se implementan y no afectan al indexador o catálogo, ya que en este momento solo hay un catálogo para Windows Search.

- **get \_ BypassList**
- **get \_ LocalBypass**
- **get \_ PortNumber**
- **get \_ ProxyName**
- **get \_ UseProxy**
- **get \_ UserAgent**
- **put \_ UserAgent**
- **SetProxy**

**GetParameter** y **SetParameter** también se reservan para su uso futuro, pero no se implementan.

## <a name="related-topics"></a>Temas relacionados

[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para administrar el índice](interfaces-for-managing-the-index.md)

[Uso del Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)

[Uso del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md)
