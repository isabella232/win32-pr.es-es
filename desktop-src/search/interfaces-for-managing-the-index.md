---
description: Obtenga información Windows Search le permite administrar el índice Windows Search con el Administrador de búsqueda, el Administrador de catálogos y Administrador del ámbito de rastreo.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para administrar el índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120020"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="fb449-103">Interfaces para administrar el índice</span><span class="sxs-lookup"><span data-stu-id="fb449-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="fb449-104">Windows Search permite administrar el índice de Windows Search con tres componentes principales: Administrador de búsqueda, Administrador de catálogos y Administrador del ámbito de rastreo.</span><span class="sxs-lookup"><span data-stu-id="fb449-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="fb449-105">Algunas de estas interfaces de administración se pueden usar con privilegios de usuario estándar, pero las que cambian el estado del índice requieren privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="fb449-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="fb449-106">Acerca de las interfaces para administrar el índice</span><span class="sxs-lookup"><span data-stu-id="fb449-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb449-107">Componente</span><span class="sxs-lookup"><span data-stu-id="fb449-107">Component</span></span></th>
<th><span data-ttu-id="fb449-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fb449-108">Interfaces</span></span></th>
<th><span data-ttu-id="fb449-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb449-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb449-110">Administrador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="fb449-110">Search Manager</span></span></td>
<td><span data-ttu-id="fb449-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="fb449-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="fb449-112">Proporciona métodos para recuperar y establecer información sobre Windows Search:</span><span class="sxs-lookup"><span data-stu-id="fb449-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="fb449-113">Obtener una instancia del Administrador de catálogos para un catálogo específico.</span><span class="sxs-lookup"><span data-stu-id="fb449-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="fb449-114">Obtención o configuración de información de proxy.</span><span class="sxs-lookup"><span data-stu-id="fb449-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="fb449-115">Obtención de información de versión sobre el motor Windows Search datos.</span><span class="sxs-lookup"><span data-stu-id="fb449-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="fb449-116">Para obtener más información, <a href="-search-3x-wds-mngidx-searchmanager.md">vea Uso del Administrador de búsqueda.</a></span><span class="sxs-lookup"><span data-stu-id="fb449-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb449-117">Administrador de catálogos</span><span class="sxs-lookup"><span data-stu-id="fb449-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="fb449-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="fb449-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="fb449-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="fb449-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="fb449-120">Proporciona métodos para administrar un catálogo de búsqueda individual, como provocar una nueva indexación o establecer tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="fb449-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="fb449-121">Esta interfaz administra el catálogo en cuatro áreas:</span><span class="sxs-lookup"><span data-stu-id="fb449-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="fb449-122">Contenido del catálogo: garantiza que los nuevos datos se indexe y que otras aplicaciones y componentes funcionen correctamente forzando una nueva indexación de todo el catálogo o parte del mismo o restableciendo todo el catálogo.</span><span class="sxs-lookup"><span data-stu-id="fb449-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="fb449-123">Propiedades del catálogo: establece propiedades que determinan cómo administra el catálogo los tiempos de espera al conectarse a controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.</span><span class="sxs-lookup"><span data-stu-id="fb449-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="fb449-124">Estado del catálogo: obtener información sobre el catálogo, incluido el estado, el tamaño y el estado de actividad actual.</span><span class="sxs-lookup"><span data-stu-id="fb449-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="fb449-125">Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el Administrador del ámbito de rastreo, las notificaciones de cambio de datos y la <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>interfaz ISearchQueryHelper.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb449-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="fb449-126">Para obtener más información, <a href="-search-3x-wds-mngidx-catalog-manager.md">vea Usar el Administrador de catálogos</a>.</span><span class="sxs-lookup"><span data-stu-id="fb449-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb449-127">Administrador del ámbito de rastreo</span><span class="sxs-lookup"><span data-stu-id="fb449-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="fb449-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb449-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="fb449-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="fb449-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="fb449-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb449-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="fb449-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="fb449-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="fb449-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb449-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="fb449-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb449-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="fb449-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="fb449-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="fb449-135">Proporciona métodos para informar al motor de búsqueda sobre los contenedores que se rastrearán o observarán, y los elementos de esos contenedores que se incluirán o excluirán en el índice.</span><span class="sxs-lookup"><span data-stu-id="fb449-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="fb449-136">También puede consultar el Administrador del ámbito de rastreo para ver si una dirección URL determinada está en el ámbito de rastreo.</span><span class="sxs-lookup"><span data-stu-id="fb449-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="fb449-137">Para obtener más información, <a href="-search-3x-wds-extidx-csm.md">vea Using the Administrador del ámbito de rastreo</a>.</span><span class="sxs-lookup"><span data-stu-id="fb449-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="fb449-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb449-138">Related topics</span></span>

[<span data-ttu-id="fb449-139">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="fb449-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="fb449-140">Uso del Administrador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="fb449-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="fb449-141">Uso del Administrador de catálogos</span><span class="sxs-lookup"><span data-stu-id="fb449-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="fb449-142">Uso del Administrador del ámbito de rastreo</span><span class="sxs-lookup"><span data-stu-id="fb449-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
