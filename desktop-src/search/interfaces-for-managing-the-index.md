---
description: 'Windows Search permite administrar el índice de Windows Search con tres componentes principales: administrador de búsqueda, administrador de catálogos y administrador de ámbito de rastreo.'
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para administrar el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275257"
---
# <a name="interfaces-for-managing-the-index"></a>Interfaces para administrar el índice

Windows Search permite administrar el índice de Windows Search con tres componentes principales: administrador de búsqueda, administrador de catálogos y administrador de ámbito de rastreo. Algunas de estas interfaces de administración se pueden usar con privilegios de usuario estándar, pero las que cambian el estado del índice requieren privilegios administrativos.

## <a name="about-the-interfaces-for-managing-the-index"></a>Acerca de las interfaces para administrar el índice

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Interfaces</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Administrador de búsqueda</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>Proporciona métodos para recuperar y establecer información acerca de la búsqueda de Windows:
<ul>
<li>Obtener una instancia del administrador de catálogo para un catálogo específico.</li>
<li>Obtener o establecer la información del proxy.</li>
<li>Obtener información sobre la versión del motor de búsqueda de Windows.</li>
</ul>
Para obtener más información, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">uso del administrador de búsqueda</a>.<br/></td>
</tr>
<tr class="even">
<td>Administrador de catálogos</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Proporciona métodos para administrar un catálogo de búsqueda individual, como provocar una nueva indexación o establecer tiempos de espera. Esta interfaz administra el catálogo en cuatro áreas:
<ul>
<li>Contenido del catálogo: asegurarse de que los nuevos datos se indizan y que otras aplicaciones y componentes funcionan correctamente forzando una reindexación de todo o parte del catálogo o restableciendo todo el catálogo.</li>
<li>Propiedades del catálogo: establecer propiedades que determinan cómo administra el catálogo los tiempos de espera al conectarse a los controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.</li>
<li>Estado del catálogo: obtener información sobre el catálogo, incluidos el estado, el tamaño y el estado de la actividad actual.</li>
<li>Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el administrador de ámbito de rastreo, las notificaciones de cambio de datos y la interfaz <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</li>
</ul>
Para obtener más información, vea <a href="-search-3x-wds-mngidx-catalog-manager.md">usar el administrador de catálogos</a>.<br/></td>
</tr>
<tr class="odd">
<td>Administrador de ámbito de rastreo</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>Proporciona métodos para informar al motor de búsqueda sobre los contenedores que se van a rastrear o inspeccionar, y los elementos de esos contenedores que se van a incluir o excluir en el índice. También puede consultar el administrador de ámbito de rastreo para ver si una dirección URL determinada está en el ámbito de rastreo. Para obtener más información, consulte <a href="-search-3x-wds-extidx-csm.md">uso del administrador de ámbito de rastreo</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Temas relacionados

[Administración del índice](-search-3x-wds-mngidx-overview.md)

[Usar el administrador de búsqueda](-search-3x-wds-mngidx-searchmanager.md)

[Usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)

[Usar el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md)
