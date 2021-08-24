---
description: Obtenga información Windows Search le permite administrar el índice Windows Search con el Administrador de búsqueda, el Administrador de catálogos y Administrador del ámbito de rastreo.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para administrar el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505752cc496d55057eece87bd673b31a323c6597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476801"
---
# <a name="interfaces-for-managing-the-index"></a>Interfaces para administrar el índice

Windows La búsqueda le permite administrar el índice Windows Search con tres componentes principales: Administrador de búsqueda, Administrador de catálogos y Administrador del ámbito de rastreo. Algunas de estas interfaces de administración se pueden usar con privilegios de usuario estándar, pero las que cambian el estado del índice requieren privilegios administrativos.

## <a name="about-the-interfaces-for-managing-the-index"></a>Acerca de las interfaces para administrar el índice


| Componente | Interfaces | Descripción | 
|-----------|------------|-------------|
| Administrador de búsquedas | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a> | Proporciona métodos para recuperar y establecer información sobre Windows Search:<ul><li>Obtener una instancia del Administrador de catálogos para un catálogo específico.</li><li>Obtención o configuración de información de proxy.</li><li>Obtener información de versión sobre el motor Windows Search.</li></ul>Para obtener más información, <a href="-search-3x-wds-mngidx-searchmanager.md">vea Using the Search Manager</a>.<br /> | 
| Administrador de catálogos | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br /> | Proporciona métodos para administrar un catálogo de búsqueda individual, como provocar una nueva indexación o establecer tiempos de espera. Esta interfaz administra el catálogo en cuatro áreas:<ul><li>Contenido del catálogo: garantiza que los nuevos datos estén indexados y que otras aplicaciones y componentes funcionen correctamente forzando una nueva indexación de todo el catálogo o parte del mismo o restableciendo todo el catálogo.</li><li>Propiedades del catálogo: establecer propiedades que determinan cómo administra el catálogo los tiempos de espera al conectarse a controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.</li><li>Estado del catálogo: obtención de información sobre el catálogo, incluido el estado, el tamaño y el estado actual de la actividad.</li><li>Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el Administrador del ámbito de rastreo, las notificaciones de cambio de datos y la <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>interfaz ISearchQueryHelper.</strong></a></li></ul>Para obtener más información, <a href="-search-3x-wds-mngidx-catalog-manager.md">vea Uso del Administrador de catálogos.</a><br /> | 
| Administrador del ámbito de rastreo | <a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br /><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br /> | Proporciona métodos para informar al motor de búsqueda sobre los contenedores que se rastrearán o observarán, y los elementos de esos contenedores que se incluirán o excluirán en el índice. También puede consultar el Administrador del ámbito de rastreo para ver si una dirección URL determinada está en el ámbito de rastreo. Para obtener más información, <a href="-search-3x-wds-extidx-csm.md">vea Using the Administrador del ámbito de rastreo</a>.<br /> | 


## <a name="related-topics"></a>Temas relacionados

[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Uso del Administrador de búsqueda](-search-3x-wds-mngidx-searchmanager.md)

[Uso del Administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)

[Uso del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md)
