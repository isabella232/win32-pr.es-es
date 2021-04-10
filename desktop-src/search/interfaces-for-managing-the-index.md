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
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="51457-103">Interfaces para administrar el índice</span><span class="sxs-lookup"><span data-stu-id="51457-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="51457-104">Windows Search permite administrar el índice de Windows Search con tres componentes principales: administrador de búsqueda, administrador de catálogos y administrador de ámbito de rastreo.</span><span class="sxs-lookup"><span data-stu-id="51457-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="51457-105">Algunas de estas interfaces de administración se pueden usar con privilegios de usuario estándar, pero las que cambian el estado del índice requieren privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="51457-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="51457-106">Acerca de las interfaces para administrar el índice</span><span class="sxs-lookup"><span data-stu-id="51457-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51457-107">Componente</span><span class="sxs-lookup"><span data-stu-id="51457-107">Component</span></span></th>
<th><span data-ttu-id="51457-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="51457-108">Interfaces</span></span></th>
<th><span data-ttu-id="51457-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="51457-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51457-110">Administrador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="51457-110">Search Manager</span></span></td>
<td><span data-ttu-id="51457-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="51457-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="51457-112">Proporciona métodos para recuperar y establecer información acerca de la búsqueda de Windows:</span><span class="sxs-lookup"><span data-stu-id="51457-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="51457-113">Obtener una instancia del administrador de catálogo para un catálogo específico.</span><span class="sxs-lookup"><span data-stu-id="51457-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="51457-114">Obtener o establecer la información del proxy.</span><span class="sxs-lookup"><span data-stu-id="51457-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="51457-115">Obtener información sobre la versión del motor de búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="51457-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="51457-116">Para obtener más información, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">uso del administrador de búsqueda</a>.</span><span class="sxs-lookup"><span data-stu-id="51457-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51457-117">Administrador de catálogos</span><span class="sxs-lookup"><span data-stu-id="51457-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="51457-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="51457-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="51457-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="51457-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="51457-120">Proporciona métodos para administrar un catálogo de búsqueda individual, como provocar una nueva indexación o establecer tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="51457-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="51457-121">Esta interfaz administra el catálogo en cuatro áreas:</span><span class="sxs-lookup"><span data-stu-id="51457-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="51457-122">Contenido del catálogo: asegurarse de que los nuevos datos se indizan y que otras aplicaciones y componentes funcionan correctamente forzando una reindexación de todo o parte del catálogo o restableciendo todo el catálogo.</span><span class="sxs-lookup"><span data-stu-id="51457-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="51457-123">Propiedades del catálogo: establecer propiedades que determinan cómo administra el catálogo los tiempos de espera al conectarse a los controladores de protocolo y cómo se tratan las marcas diacríticas en las búsquedas.</span><span class="sxs-lookup"><span data-stu-id="51457-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="51457-124">Estado del catálogo: obtener información sobre el catálogo, incluidos el estado, el tamaño y el estado de la actividad actual.</span><span class="sxs-lookup"><span data-stu-id="51457-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="51457-125">Acceso a otras interfaces: recuperación de otras interfaces relacionadas con la búsqueda requeridas por el administrador de ámbito de rastreo, las notificaciones de cambio de datos y la interfaz <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51457-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="51457-126">Para obtener más información, vea <a href="-search-3x-wds-mngidx-catalog-manager.md">usar el administrador de catálogos</a>.</span><span class="sxs-lookup"><span data-stu-id="51457-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51457-127">Administrador de ámbito de rastreo</span><span class="sxs-lookup"><span data-stu-id="51457-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="51457-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="51457-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="51457-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="51457-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="51457-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="51457-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="51457-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="51457-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="51457-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="51457-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="51457-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="51457-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="51457-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="51457-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="51457-135">Proporciona métodos para informar al motor de búsqueda sobre los contenedores que se van a rastrear o inspeccionar, y los elementos de esos contenedores que se van a incluir o excluir en el índice.</span><span class="sxs-lookup"><span data-stu-id="51457-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="51457-136">También puede consultar el administrador de ámbito de rastreo para ver si una dirección URL determinada está en el ámbito de rastreo.</span><span class="sxs-lookup"><span data-stu-id="51457-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="51457-137">Para obtener más información, consulte <a href="-search-3x-wds-extidx-csm.md">uso del administrador de ámbito de rastreo</a>.</span><span class="sxs-lookup"><span data-stu-id="51457-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="51457-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51457-138">Related topics</span></span>

[<span data-ttu-id="51457-139">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="51457-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="51457-140">Usar el administrador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="51457-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="51457-141">Usar el administrador de catálogos</span><span class="sxs-lookup"><span data-stu-id="51457-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="51457-142">Usar el administrador de ámbito de rastreo</span><span class="sxs-lookup"><span data-stu-id="51457-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
